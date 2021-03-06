# Configure the Setup

An OS is a large and seemingly unweildy piece of kit. Let's fix that perception and learn how to controll the build configuration.

## Aims
By the end of this, you will:

* Understand how to configure os161 for compilation and installation
* Be primed to learn how to use configuration as a tool in future projects.

## Objectives
* Understand what controls the build and install of the OS.
* Have a config file with minor changes tailored to your dev systems.
* Be set up to run the terminal commands that will install your first os161

## Known Issues
* Dependencies missing if using Ubuntu later than v14
* Some automatic processes not yet complete.

```text
This book assumes your project is run in the default $(HOME)/os161/
This page will show you how to change this default.
From here, $(HOME)/os161 will be refered to as $(TOP)
```

## The kernel config scripts and files

The two main files of interest are $(TOP)/src/configure and $(TOP)/src/kern/conf/config

#### $(TOP)/src/configure
Looking at this file, we will get a familiarity of the more fundamental settings for the compiler, and be able to make some changes to suit our needs. 

* OSTREE. When we build our OS, we need to build the directory tree of said OS (as in the running system, not the source code).  By default, it is `$(TOP)/root`. If you want this default to be, `~/Documents/os_proj/` instead of `~/os161/`, you will have to change  OSTREE accordingly.
* run this script with `./configure`
* note the other variables, at this stage, little more than a curiosity:
  * PLATFORM - related to the toolchain.
  * MACHINE - Would need to change if implimenting for other architecture.
  * DEBUG - will become handy later on, when we start developing.

#### $(TOP)/src/kern/conf/config and $(TOP)/src/kern/conf/HELLO
Earlier projects exclusively touch code found below `$(TOP)/src/kern/`. Looking in the `kern` sub-directory will allow us to understand how to have some power over the kernel build. `kern/conf/config` and `kern/conf/HELLO` are best looked at together.

We can see in `$(TOP)/src/kern/conf/config` that we have ` # recognised directives`. `HELLO` alread has `debug` selected, and a series of devices. If you want to take an early look at how  the compiler puts things together, this is a good file to look at. Note how we `include conf/conf.kern`. We will look at that when we start adding more files.
