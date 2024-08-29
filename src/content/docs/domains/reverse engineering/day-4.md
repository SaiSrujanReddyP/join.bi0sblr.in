---
title: "Day 4: Obfuscation and Solvers"
description: "encryption and solving"
---

### Obfuscation

After going through source code or decompiler output, you will usually encounter some basic encryption. To solve such encryptions (like Xor and Bit manipulation) you must understand what's happening in the code.

#### Bitwise Operations

These are just logical operations like AND, OR and NOT being done on the individual bits of the input.

#### Xor

XOR (Exclusive OR) is a fundamental technique used in various cryptographic and obfuscation algorithms. It operates on binary data - such that if the bits in both inputs are different, the output is 1, else 0. The basic idea of reversing an Xor operation is exploiting its reversible nature - like if `a ^ b = c`, then `a ^ c = b`.

#### Bit Shifting

The bits of a number can be shifted either to the left or right within its fixed size. The bits that go beyond the end are truncated, and the void created before the shifted part is filled with zeros.

Consider a number 49 or 0b110001 stored in a single byte.

```
0b00110001 << 1 = 0b01100010
0b00110001 << 2 = 0b11000100
0b00110001 << 3 = 0b10001000
0b00110001 << 4 = 0b00010000

0b00110001 >> 1 = 0b00011000
0b00110001 >> 2 = 0b00001100
0b00110001 >> 3 = 0b00000110
0b00110001 >> 4 = 0b00000011
```

*Bit rotation* is a similar operation, where the bits that go beyond the end instead wrap around to the other side, and no zeros are added.

#### Solvers

Sometimes the operations done on the data we're trying to extract are *destructive* and non-reversible. Other times, we have a huge set of conditions to satisfy that would be impossible to reverse by hand. This is where *solvers* come in.

Satisfiability Modulo Theories (SMT) solvers are powerful tools used in reverse engineering and formal verification to determine the satisfiability of logical formulas under certain constraints. These can be used to solve the [np-hard](https://en.wikipedia.org/wiki/P_versus_NP_problem) problem of finding the possible initial states of a system of variables that will lead to a final state that satisfies the constraints we provide - like the input characters needed to satisfy all the checks in a password-checking algorithm. This lets us treat the constraints like a 'black box' to some extent, allowing us to just map inputs to outputs.

:::note
This forms a potent combination with binary analysis and symbolic execution to solve for states in the binary itself, with [angr](https://angr.io). Avoid concerning yourself with this for now!
:::

#### Theory
<details>
<summary>Xor</summary>

> Objective: Learn the basics of xor operation, look into the fundamentals of how it works on bit level

</details>

<details>
<summary>Bit manipulation</summary>

> Objective: Learn the basics of bit operations like bitwise and, bitwise or, left shift, right shift and so on.

</details>


<details>
<summary>Z3 Solver</summary>

> Objective: Understand the syntax of Z3 and solve some easy challenges
> > https://irregular-25.vercel.app/posts/understanding-z3/
> > https://github.com/Joy2225/Rev_Treasure/tree/main/Z3/challanges -Some sample challenges and their solution
</details>

#### Practice

<details>
<summary>Xor</summary>

> Objective: Just get me the flag here, format: bi0sblr{}
```
if enc_flag == 'hc:yhfxqlka9Ulf>Mw':
    print("Accepted :)")
else:
    print("Rejected :(")
```
> > Note: Every character of the flag is xored with the same number


</details>