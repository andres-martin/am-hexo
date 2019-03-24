---
title: The difference between a hard link and a symbolic link .
date: 2019-03-24 11:21:48
author: Andres
tags: [C]
---

{% img [class names] https://cdn-images-1.medium.com/max/800/1*UWqVL3t6rCJ4tjFNvlQpzA.png [width] [height] [title text [alt text]] %}


A symbolic link is a term used for any file that holds a reference to another file or directory in the form of an absolute or relative path , any changes made through the symbolic will affect the original file, however if the symlink is deleted the original file still remain.

Hard links may take less disk space as they only take up a directory entry, and they share the same inode as the original file,whereas a symlink needs its own inode to store the name it points to.

If a Hard link is deleted it may delete the file as well, if there aren’t other hard links pointing to that file.

Here is an example of how to create symlinks and hard links:

First create a file:

$ echo 'Hello, World!' > myfile.txt

Create a hard link hard-link to the file myfile.txt, which means "create a file that points to the same inode that myfile.txt is pointing to, use the ln command:

$ ln myfile.txt hard-link

Creating a soft link soft-link to the file myfile.txt, which in other words means create a file that points to the filemyfile.txt to achieve this you need to use ln -s command:

$ ln -s myfile.txt my-soft-link

Look what will happen now if myfile.txt is deleted or moved: hard-link still points to the same file and subsequently unaffected, whereas soft-link now points to nothing.


source venngage.com
I hope you have learned how Hard links and symbolic links work, and how to create them.