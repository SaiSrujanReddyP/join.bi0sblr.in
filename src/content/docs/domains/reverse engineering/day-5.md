---
title: "Day 5: Dynamic Analysis"
description: "GDB Intro"
---

### What is Dynamic Analysis?

Dynamic analysis is the process of running a program to observe and analyze its behavior in real-time.
Tools like debuggers are used to facilitate this analysis by allowing the inspection of variables, memory, and system interactions and help identify vulnerabilities that static analysis alone may miss. 
Some issues in our program may not be apparent when analysed statically. That's where this comes into picture.

### How is it Useful in Reversing?

Let's say you have a binary, you wish to see what exactly happens inside it as it is running, you can't do all of it through static analysis, because for large programs you'll need to manually note the values passed into the system registers and the program flow.
So using debuggers is crucial to understand the impact of a part of your programs' code. Especially when some information is obfuscated and you need to extract some sensitive information. (maybe even a flag? ^-^)

So you can pretty much guess that it's used in malware analysis, bypassing protections and even modifying code behaviour.

Now that you understand this, get steppin'! :D

#### Theory

<details>
<summary>GDB Basics</summary>

> Objective: Learn how to use basic GDB commands.

> > GDB Tutorial: [Read Here](https://www.geeksforgeeks.org/gdb-step-by-step-introduction/)

GDB allows you to set breakpoints, watch variables, step through code line-by-line, and inspect the state of your program. Understanding these basics is the first step in debugging and analyzing binaries.

</details>

#### Practice This

<details>
<summary>Hands-On Exercise</summary>

> > **Install GDB:** Install GDB, ofc.
> > **Debug a simple program:** Use GDB to step through a simple C program and examine its assembly code. Practice setting breakpoints, stepping through instructions, and examining register values.
> > **Disassemble Functions:** Use GDB to disassemble functions in a binary and analyze their assembly instructions. Identify function prologues, epilogues, and control flow.
</details>

