---
layout: post
title: Playing with .NET (dotnet) and IronFunctions
date: '2016-12-05 22:15:39'
tags:
- mozilla
- serverless
- dotnet
- net
- microsoft
- open-source
- tech
---

Again if you missed it, [IronFunctions](https://github.com/iron-io/functions) is open-source, lambda compatible, on-premise, language agnostic, server-less compute service.

While AWS Lambda only supports Java, Python and Node.js, Iron Functions allows you to use any language you desire by running your code in containers.

With Microsoft being one of the biggest players in open source and .NET going cross-platform it was only right to add support for it in the IronFunctions's [fn tool](https://github.com/iron-io/functions/tree/master/fn).

## TL;DR:

The following demos a .NET function that takes in a URL for an image and generates a MD5 checksum hash for it:

![](/content/images/2016/12/ezgif-com-gif-maker.gif)

## Using dotnet with functions

Make sure you downloaded and installed [dotnet](https://www.microsoft.com/net/core). Now create an empty dotnet project in the directory of your function:

```bash
dotnet new
```

By default dotnet creates a ```Program.cs``` file with a main method. To make it work with IronFunction's `fn` tool please rename it to ```func.cs```.

```bash
mv Program.cs func.cs
```

Now change the code as you desire to do whatever magic you need it to do. In our case the code takes in a URL for an image and generates a MD5 checksum hash for it. The code is the following:

```cs
using System;
using System.Text;
using System.Security.Cryptography;
using System.IO;

namespace ConsoleApplication
{
    public class Program
    {
        public static void Main(string[] args)
        {
            // if nothing is being piped in, then exit
            if (!IsPipedInput())
                return;

            var input = Console.In.ReadToEnd();
            var stream = DownloadRemoteImageFile(input);
            var hash = CreateChecksum(stream);
            Console.WriteLine(hash);
        }

        private static bool IsPipedInput()
        {
            try
            {
                bool isKey = Console.KeyAvailable;
                return false;
            }
            catch
            {
                return true;
            }
        }
        private static byte[] DownloadRemoteImageFile(string uri)
        {

            var request = System.Net.WebRequest.CreateHttp(uri);
            var response = request.GetResponseAsync().Result;
            var stream = response.GetResponseStream();
            using (MemoryStream ms = new MemoryStream())
            {
                stream.CopyTo(ms);
                return ms.ToArray();
            }
        }
        private static string CreateChecksum(byte[] stream)
        {
            using (var md5 = MD5.Create())
            {
                var hash = md5.ComputeHash(stream);
                var sBuilder = new StringBuilder();

                // Loop through each byte of the hashed data
                // and format each one as a hexadecimal string.
                for (int i = 0; i < hash.Length; i++)
                {
                    sBuilder.Append(hash[i].ToString("x2"));
                }

                // Return the hexadecimal string.
                return sBuilder.ToString();
            }
        }
    }
}
```

**Note:**
*IO with an IronFunction is done via **stdin** and **stdout**. This code*

## Using with IronFunctions

Let's first init our code to become IronFunctions deployable:
```bash
fn init <username>/<funcname>
```

Since IronFunctions relies on Docker to work (we will add rkt support soon) the `<username>` is required to publish to docker hub. The `<funcname>` is the identifier of the function. 

In our case we will use `dotnethash` as the `<funcname>`, so the command will look like:

```bash
fn init seiflotfy/dotnethash
```

When running the command it will create the ```func.yaml``` file required by functions, which can be built by running:

## Push to docker
```bash
fn push
```

This will create a docker image and push the image to docker.

## Publishing to IronFunctions

To publish to IronFunctions run ...

```bash
fn routes create <app_name>
```

where `<app_name>` is (no surprise here) the name of the app, which can encompass many functions.

This creates a full path in the form of `http://<host>:<port>/r/<app_name>/<function>`

In my case, I will call the app ```myapp```:
```bash
fn routes create myapp
```
## Calling

Now you can 
```bash
fn call <app_name> <funcname>
```

or

```bash
curl http://<host>:<port>/r/<app_name>/<function>
```

So in my case

```bash
echo http://lorempixel.com/1920/1920/ | fn call myapp /dotnethash
```
or

```bash
curl -X POST -d 'http://lorempixel.com/1920/1920/'  http://localhost:8080/r/myapp/dotnethash
```

## What now?
You can find the whole code in the [examples on GitHub](https://github.com/iron-io/functions/tree/master/examples/hash). Feel free to join the Iron.io Team on [Slack](https://open-iron.herokuapp.com).
Feel free to write your own examples in any of your favourite programming languages such as Lua or Elixir and create a PR :)