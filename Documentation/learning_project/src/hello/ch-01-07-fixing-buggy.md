# Fixing buggy_hello.c

So the code we've added to the kernel causes a kernel panic. Not Good! So let's fix it.

### Aims

* Understand how to use the gdb based `os161-gdb` debugging tool.
* Use `os161-gdb` to look at a crashing kernel.
* Run the kernel under `os161-gdb`, which is based on `gdb`

### Objectives

* Having used gdb, we find and fix `buggy_hello.c` and rename it to `complex_hello.c`
* Have configurations for development and testing compilations

### Revision

* gdb
* role of `~/os161/src/kern/conf/conf.kern`

Maybe you see the bug just by looking at the code. In that case, well done. In any case, debugging kernels in general is a tall order and an essential skill to actively devolop, so let's build our arsenel of awesome, and get some practice in.


As we go through the projects we are working on, there is the ever present cloud of bugs. With the help of debugging tools, we are well equiped to clear the skies. Debugging a kernel, however, presents an interesting problem, which OS/161 handles with `os161-gdb`. This is a tool that can connect to an instance of OS/161 running on top of sys161 as a seperate process. This allows us to connect to an OS/161 process when a crash is in progress.

## Connecting to a dying kernel

The os runs, but it crashes. As it's currently configured, though, OS/161 will halt during the crash, giving you an opportunity to see what happens. Let's do exactly that.

To open up a modified gdb that suites the needs of OS/161.
```cmd
cd ~/os161/root/
sys161-gdb kernel
```
 
Now, to make the debugger connection

``` gdb
(gdb) set can-use-hw-watchpoints 0 # Beyond scope.
(gdb) dir ~/os161/src/kern/compile/HELLO # [issue 9](https://github.com/Ben-PH/os161/issues/9)
(gdb) target remote unix:.sockets/gdb
```

and voila. You now have a gdb connected to an OS in the process of dying 
#### Useful tip
This chapters [appendix](./appendix.html) provides a way to do this with a single command.

## Doing a post-mortem on a crashed kernel

Now that we are connected, we can run a few commands to get an idea of what went wrong. 
* info locals   # i lo
* backtrace     # bt
* frame 1       # f 1

With this information, we can restart the kernel, and go through it line by line.

## Debugging a running kernel

First, we run the kernel as before, but with a key difference.
```cmd
sys161 -w kernel    # run sys161 -h for information on -w
```

in another terminal, connect to the running OS as before. At this point, os161-gdb is running much like any regular gdb.

Now you can use commands such as `break`, `continue`, `next`, `step`, etc. 

Use your debugging skills to find the issue! Complete this project by changing the file-name, make any needed changes to config files, reconfigure, build, and run your working kernel complete with `no_longer_buggy_hello.c`!
