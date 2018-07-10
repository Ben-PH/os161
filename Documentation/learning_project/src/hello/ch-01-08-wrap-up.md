# Wrapping up Project Hello

Let's look at our aims and objectives, and see if we are happy with our learning
outcomes. If you can answer these questions with a degree of confidence, this 
learning project has done well

## Aims
* Understand how to configure os161 for compilation and installation
    * If you wanted to change where your project was in your host machine,
    what changes do you think will need to be made if you moved it to, for example, `~/Documents/myos`?
* Be primed to learn how to use configuration as a tool in future projects.
    * If we were debugging our OS, and printing a variable gives `<optimized out>`,
    where would you start looking to make changes?
* Understand what controls the build and install of the OS.
    * If we wanted to go about exercising controll over the build process, which files would first look at?
* To be able to efficiently navigate our project using a selection of tools.
    * How would you find where `boot()` is defined in the kernel?
    * Is your environment set up so you can to jump to a function definition with a click, or keyboard a short keyboard command?
    * If you needed to go to a kernel source-code file, which section of the file tree would it be?
    * Suppose someone told you to find a file. "I don't know where it is, but it's got something to do with the mips architecture"
    * If you needed to go to userland source-code, where would you start looking?
* Use basic intro-level C skills to make changes to the code.
    * Consider `$(TOP)/src/kern/arch/mips/syscall.c:syscall()`. Add code for the SYS_sync case in a way consistent with the other cases.
      * Extra: use SYS_reboot as an example, impliment code for the SYS_sync case, which ultimately panics with the message "sync syscall not implimented"
* Understand what needs to be done to make these changes take effect.
    * What are the steps to build, run, and debug a compilation?

* To understand how to include additional source-code files into the kernel
as part of a successfull build.
    * How do you add another file to the system, and configure the build to include it?
* To practice selecting where to put a function call in a large code-base.
    * With the use of os161-gdb, how would you research where to place a kprintf() call so it's immediately before the function of a command is called?
* To use TAGS to efficiently move around the project source-code.
    * Use your development environment to *rapidly* traverse the code as follows:
      * the definition of the function that is called under `SYS___time`->the definition of the first function called in here->the definition of the struct in that function. It should have a name analagous to "development information"
* To use os161-gdb to debug our kernel.
    * How can we inspect the kernels state when it crashed?
    * How do you determine the function calls made to get to a current break?
    * What gdb command do you use to move to an earlier function call?
    * What steps do we take to debug a running os161 in a way that is similar to non-kernel development?
