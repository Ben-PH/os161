# Making changes

Having run our first build of os161, let's get into putting our own touch into the system. This 

* Make changes to existing code.
* Add code by adding files, and changing configuration to reconize these files.
* Fix bugs in changes that have been made.

## Our first changes

We will start off with something simple. Let's change a print statement.

## Aims

* To be able to efficiently navigate our project using a selection of tools.
* Use basic intro-level C skills to make changes to the code.
* Understand what needs to be done to make these changes take effect.


## Objectives

* Instead of the default message at startup, it prints what *you* think it should print.
* Your devolopment environment has the tools to navigate and search the code efficiently.

## Revision

* grep - [A usefull learning resource](https://www.linode.com/docs/tools-reference/tools/how-to-grep-for-text-in-files/)
* printf - `man 3 printf`
* building os161 - [Build and install](./hello/ch-01-03-first-install.html)

## Finding the code

Given the size of OS's, navigating the code base to where you need to be is a crucial skill. os161 is short, in the order of 7000 lines of code and well layed-out. This makes it an ideal place to build this skill.

#### Quick Theory
```text
At around 7000 lines of code, os161 is very small for a unix/linux based OS. 
Linux has [passed 20m lines](https://www.linuxcounter.net/statistics/kernel) 
of code. Literaly orders of magnitude larger.
```

There are some great tools available to us. For now we will just use...

### grep
"**g**lobal **r**egular **e**xpresion, **p**rint". This approach is a foundational skill to linux usage, so there are plenty of intros elsewhere. For this exercise it's sufficient to know the basics. 

We are working inside kernel code. Make sure you are familiar enough with the `~/os161/` file tree to recognise where we should start our search. Once there, do a grep search through the source-code, and find a line of code that prints something you want to change. Make the changes, and save.

### Seeing the changes take place.

At this point, you should be thinking back to when you built the os161 for the first time. If you're unsure how to build and install, go back to [our first build](ch-01-03-first-install) and play around with what you do/don't need to do.

Now run it again! If things went well, you should see something like this:

```text
TODO: put in output of example change
```

Notice how the build number changes? This gives you valuable info during the build. Have a look at the other pieces of info. Maybe this is a moment you'd like to go down a rabbit hole, and understand how this info is [generated and handled](TODO) in the system. TODO: find and change GROUP_VERSION as appropriate. 

Now that we know how to change existing code, let's look at how we can add more code...
