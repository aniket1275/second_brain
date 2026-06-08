---
title: Why Buffers are used
draft: false
tags:
  - SystemProgramming
---
## Why buffering is necessary

### 1. You can’t process what you don’t store

CPU works on memory (RAM).
Even if data comes from:

- disk
- network
- pipe
- file

It must land in RAM first.
That RAM region = buffer.
### 2. Hardware & OS don’t give data instantly

When you read from:

- a file 
- a socket 
- stdin 

You’re dealing with external or kernel-managed resources.
Data comes:
in chunks
at unpredictable times (especially sockets)

So the OS says:
“I’ll give you some bytes—store them somewhere.”
That “somewhere” = buffer.

### 3. System calls are expensive

Every read() in C or read() in Rust:

- switches from user mode → kernel mode
- costs CPU time
If you read 1 byte at a time, it’s horribly slow.

So instead:
- read 1000 bytes into a buffer
- process them in your program
Buffer = performance optimization.

### 4. Streams don’t have boundaries

A stream is just:
“continuous flow of bytes”

Example:
- TCP socket doesn’t say “this is one message”
- It just gives raw bytes

So buffer helps you:
- collect chunks
- assemble meaningful data
