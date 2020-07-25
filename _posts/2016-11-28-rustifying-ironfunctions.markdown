---
layout: post
title: Rustifying IronFunctions
date: '2016-11-28 21:47:56'
tags:
- mozilla
- gnome
- ubuntu
- lambda
- serverless
---

As mentioned in my [previous blog post](http://seif.codes/importing-aws-lambda-to-ironfunctions) there is new open-source, lambda compatible, on-premise, language agnostic, server-less compute service called [IronFunctions](https://github.com/iron-io/functions).
![IronFunctions](/content/images/2016/11/logo-black-400w.png)

While IronFunctions is written in Go. Rust is still very much admired language and it was decided to add support for it in the [fn tool](https://github.com/iron-io/functions/tree/master/fn).

So now you can use the [fn tool](https://github.com/iron-io/functions/tree/master/fn) to create and publish functions written in rust.

## Using rust with functions

The easiest way to create a iron function in rust is via ***cargo*** and ***fn***. 

## Prerequisites
First create an empty rust project as follows:
```bash
$ cargo init --name func --bin
```

Make sure the project name is ***func*** and is of type ***bin***. Now just edit your code, a good example is the following "Hello" example:

```c++
use std::io;
use std::io::Read;

fn main() {
    let mut buffer = String::new();
    let stdin = io::stdin();
    if stdin.lock().read_to_string(&mut buffer).is_ok() {
        println!("Hello {}", buffer.trim());
    }
}
```
You can find this example code in the [repo](https://github.com/iron-io/functions/tree/master/examples/hello/rust).

Once done you can create an iron function.

## Creating a function

```bash
$ fn init --runtime=rust <username>/<funcname>
```
in my case its ```fn init --runtime=rust seiflotfy/rustyfunc```, which will create the ```func.yaml``` file required by functions.

## Building the function

```bash
$ fn build
```

Will create a docker image ```<username>/<funcname>``` (again in my case seiflotfy/rustyfunc).

## Testing

You can run this locally without pushing it to functions yet by running:
```bash
$ echo Jon Snow | fn run
Hello Jon Snow
```

## Publishing

In the directory of your rust code do the following:
```bash
$ fn publish -v -f -d ./
```
This will publish you code to your functions service.

## Running it

Now to call it on the functions service:
```bash
$ echo Jon Snow | fn call seiflotfy rustyfunc 
```
which is the equivalent of:
```bash
$ curl -X POST -d 'Jon Snow' http://localhost:8080/r/seiflotfy/rustyfunc
```

## Next
In the next post I will be writing a more computation intensive rust function to test/benchmark IronFunctions, so stay tune :D