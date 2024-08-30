---
title: "Day 4: Static Analysis"
description: "Inspect binaries"
---

### Static Analysis

Static analysis is the act of examining a program without actually running it. A lot of preliminary information can be gleaned through this (in the real world, without risk of accidentally 'detonating' malware). The standard free tool for this is [Ghidra](https://ghidra-sre.org/) - it lets us *disassemble* machine code to assembly, and *decompile* this to human readable *pseudocode*. This is pseudocode for a reason - the program is just guessing what the code could look like, and it won't be 100% accurate, but it should take you quite far.