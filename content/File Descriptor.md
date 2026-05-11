---
title: File Descriptor
draft: false
tags:
  - SystemProgramming
---
# File Descriptor

It is just a positive number given by the operating system to a process for allocate the number to resources are in use ( or opened by process ) by the process.

### Analogy for this

"After ordering the food in the restaurant we get a token descriptor is same token".

file = actual resource process needs to access
file descriptor = number for resources opened by process.

Every program get these resources by default so that it has fix number.
And the resources are :

- Stdin (keyboard) = 0
- Stdout ( screen ) = 1
- Stderr ( screen ) = 2

### why does it exists

To abstract everything as file.
Like in linux everything is file socket, devices, pipes, etc.

So I can just use the number to read and write using the system call.
Ex: 
read(fd, buffer, size);  
write(fd, buffer, size);  
close(fd);

## Where the FD lives

For every process there is and fd table which store it.
Like:
 process FD Table  
----------------  
0 → stdin  
1 → stdout  
2 → stderr  
3 → file.txt  
4 → socket  
5 → pipe

## what does it actually points to

FD (user space)
   ↓
File Descriptor Table (per process)
   ↓
Open File Table (kernel)
   ↓
Inode / actual file
