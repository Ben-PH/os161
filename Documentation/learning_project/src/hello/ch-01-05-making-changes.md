# Making changes

Having run our first build of OS/161, let's get into putting our own touch into the system. From here, we will

* Make changes to existing code.
* Add code by adding files, and changing configuration to reconize these files.
* Fix bugs in changes that have been made.

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
* building OS/161 - [Build and install](./hello/ch-01-03-first-install.html)

## Finding the code

Given the size of OS's, navigating the code base to where you need to be is a crucial skill. OS/161 is short for an OS, in the order of 7000 lines of code and well layed-out. This makes it an ideal place to build this skill.

#### Quick Theory
```text
At around 7000 lines of code, OS/161 is very small for a unix/linux based OS. 
Linux has [passed 20m lines](https://www.linuxcounter.net/statistics/kernel) 
of code. Literaly orders of magnitude larger.
```

There are some great tools available to us. For now we will just use...

### grep
"**g**lobal **r**egular **e**xpresion, **p**rint". Use of this tool is a foundational skill to linux usage, so there are plenty of intros elsewhere. For this exercise it's sufficient to know the basics. 

We are working inside kernel code. Make sure you are familiar enough with the `~/os161/` file tree to recognise where we should start our search. Once there, do a grep search through the source-code, and find a line of code that prints something you want to change. Make the changes, and save.

### Seeing the changes take place.

At this point, you should be thinking back to when you built the OS/161 for the first time. If you're unsure how to build and install, go back to [our first build](ch-01-03-first-install) and play around with what you do/don't need to do.

Now run it again! If things went well, you should see something like this:

```text
sys161: System/161 release 2.0.8, compiled Feb 19 2017 14:31:53

OS/161 base system version 2.0.3
(with locks&CVs solution)
Copyright (c) 2000, 2001-2005, 2008-2011, 2013, 2014
   President and Fellows of Harvard College.  All rights reserved.

THIS ISN'T EVEN MY FINAL FORM! (HELLO #2)

1892k physical memory available
Device probe...
lamebus0 (system main bus)
emu0 at lamebus0
ltrace0 at lamebus0
ltimer0 at lamebus0
beep0 at ltimer0
rtclock0 at ltimer0
lrandom0 at lamebus0
random0 at lrandom0
lser0 at lamebus0
con0 at lser0

cpu0: MIPS/161 (System/161 2.x) features 0x0
OS/161 kernel [? for menu]: 
```

Notice how the build number changes? This gives you valuable info during the build. Have a look at the other pieces of info. Maybe this is a moment you'd like to go down a rabbit hole, and understand how this info is generated and handled in the system.

Now that we know how to change existing code, let's look at how we can add more code...
