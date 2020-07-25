---
layout: post
title: Importing AWS Lambda to IronFunctions
date: '2016-11-24 13:13:00'
tags:
- mozilla
- severless
- aws
- lambda
- functions
- devops
- docker
- gnome
- ubuntu
---

### Imagine AWS Lambda being:


* **On-Premise** (host it anywhere)
* **Language Agnostic** (writing lambda functions in any language: Go, Rust, Python, Scala, Elixir you name it...)
* **Horizontally Scalable**
* **Open-Source**



### Would be nice wouldn't it?
[![IronFunction](http://open.iron.io/img/ironio-robot.png)](http://open.iron.io). 

Well fear not [Iron.io](http://iron.io) released [IronFunctions](http://open.iron.io) last week and its all that.

IronFunction supports a simple stdin/stdout API, as well as being able to import your existing functions directly from AWS Lambda.


### Getting started!

You can grab the latest code from [GitHub](https://github.com/iron-io/functions) or just run it in docker:

```bash
docker run --rm -it --name functions --privileged -v $PWD/data:/app/data -p 8080:8080 iron/functions
```

Currently IronFunctions supports importing the following languages from AWS Lambda:

* **Python**: 2.7
* **Java8**: 1.80
* **NodeJS**: 0.10
* **NodeJS**: *[4.3 in development](https://github.com/junedev/lambda/tree/node4.3)*


### The almighty fn tool

The [fn](https://github.com/iron-io/functions/fn/) tool includes a set of commands to act on Lambda functions. Most of these are described in the [getting-started](https://github.com/iron-io/functions/blob/master/docs/lambda/getting-started.md) in the repository. One more subcommand is `aws-import`.
If you have an existing AWS Lambda function, you can use this command to automatically convert it to a Docker image that is ready to be deployed on other platforms.

### Credentials

To use this, either have your AWS access key and secret key set in config files, or in environment variables. In addition, you'll want to set a default region. You can use the `aws` tool to set this up. Full instructions are in the [AWS documentation][awscli].

[awscli]: http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html#cli-config-files

### Importing

The aws-import command is constructed as follows:

```bash
fn lambda aws-import <arn> <region> <image>
```

* **arn**: describes the ARN formats which uniquely identify the AWS lambda resource
* **region**: region on which the lambda is hosted
* **image**: the name of the created docker image which should have the format <username>/<image-name>

Assuming you have a lambda with the following arn `arn:aws:lambda:us-west-2:123141564251:function:my-function`, the following command:

```bash
fn lambda aws-import arn:aws:lambda:us-west-2:123141564251:function:my-function us-east-1 user/my-function
```

will import the function code from the region `us-east-1` to a directory called `./user/my-function`. Inside the directory you will find the `function.yml`, `Dockerfile`, and all the files needed for running the function.

Using Lambda with Docker Hub and IronFunctions requires that the Docker image be named `<Docker Hub username>/<image name>`. This is used to uniquely identify images on Docker Hub. You should use the `<Docker Hub username>/<image name>` as the image name with `aws-import` to create a correctly named image.

### Publish and Voila!
You can then publish the imported lambda as follows:
```
./fn publish -d ./user/my-function
```

Now the function can be reached via ```http://$HOSTNAME/r/user/my-function```

Make sure you check out the [importing documentation](https://github.com/iron-io/functions/tree/master/docs/lambda), and feel free to hang out and ask question on the slack channel. <a href="https://open-iron.herokuapp.com">
              <img src="https://open-iron.herokuapp.com/badge.svg" alt="Join Community" height="24" style="margin:0;">
            </a>

Stay tuned for my next blog post on adding **Cargo** and **Rust** support to the Fn Tools :D