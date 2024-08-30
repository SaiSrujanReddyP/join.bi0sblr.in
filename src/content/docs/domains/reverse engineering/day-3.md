---
title: "Day 3: Assembly, ABI and Syscalls"
description: "asdf"
---

### Assembly

Assembly is essentially a human-readable version of ISA instructions executed directly by the computer. Higher-level constructs like conditionals and loops are turned into lower-level primitives. Understanding how high level languages map to assembly is an important skill.

### ABI
The idea of function calls in a language like C is represented in assembly by a standard called the ABI or Application Binary Interface. It defines a contract between the caller and callee about the registers used to pass arguments, whether the stack is cleaned up by the caller and callee, and more.

### Syscalls

Normal usermode programs can do very little on their own - they cannot interact with other processes, do disk or network I/O, or anything else that would result in useful output. For all this, they must request the operating system kernel to do this operation for them using a mechanism called *syscalls*. This is similar to calling a function, with its own ABI, and a special instruction `syscall` (on x64) to trigger the syscall.

#### Theory

<details>
<summary>Assembly</summary>

> Objective: Understand the basics of x86 assembly
> > https://github.com/0xAX/asm
> > https://gpfault.net/posts/asm-tut-0.txt.html - more Windows focused article

</details>

<details>
<summary>ABI</summary>

> Objective: Become familiar with the System V ABI
> > Write a few C programs that call functions in https://godbolt.org/ and look at the register usage around the function call

</details>

<details>
<summary>Syscalls</summary>

> Objective: Understand the basics of syscalls
> > https://www.youtube.com/watch?v=JdVn3RMLU_Q
> > Syscall Table: https://x64.syscall.sh/

</details>

#### Practice

<details>
<summary>Assembly</summary>

> Objective: Attempt trivial assembly challenges
> > https://play.picoctf.org/practice/challenge/20
> > https://play.picoctf.org/practice/challenge/16
> > https://play.picoctf.org/practice/challenge/72

</details>

<details>
<summary>ABI</summary>

> Objective: Become familiar with the System V ABI
> > Write a few C programs that call functions in https://godbolt.org/ and look at the register usage around the function call

</details>

<details>
<summary>Syscalls</summary>

> Objective: Become familiar with the mechanics of syscalls
> > Try using simple Linux syscalls in C and assembly

</details>
