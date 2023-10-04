# CS0449 Exam I Study Guide

> **Prepared by [Shinwoo Kim](https://sites.pitt.edu/~shk148/)**

Below is a **non-exhaustive** list of topics that _may_ appear on the first exam. Note that topics not on this document may show up on the exam if it was discussed in lecture, recitation, or in an assignment. Conversely, the topics on this list are not guaranteed to be on the exam! This document purely serves to motivate students who "_do not even know where to begin_."

## Overview

Studying for an exam is about gaining a level of familiarity with the material such that you can solve interesting problems that aren't just repetitions of things you've already seen. Some general tips:

- Start early and spread things out over time. Sleep does some sort of magic where things sink in better. More shorter study days is way preferably to a few short ones. One of the reasons we have assignments with deadlines is to exploit this fact.
- Be as active in your studying as possible. Working through problems and developing cheat sheets are "active". Simply rewatching lectures and rereading something you've read is not.
- The often missing component: Reflect on your own problem-solving process. This is much easier through discussion with others, particularly other students.

**Useful Excercises (PDFs)**

- [Data Tutorial](./data-tutorial.pdf)
  - [Solutions](./data-tutorial-sol.pdf)
- [C Tutorial](./c-tutorial.pdf)
  - [Solutions](./c-tutorial-sol.pdf)
- [Memory Tutorial](./tutorial-malloc.pdf)
  - [Solutions](./tutorial-malloc-solutions.pdf)
- [x86 Tutorial](./x86-homework.pdf)
  - [Solutions](./x86-homework-solutions.pdf)

## Data Representation

The first few weeks of the semester focused on how computers store and manipulate data. This may have been a review
for some of you (especially if you’ve already taken CS 0447[^447]), or it may have been new material. Either way, you are
expected to know the following:

- Basics of **Binary Representation**
  - The difference between Base-2, Base-10, Base-16, and how to convert between each of them.
- Different ways that a computer represents data
  - The difference between signed and unsigned numbers
  - Two's complement and how to convert to decimal (and vice versa)
  - Types of integers and their quirks (including the effects of explicit/implicit casting)
  - Floating point numbers in C (including the effects of casting)

## C Programming

The main programming lanuage of choice for this course is C. C is particularly useful in studying systems because it "_provides a nice abstract syntax (of a high-level programming language) while maintaining the direct access to memory (like assembly)_." For the purposes of the exam, you should be familiar with:

- Characteristics of C
  - What does it mean to be a compiled language?
  - How does C differ from languages such as Java or Python?
  - How does C allow us to directly control memory?
  - What is the C preprocessor?
- C programming (including reading and writing C code) - C syntax for functions, variables, operators, control flow, etc. - Scope and lifetime of variables
- Bitwise operations in C - AND, OR, XOR, Shifting (Logical/Arithmetic) - Bitwise operation vs Boolean operations - Extracting fields with shifting and masking
- Boolean operations in C - Boolean as integers
- Structs
  - What are they used for, and how we can create one
  - What is `typedef`?
  - What is `sizeof()`?

## C Memory Model

A major focus of this course is on how memory works. Mainly, we look at different ways of managing memory (static vs dynamic), and peek inside some of the abstractions provided by the operating system. Studying memory is crucial as all the code you write is fetched from memory!

For the exam, you should know that:

- Memory is a continuous series of bits
- The C Memory Model
  - The sections such as the stack, heap, static data, code
  - What each section is for. Given a peice of code, can you identify where that variable/code lives?
- Addressable Memory
  - What it means by "Byte-addressable"
  - Direct memory access through pointers
- Arrays and Pointers
  - What is an array? What's a pointer?
  - How they are the same, and how they are different?
  - Pointer arithmetic vs normal arithmetic
- C Strings - What is a string literal? - How are strings and arrays similar? How are they different - `sizeof()` vs `strlen()` - What are some common string functions? - Null-terminator `\0`

## Input/Output in C

- How to read from and write to the terminal (`printf()`, `scanf()`)
- How to read from command line arguments
- How to read from and write to files
  - Common file functions: `fopen()`, `fseek()`, `fwrite()`, `fread()`, `fclose()`
- How are files and pointers similar (parallels between disk and memory)?

## Memory Management

- What is dynamic memory allocation?
  - What do we mean by "dynamic"?
  - When should we use it? When should we not?
  - How do we use it? (Hint: `malloc()`)
- What is the heap?
  - How does `malloc()` work under the hood?
  - Implementation details of malloc (including how Linked Lists work)
  - Various search mechanisms for `malloc()` and their pros/cons.
  - Ways to optimize `malloc()`
  - Tracing through `malloc()` given a memory diagram

## Assembly Programming

- What is assembly?
- How is x86-64 different from MIPS?
  - CISC vs RISC
- x86 basic syntax
  - Can you read & interpret x86 code?
  - Translating C to assembly (and vice versa)
- The C ABI
  - Registers in x86 and what each one is for

**Remember: Anything discussed in lecture/recitation/assignment is fair game for the exam!**

[^447]: Computer Organization and Assembly
