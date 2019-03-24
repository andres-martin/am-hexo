---
title: C Static Libraries
author: Andres
date: 2019-03-24 11:28:21
tags:
---
{% img [class names] https://cdn-images-1.medium.com/max/800/1*MMmlzztUmGro_ij6RBYMDg.jpeg  [width] [height] [title text [libraries]] %}

Inbuilt functions are sometimes grouped together and placed in a file called library, that’s the definition of a C library.

Why should you use libraries in C?

Static libraries are useful when it comes to maximizing your productivity, and allows the user to get access to a bunch of functions that gets pre-defined output instead of writing your own code.

How do libraries work?

All C libraries are declared in the header of a file, a library is saved as libame.h , then this file should be included at the beginning of your C program like this #include <libname.h> this allows us to get access to the functions inside the library.

How to create a static library in C?

Before getting started you should compile all your .c files into object files, you can use the following command:

gcc -c *.c

The basic command to create a static library in C is ar which stands for “archiver”, In order to create a static library we can use the command like this:

ar rc libname.a file1.o file2.o file3.o

This program creates a static library named libname.a and includes copies of files ending in .o which are object files. If the library file already exists, it is replaced, if they are newer than those inside the library.

The c flag tells ar to create the library if it doesn’t exist. The r flag tells it to replace older object files in the library, with new ones.

Next, the library should be indexed using the command randlib as follows:

randlib libname.h

randlib is also used to re-generate the index.

How to use Static Libraries?

After the library is created, eventually we will want to use it, to do this we need to add the library’s name to the list of object files given to the linker. Using a special flag like -l, here is an example:

cc main.o -L -lname -o prog

Note the usage of the -L flag, this flag tells the linker that libraries might be found in the current directory.