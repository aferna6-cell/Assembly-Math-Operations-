# Assembly Math Operations

A collection of mathematical functions implemented in x86 assembly language, demonstrating low-level programming concepts and computer architecture fundamentals.

## Overview

This project implements three core mathematical operations in 32-bit x86 assembly:
- **Difference calculation**: `diff = digit1² + digit2² - digit3²`
- **Sum and product calculation**: Computing sum and product of three digits
- **Remainder calculation**: `remainder = product % sum`

## Functions

### `dodiff`
Calculates the difference using the formula: `(digit1 * digit1) + (digit2 * digit2) - (digit3 * digit3)`
- Uses `imull` for multiplication operations
- Demonstrates arithmetic instruction chaining

### `dosumprod` 
Computes both sum and product of three input digits:
- **Sum**: `digit1 + digit2 + digit3`
- **Product**: `digit1 * digit2 * digit3`
- Shows efficient register usage for multiple calculations

### `doremainder`
Calculates the remainder of product divided by sum using integer division:
- Uses `cdq` for proper sign extension
- Demonstrates `idivl` instruction for division with remainder

## Technical Features

- **Proper function structure**: Standard prolog/epilog with stack management
- **Register preservation**: Saves and restores `%ebx` register
- **Global variable handling**: Uses `.comm` directives for variable declaration
- **Memory operations**: Efficient load/store operations with global variables
- **Error handling**: Proper setup for signed division operations

## File Structure

```
├── Fernandes_2730_001_02.s    # Main assembly source file
└── README.md                   # This file
```

## Usage

This code is designed to be assembled and linked with a C program or testing framework. The functions operate on global variables:

**Input variables**: `digit1`, `digit2`, `digit3`  
**Output variables**: `diff`, `sum`, `product`, `remainder`

## Assembly and Linking

```bash
# Assemble the code
as -32 Fernandes_2730_001_02.s -o math_ops.o

# Link with your C program (example)
gcc -m32 main.c math_ops.o -o math_program
```

## Learning Objectives

This project demonstrates understanding of:
- x86 assembly language syntax and structure
- CPU register management and calling conventions
- Memory addressing and global variable manipulation
- Integer arithmetic operations at the machine level
- Stack frame management for function calls

## Course Context

Developed as part of ECE 2730 (Computer Engineering) coursework, focusing on:
- Low-level programming concepts
- Computer architecture fundamentals  
- Assembly language programming techniques
- Hardware-software interface understanding

## Skills Demonstrated

- **Systems Programming**: Understanding of how high-level operations translate to machine code
- **Performance Awareness**: Knowledge of efficient register usage and instruction selection
- **Debugging Skills**: Ability to work with low-level debugging tools and concepts
- **Computer Architecture**: Deep understanding of CPU operations and memory hierarchy

---

*This project showcases fundamental computer engineering concepts through practical assembly language implementation.*
