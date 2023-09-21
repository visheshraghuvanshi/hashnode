---
title: "C-Programming Operators"
seoTitle: "A Guide to C Operators | Arithmetic, Assignment, Relational & More"
seoDescription: "A detailed guide to operators in C including arithmetic, assignment, relational, bitwise, logical and conditional operators. Learn about operator precedence"
datePublished: Thu Sep 21 2023 12:30:09 GMT+0000 (Coordinated Universal Time)
cuid: clmt5hwaa000x09jofuy995kw
slug: c-operators
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1695187220912/11b57c9f-c3d6-477b-b883-62935f5a1b4b.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1695187231320/e9bbc469-fd9b-4a93-bdbb-902c5aa88896.png
tags: c, operators, type-conversion, bitwise-operators, operator-precedence

---

## Operators

Operators are special symbols that perform operations on variables and values. They are used to assign values, compare values, perform arithmetic operations, perform logical operations, etc.

![C Operators and Expressions - JustdoCodings](https://3.bp.blogspot.com/-fJWSAG_fLUc/WuQKpwtcMFI/AAAAAAAAAj8/fVbo7p7TWI8QMNH-n3HsOkhj3f5V3kEpgCLcBGAs/s1600/Operators.png align="center")

Some of the main types of operators in programming languages are:

1. Arithmetic operators - Used for basic arithmetic operations like addition, subtraction, multiplication, division, etc.
    
    Examples: +, -, \*, /
    
2. Assignment operators - Used to assign values to variables.
    
    Examples: =, +=, -=
    
3. Comparison operators - Used to compare two values and return a boolean result.
    
    Examples: ==, !=, &gt;, &lt;, &gt;=, &lt;=
    
4. Logical operators - Used to combine conditional statements.
    
    Examples: && (and), || (or), ! (not)
    
5. Bitwise operators - Used to perform bit-level operations on integer values.
    
    Examples: & (and), | (or), ^ (xor)
    
6. String operators - Used to concatenate and compare strings.
    
    Examples: + (concatenation), ==, !=
    
7. Conditional operator - Acts as a mini if-else expression.
    
    Example: condition ? exprIfTrue : exprIfFalse
    

### Precedence And Associativity of Operators

| **Precedence** | **Operator** | **Description** | **Associativity** |
| --- | --- | --- | --- |
| 1 | **()** | Parentheses (function call) | Left-to-Right |
| **\[\]** | Array Subscript (Square Brackets) |  |  |
| **.** | Dot Operator |  |  |
| **\-&gt;** | Structure Pointer Operator |  |  |
| **++ , —** | Postfix increment, decrement |  |  |
| 2 | **++ / —** | Prefix increment, decrement | Right-to-Left |
| **\+ / –** | Unary plus, minus |  |  |
| **! , ~** | Logical NOT,  Bitwise complement |  |  |
| **(type)** | Cast Operator |  |  |
| **\*** | Dereference Operator |  |  |
| **&** | Address of Operator |  |  |
| **sizeof** | Determine size in bytes |  |  |
| 3 | **\*,/,%** | Multiplication, division, modulus | Left-to-Right |
| 4 | **+/-** | Addition, subtraction | Left-to-Right |
| 5 | **&lt;&lt; , &gt;&gt;** | Bitwise shift left, Bitwise shift right | Left-to-Right |
| 6 | **&lt; , &lt;=** | Relational less than, less than or equal to | Left-to-Right |
| **&gt; , &gt;=** | Relational greater than, greater than or equal to |  |  |
| 7 | **\== , !=** | Relational is equal to, is not equal to | Left-to-Right |
| 8 | **&** | Bitwise AND | Left-to-Right |
| 9 | **^** | Bitwise exclusive OR | Left-to-Right |
| 10 | \*\* | \*\* | Bitwise inclusive OR |
| 11 | **&&** | Logical AND | Left-to-Right |
| 12 | \*\* |  | \*\* |
| 13 | **?:** | Ternary conditional | Right-to-Left |
| 14 | **\=** | Assignment | Right-to-Left |
| **+= , -=** | Addition, subtraction assignment |  |  |
| **\*= , /=** | Multiplication, division assignment |  |  |
| **%= , &=** | Modulus, bitwise AND assignment |  |  |
| \*\*^= , | \=\*\* | Bitwise exclusive, inclusive OR assignment |  |
| **&lt;&lt;=, &gt;&gt;=** | Bitwise shift left, right assignment |  |  |
| 15 | **,** | comma (expression separator) | Left-to-Right |

## Type Conversion

Type conversion is the process of converting a value of one data type into another data type.

In C, type conversion can be either implicit or explicit.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695179009070/4bfa4bc6-e770-4e83-bfe4-6b3aff9768ed.png align="center")

Implicit type conversion is done automatically by the compiler based on the context. For example:

* Assigning a smaller type to a larger type - int to float.
    
* Using a smaller type in arithmetic operations with a larger type.
    

Explicit type conversion involves using a typecast operator. For example:

`(type) expression`

## Bitwise Operators

Bitwise operators work on bits and perform bit-by-bit operation

& - Bitwise AND

| - Bitwise OR

^ - Bitwise Exclusive

~ - Bitwise Compliment

&lt;&lt; - Left Shift

\&gt;&gt; - Right Shift

### Bitwise AND (&)

The Bitwise AND operator (&) performs a logical AND operation on each pair of corresponding bits in its two operands. It returns a 1 in the corresponding bit position if both the bits are 1. Otherwise, it returns a 0.

eg.

```plaintext
   12   = 00001100
   25   = 00011001
12 & 25 = 00001000 = 8
```

### Bitwise OR (|)

The Bitwise OR operator (|) performs a logical OR operation on each pair of corresponding bits in its two operands. It returns a 1 in the corresponding bit position if at least one of the two bits is 1.

```plaintext
   12   = 00001100
   25   = 00011001
12 | 25 = 00011101 = 29
```

### Bitwise XOR (^)

The Bitwise XOR operator (^) performs a logical XOR (exclusive OR) operation on each pair of corresponding bits in its two operands. It returns a 1 in the corresponding bit position if only one of the two bits is 1.

```plaintext
   12   = 00001100
   25   = 00011001
12 ^ 25 = 00010101 = 21
```

### Bitwise Compliment (~)

The Bitwise Compliment operator (~) performs a bitwise NOT operation on each bit of its operand. It inverts all the bits and then adds one to the result.

```plaintext
 35 = 00100011
~35 = 11011100 //2's compliment of this number
Ans = -36
```

### Right Shift (&gt;&gt;)

The Right Shift operator (&gt;&gt;) shifts the bits of the left operand (n) rightwards by the number of bits specified by the right operand (m). The vacated bits are filled in with 0s.

For example:

```plaintext
   12   = 00001100 
12 >> 2 = 00000011 = 3
```

### Left Shift (&lt;&lt;)

The Left Shift operator (&lt;&lt;) shifts the bits of the left operand (n) leftwards by the number of bits specified by the right operand (m). The vacated bits are filled in with 0s.

For example:

```plaintext
   12   = 00001100 
12 << 2 = 00110000 = 48
```