# Extending and debugging your OS

Now that we can make changes to existing source-code, let's extend the code-base.

As you've probably noticed, buiding OS/161, and OS's in general, is a much more convoluted process compared to the typical build. It might not be a surprise that this follows for many OS development tasks, such as debugging. Once we cover this page, we will have enough to go by for most of the Learning Projects in this book.

## Aim

* To understand how to include additional source-code files into the kernel as part of a successfull build.
* To practice selecting where to put a function call in a large code-base.
* To use TAGS to efficiently move around the project source-code.
* To use os161-gdb to debug our kernel.

## Objectives

When this part of the project has been completed, you will have made changes so that
* The kernel has access to `complex_hello()`, which is successfully called and run.
* Your development environment is set up to jump around the code-base using TAGS.
* `complex_hello()` is in a different file to where it is called.
* We can run the kernel with a call to `complex_hello()`, but it crashes (debug is after)

## Revision
* Multi-file C programs
* The role of src/kern/conf/conf.kern in the build process[^1]

## buggy_hello.c

At this stage, we are adding files to our kernel. Inside this file is the code that runs `complex_hello()`, which itself calls helper functions, which is provided. All it does is print a "hello world" message.

Start by choosing where to put the `complex_hello()` function call. Place it so the line is printed just above the prompt.

#### Adding buggy_hello.c to the build

Although you are provided the code in this projects [appendix](./appendix.html), it is your job to select where to put the file. This is up to you, but be smart about it. It makes sense to put it somewhere in `$(TOP)/src/kern/` or one of it's sub-directories, but where it goes is up to you.

```text
Just like source-code style, there are differences in opinion on project layout style,
but some opinions are more valid than others. As you take on more learning projects, 
you will develope your own style of how to layout the OS. Play around and experiment
with what style works for you
```

At this point, by trial and error, work on how to configure your build so that the compile and install is successful. 

Once you've managed to compile the program successfully, run it, and it shall crash...

#### Turning buggy\_hello.c into complex_hello.c

So you have extended the OS, but the extension causes a crash. This is a common thing, so let's learn how to fix that.

[^1]: You might be interested in also looking into what `bmake depend` does 
