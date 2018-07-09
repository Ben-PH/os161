# Introduction

Welcome to this os161 Learning Project, where we work on practical skills, and theoretical understandings for OS engineering. We this piece by piece with sub-projects, such as concurrancy, system calls, and virtual memory. Each subproject will give you hands-on activities, and will be accompanied by the relevant thoery TODO: write thoery for hello.

## Project Background

After an early exit from my university OS course (because: reasons), I resolved to return for next course enrollment. For me, teaching is not just a hobby, but my preferred study method, because you must set yourself a path of commitment, integrity and self-study of the highest standard in to do so, and writing these is an important part of that. By developing this material, I don't only have a lot of fun and learn across a broad scope, I get to demonstrate my work, build my own skills, and prepare for the next enrollment for maximum learning value.

This Learning Project was inspired by, and is drawn heavily from, UNSW's [COMP3231 "Operating Systems"](http://www.handbook.unsw.edu.au/undergraduate/courses/2017/COMP3231.html) course. This courses practical component uses [OS/161](http://os161.eecs.harvard.edu/), alongside in depth theory. COMP3231 is a pre-requisite for[COMP9242](http://www.handbook.unsw.edu.au/undergraduate/courses/2017/COMP9242.html), and has close ties with [the seL4 project](https://sel4.systems/). Opinion: This relationship between COMP3231 and seL4 makes for an interesting pathway between instructional OS engineering and OS engineering at the highest level.

### Project Aim

The overall aim of this Learning Project, is that through practical and theoretical application, you will:

* Be comfortable navigating and working with large, complex code-bases.
* Be comfortable developing in a fault-**in**tollerant setting.
* Gain profficiency in practical OS development, and its underlying theory.
* Develop Software Engineering skills, disciplines and understandings that are universally applicable.

This is very general, and you will pick up more specific things as we go. Every part of this book serves as an aid to these aims.

### Project Approach

The overall Learning Project consists of smaller Projects organised by chapters in this book. Project source-code is organised using git branches with equivilent names (with the exception of ch-1 Hello, which is on master). Aims and Objectives are used throughout. **Aims** are subjective, and self-assesed. Questions related to these aims are provided as a guide to help you determine how effectively you have learnt. **Objectives** outline at the beginning of a Project or section what will be produced. It is up to you to self-asses the quality of what you produce, however guidelines will be provided where possible.

### Logistics to get started

You will need to have the following installed on your machine:

* git
* gcc
* gdb
* Ubuntu desktop version 14 - either native or running as a virtual machine. (TODO: refine this so can use later/other dists)

The Learning Project starts of relatively straight forward and assumes little at the start, but rapidly ramps up. Having the following is important to an enjoyable project
* Comfortable with C or similar language, especially pointers, multi-file development, and particularly memory management. 
* Familiarity with function pointers and macros in C.
* Comfortable using gdb, or similar debugging system.
* Familiarity with git, and comfortable with its basic usage.
* Awareness of what assembly language is.

Resources that can help you are widely available. Here are some recommended resources
* [Basic git](learngitbranching.js.org).
* [Intermediate C and gdb](https://www.edx.org/course/cs50s-introduction-computer-science-harvardx-cs50x)

Finally, having a good development environment is important on such a large code-base. This is a personal choice, but options that can work well include
* Emacs - with the following package list as an example. Alternatively, spacemacs for an "out of the box" configuration.
  * flycheck - for on-the-go error checking
  * projectile - for project navigation
  * neotree - for file-tree visualisation
  * undo-tree - for undo/redo management.
  * magit - for git management
  * evil - for Vim emulation
  * a gdb configuration - for in-window debugging

* Vim - A phenominally powerful text editor, you will want plugins for a good setup. Suggestions include:
  * cscope - project navigation
  * nerd-tree - file-tree visualisation
  * TODO: Add more

There are IDEs that work well "out of the box", if configuration and customisation is not your thing. Examples include:
* VS Code
* Atom
* Sublime

Whatever your development environment is, key features to include/setup are
* Suites your style
* real-time error checking
* navigation by TAGS, or similar method
* Good file-structure visualisation
* Support for powerfull gdb use
  * Note: Instead of `gdb [options] ./executable` to debug, we do things differently as outlined in the Hello Learning Project. So long as your dev environment can use `os161-gdb` plus cli arguments for its gdb call, it's all good.
