---
layout: post
title:  "CMake: What You Need to Know - Part 1"
---
<img src="{{ site.url }}/assets/jeff-web.jpg" 
     alt="Jeff Bell" 
     style="width: 200px; height: 200px; padding-bottom: 25px" />  
In my [last post][last-post] I talked about some recent discoveries I've had
with using [CMake][cmake]. I decided today I would take the time to talk a
little about what I learned. This will be the first part of a few posts that
will walk through one way I have found to use CMake in a logical, and helpful
manner.

# What is CMake?

Well, according to their [website][cmake]:

> CMake is an open-source, cross-platform family of tools designed to build, 
> test and package software. CMake is used to control the software compilation 
> process using simple platform and compiler independent configuration files, 
> and generate native makefiles and workspaces that can be used in the compiler
> environment of your choice. The suite of CMake tools were created by Kitware
> in response to the need for a powerful, cross-platform build environment for
> open-source projects such as ITK and VTK.

Great, so what does that mean to the average user?

* CMake is a Makefile generator (or Makefile equivalent).
* CMake is cross-platform.
* CMake _should_ make your life easier.

# How do I use CMake?

CMake is run using files called `CMakeLists.txt`. Inside of these files is
where you will specify the configuration options that you would normally use
in a Makefile. Furthermore, CMake allows for the use of multiple 
`CMakeLists.txt` files to allow for better organization. Here is an example of 
_the simplest CMake project you can make_.

```
HelloWorld
|-- CMakeLists.txt
|-- Hello.cpp
|-- Hello.h
|-- RunHello.cpp
```

Imagine that `RunHello.cpp` uses `Hello.h` and `Hello.cpp` to print "Hello,
world!" to standard output. We have written the code necessary to do so, and
now we are ready to compile our program.

[cmake]:        http://cmake.org
[last-post]:    {{ site.baseurl }}{% post_url 2017-06-11-welcome-to-my-blog %}