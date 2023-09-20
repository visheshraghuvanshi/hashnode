---
title: "C-Programming Introduction and Basic Building Blocks"
seoTitle: "C Programming for Beginners | Basic C Programming Tutorial"
seoDescription: "A complete guide to C programming for beginners. Learn C basics - variables, data types, operators, functions, arrays, pointers and more in this C tutorial"
datePublished: Wed Sep 20 2023 06:30:11 GMT+0000 (Coordinated Universal Time)
cuid: clmrd74rh000e09mt7ylseoq3
slug: c-programming-basics
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1695185882328/b80db76b-c906-4678-a37e-9d646b461253.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1695186001888/dad7beb3-9a30-4a72-bd9e-09daa2f8178e.png
tags: c, programming-languages, basics

---

### The First C Program

```c
// First C Program
/* The comment self document our
   source code & enhances its readability */

#include <stdio.h> // Used for loading header files
#define MESSAGE "Hello World!" // Define symbolic constants & macros

int main() {
  // Print the message
  printf(MESSAGE);
  return 0;
}
```

**OUTPUT:**

Hello World!

### printf()

`printf(format_string, arguments);`

* printf() stands for print formatted and is used to print data to the stdout (screen).
    
* The format string specifies how the following arguments (variables) should be converted for output.
    
* The format specifiers (like %d for integers, %f for floats, %c for characters etc.) in the format string are replaced by the corresponding arguments.
    
* Example:
    
    ```c
    int a = 10; 
    float b = 20.5;
    char c = 'A';
    
    printf("%d", a);  // Prints 10
    printf("%f", b);  // Prints 20.50
    printf("%c", c);  // Prints A
    ```
    

### C - Characters

* **Letters:-**
    
    * A - Z `ASCII Values:- 65 - 90`
        
    * a - z `ASCII Values:- 97 - 122`
        
* **Digits:-**
    
    * 0 - 9 `ASCII Values:- 48 - 57`
        
* **Other Characters:-**
    
    * Blank, Horizontal tab, Vertical tab, newline, etc.
        

```plaintext
Dec  = Decimal Value
Char = Character

Dec  Char                           Dec  Char     Dec  Char     Dec  Char
---------                           ---------     ---------     ----------
  0  NUL (null)                      32  SPACE     64  @         96  `
  1  SOH (start of heading)          33  !         65  A         97  a
  2  STX (start of text)             34  "         66  B         98  b
  3  ETX (end of text)               35  #         67  C         99  c
  4  EOT (end of transmission)       36  $         68  D        100  d
  5  ENQ (enquiry)                   37  %         69  E        101  e
  6  ACK (acknowledge)               38  &         70  F        102  f
  7  BEL (bell)                      39  '         71  G        103  g
  8  BS  (backspace)                 40  (         72  H        104  h
  9  TAB (horizontal tab)            41  )         73  I        105  i
 10  LF  (NL line feed, new line)    42  *         74  J        106  j
 11  VT  (vertical tab)              43  +         75  K        107  k
 12  FF  (NP form feed, new page)    44  ,         76  L        108  l
 13  CR  (carriage return)           45  -         77  M        109  m
 14  SO  (shift out)                 46  .         78  N        110  n
 15  SI  (shift in)                  47  /         79  O        111  o
 16  DLE (data link escape)          48  0         80  P        112  p
 17  DC1 (device control 1)          49  1         81  Q        113  q
 18  DC2 (device control 2)          50  2         82  R        114  r
 19  DC3 (device control 3)          51  3         83  S        115  s
 20  DC4 (device control 4)          52  4         84  T        116  t
 21  NAK (negative acknowledge)      53  5         85  U        117  u
 22  SYN (synchronous idle)          54  6         86  V        118  v
 23  ETB (end of trans. block)       55  7         87  W        119  w
 24  CAN (cancel)                    56  8         88  X        120  x
 25  EM  (end of medium)             57  9         89  Y        121  y
 26  SUB (substitute)                58  :         90  Z        122  z
 27  ESC (escape)                    59  ;         91  [        123  {
 28  FS  (file separator)            60  <         92  \        124  |
 29  GS  (group separator)           61  =         93  ]        125  }
 30  RS  (record separator)          62  >         94  ^        126  ~
 31  US  (unit separator)            63  ?         95  _        127  DEL
```

## Tokens

* A token is the smallest unit of a C program.
    
* ![Tokens in C - GeeksforGeeks](https://media.geeksforgeeks.org/wp-content/uploads/20230703154836/Tokens-in-C.png align="center")
    

### Special Symbols

`\n - Newline character`

`\t - Tab character`

`\b - Backspace character`

`\r - Carriage return character`

`\v - Vertical tab character`

`\a - Alert (bell) character`

`\? - Question mark`

`\' - Single quote`

`\" - Double quote`

`\ - Backslash`

`\ooo - Octal value`

`\xhh - Hexadecimal value`

**Delimiters:-** Used for syntax purposes

* Space - Separates identifiers, constants, strings, and keywords.
    
* Semicolon (;) - Separates statements.
    
* Comma (,) - Separates function arguments and variables in declarations.
    
* Parentheses (()) - Delimit function calls and group expressions.
    
* Quotes ("") - Delimit string literals.
    

### Constants

A value which will not change during the execution of the program

![Constants in Programming Language | What are Constants? | Definition](https://d1whtlypfis84e.cloudfront.net/guides/wp-content/uploads/2021/02/11180946/Types-of-Constants1.jpg align="center")

**Integer Constants**

* Integers can be written in decimal (base 10), octal (base 8) or hexadecimal (base 16) form.
    

Decimal:

```c
  int a = 10; 
  int b = -200;
```

Octal: Prefix 0

```c
  int c = 012;  // Equivalent to 10 
  int d = 0377; // Equivalent to 255
```

Hexadecimal: Prefix 0x

```c
  int e = 0xA;  // Equivalent to 10
  int f = 0xFF; // Equivalent to 255
```

* The range of integers varies based on the type - short, int, long.
    
* Integers can also be written in scientific notation using the E or e suffix:
    
    ```c
    int a = 1e6; // 1 * 10^6 
    int b = 2E8; // 2 * 10^8
    ```
    

**Floating Point Constant**

* Floating point constants can be written using decimal numbers or scientific notation
    

Decimal:

Decimal notation uses the familiar base 10 system, with a decimal point to represent fractional values.

```c
  float f = 10.5f;  
  double d = 12.345;
```

Scientific notation:

Scientific notation represents numbers as the product of a mantissa and the power of the base (usually 10). It is useful for representing very large or small numbers.

```c
  float f = 1e6f; 
  double d = 2.3e-5;
```

### Character Constant

* Character constants are written using single quotes, e.g. 'a', 'B', '7'.
    
* They represent a single character code from the execution character set.
    
* The value of a character constant is the numeric value of the character in the execution character set.
    
* We can represent non-printable characters using escape sequences:
    
    ```c
    '\t' - tab
    '\n' - new line
    '\r' - carriage return  
    '\b' - backspace
    '\a' - alert (beep)
    ```
    

### Strings

* Strings in C are actually one-dimensional arrays of characters terminated by a null character '\\0'.
    
* String literals are surrounded by double quotes:
    
    "Hello"  
    "This is a string"
    
    ![Strings — Programming and Data Structures 0.2 documentation](https://eecs280staff.github.io/notes/_images/05_string.svg align="center")
    
* String functions like strlen(), strcpy(), strcat() operate on C strings.
    
* String constants have static storage duration and reside in a read-only data section.
    
* To modify a string, we must declare a character array:
    
    ```c
    char str[] = "Hello";
    str[0] = 'J'; // Now str is "Jello"
    ```
    
* We include string.h to use string functions in C.
    
* Multi-byte character strings are supported in C using wchar. h.
    
* Strings are not true data types in C, they are just syntactic sugar for character arrays.
    
* String manipulation in C is tedious and error-prone.