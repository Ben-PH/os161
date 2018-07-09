# Wrapping up Project Hello

Let's look at our aims and objectives, and see if we are happy with our learning
outcomes. If you can answer these questions with a degree of confidence, this 
learning project has done well

## Aims
* Understand how to configure os161 for compilation and installation
    * If you wanted to change where your project was in your host machine,
    what changes do you think will need to be made if you moved it to `~/Documents/myos`?
* Be primed to learn how to use configuration as a tool in future projects.
    * If we were debugging our OS, and printing a variable gives `<optimized out>`,
    what changes would you think about making?
* Understand what controls the build and install of the OS.
    * If we wanted to make modifications to tools that are involved in controlling
    the build, which files would first look at?jj
We acquired the resources, built the os, ran it, changed it, extended it and fixed it.
This forms the core components of the skills that are involved in working on OS code.

* To be able to efficiently navigate our project using a selection of tools.
    * How would you find where `boot()` is defined in the kernel?
    * Can you click, or quick keyboard shortcut, to jump to a function definition?
    * If you needed to go to a kernel source-code file, where in the file tree might it be?
    * If you needed to go to userland source-code, where would you start looking?
* Use basic intro-level C skills to make changes to the code.
    * If you wanted to experiment with the order of initialisation calls (`boot()`,
    inside kernel `main.c` function, could you do it?) 
* Understand what needs to be done to make these changes take effect.
    * What are the steps to build, run, and debug a compilation?

* To understand how to include additional source-code files into the kernel
as part of a successfull build.
    * How do you add another file to the system, and configure the build to include it?
* To understand where to select and call a function defined in another file.
    * Are there 
* To use TAGS to efficiently move around the project source-code.
    * How do you go to a function definition with a mouse click or keyboard shortcut?
    * When the source code changes, what database needs to be updated to use TAGS properly?
* To use os161-gdb to debug our kernel.
    * How can we connect gdb to a running kernel?
    * How do you determine the function calls made to get to a current break?
    * What gdb command do you use to move to an earlier function call?
    * What steps do we take to debug a running os161 in a way that is similar to non-kernel development?
