# First Install of os161

Excited to get os161 working? Let's do it!

This takes three main steps

* Run the configuration script for the overall project.
* Do the same for the kernel.
* Building and installing the kernel code.
* Do the same for user code.

## Configure the project

We want to make sure that our project sits in our system how we want it. This is done for us by the `/src/config` script, all we need to do is run the script. 
```cmd
cd ~/os161/src
./configure
```
Remember how in [Configure the Setup](ch-01-02-configure-setup.md), how we had a default project location? That comes into play here.

#### Quick Theory
TODO: Link to theory going into "there is user space, and there is kernel space". E.g. 

An OS seperates "user space" and "kernel space" (link) goes into more detail. We have just configured "the glue" between the two spaces, but now we need to look at each space indipendently.

## Configure, build and install the kernel

As we go through more learning projects, we will cover this in more detail. For now, we just want to get up and running.

#### configure

Again, our tool of choice is going to be a configure script;  `~/os161/src/kern/conf/config`
instead of `~/os161/src/config` as before. Also, this config needs to be run with a config file
that controlls the script. In this case, we will use `~/os161/src/kern/conf/HELLO`
```cmd
cd ~/os161/src/kern/conf
./config HELLO
```

#### Build and install

Now that we have the config generated, we can create the binaries, and put them
where they need to be. First, we need to move to the directory where kernel
build is managed
* `cd ~/os161/src/kern/compile/HELLO/` (or `../compile/HELLO`)
* `bmake depend` - TODO: what does depend do?
* `bmake` - compiles the binaries
* `bmake install` - puts files and symbolic links in the right place


### User

We need to do the same user-level utilities. This one is straight forward:
* `cd ~/os161/src && bmake`

And there you have it. An operating system ready to go! Now let's run it...



