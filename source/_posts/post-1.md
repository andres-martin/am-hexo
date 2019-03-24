---
title: Explaining what happens when you type ls *.c in your Shell.
date: 2019-03-23 21:34:07
author: Andres
tags: [C]
---

{% img [class names] https://cdn-images-1.medium.com/max/800/1*5RZ6Hzu1ScVI23vnni5yKg.jpeg [width] [height] [title text [alt text]] %}

When you are working in your terminal most of the times you will want to find certain files ending with a given extension.
Let's say you have been coding some C-type files, these files have an extension ending with .c , for example you were coding some C/C++ project and you created a file named "coderun", then you will likely to run your code. For your computer to be able to run and interpret your code inside it, it's imperative that you add an extension at the end of the file that tells your computer what kind of contents your file has inside it, in this case at the end of your file named "coderun" you will need to add .c "coderun.c".
Now If you are working with the shell, there is an useful command called ls, this command allows you to list all contents (including files and directories) inside your current working directory.
In our case that we were working with C-type files you are most likely to list only files ending with a .c extension, to achieve this ls has some useful options that enables us to list files ending with a certain parameter, the syntax for listing only files ending with .c it's as follows ls *.c , the * indicates all files, but in order to be more specific with our listing after the * you will need to add a pattern that tells the terminal how to display our listing, in our example we add .c after the * symbol , this indicates that all files ending with .c should be listed ls *.c.
As you see this let us refine our listing in our terminal!
I hope this article has helped you to understand the multiple uses of ls * .