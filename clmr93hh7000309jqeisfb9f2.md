---
title: "C Programming"
datePublished: Wed Sep 20 2023 04:35:23 GMT+0000 (Coordinated Universal Time)
cuid: clmr93hh7000309jqeisfb9f2
slug: c-programming

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

Scientific notation represents numbers as the product of a mantissa and a power of the base (usually 10). It is useful for representing very large or small numbers.

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
    

### Operator

An operator is a symbol that performs some operation on one or more operands. Operators are used to assign values, compare values or perform calculations with values.

* Arithmetic Operators
    
* Relational Operators
    
* Logical Operators
    

## Keywords (or) Reserved Words

Keywords or reserved words are words that have a special meaning in a programming language. They are reserved by the compiler and cannot be used as variable names, function names, class names, etc.

Keywords can be classified as:

1. Pre-defined data types
    
    * `char`
        
    * `int`
        
    * `float`
        
    * `double`
        
    * `void`
        
2. Modifiers
    
    * `short`
        
    * `long`
        
    * `signed`
        
    * `unsigned`
        
3. Qualifiers
    
    * `const`
        
    * `volatile`
        
4. Storage classes
    
    * `auto`
        
    * `static`
        
    * `register`
        
    * `extern`
        
5. Control Structure
    
    * i`f`
        
    * `else`
        
    * `while`
        
    * `do`
        
    * `for`
        
    * `switch`
        
    * `goto`
        
    * `case`
        
    * `default`
        
    * `break`
        
    * `continue`
        
    * `return`
        
6. User-defined data type
    
    * `struct`
        
    * `union`
        
    * `enum`
        
    * `typedef`
        
7. sizeof
    
    * `sizeof()`
        

Words used in C programs are either keywords or identifiers.

### Identifiers

Identifiers are names given to entities in a program like variables, functions, constants, etc. They are used to identify these entities.

Some rules for identifiers in C are:

1. An identifier must start with the letter A-Z, a-z or underscore ( \_ ).
    
2. After the first character, identifiers can contain letters, digits and underscore.
    
3. Identifiers are case-sensitive. age and Age are two different identifiers.
    
4. Keywords cannot be used as identifiers.
    
5. Identifiers cannot start with a digit.
    

Some valid identifiers:

`age` `name` `salary1` `firstname`

Some invalid identifiers:

`1age` - starts with a digit

`class` - is a keyword

`func#` - contains special character #

## C-preprocessor

The C preprocessor is a text substitution tool that performs macro definition, macro expansion, file inclusion, and conditional compilation. It is not part of the compiler itself but rather a separate step in the compilation process.

The preprocessor uses directives that start with # to instruct the compiler to perform required preprocessing before actual compilation. Using the preprocessor has the following advantages:

* It makes programs easier to develop by:
    
    * Allowing macro definitions to reduce redundant code
        
    * Allowing file inclusion to split large programs into multiple files
        
* It makes programs easier to read and maintain by:
    
    * Using macros and #defines for constants
        
    * Giving variables and functions meaningful names
        
* It makes programs easier to modify by:
    
    * Allowing conditional compilation to compile different versions
        
    * Allowing macro parameters to change behaviour
        

| **Preprocessor Directives** | **Description** |
| --- | --- |
| **#define** | Used to define a macro |
| **#undef** | Used to undefine a macro |
| **#include** | Used to include a file in the source code program |
| **#ifdef** | Used to include a section of code if a certain macro is defined by #define |
| **#ifndef** | Used to include a section of code if a certain macro is not defined by #define |
| **#if** | Check for the specified condition |
| **#else** | Alternate code that executes when #if fails |
| **#endif** | Used to mark the end of #if, #ifdef, and #ifndef |

### #define

Defines a macro substitution. It performs simple textual substitution of the macro name before actual compilation.

Syntax:

`#define macro_name replacement_text`

Example:

`#define PI 3.14`

`#define square(x) x*x`

### #include

Used to insert the contents of a header file into the source code at the location of the #include statement.

Syntax:

`#include <filename>` // For system header files

`#include "filename"` // For user-defined header files

Example:

`#include <stdio.h>`

`#include "functions.h"`

Advantages:

* Allows splitting large programs into multiple files.
    
* Header files contain function prototypes and macro definitions that are shared across multiple source files.
    

## C Program Execution Process

![Explain program execution process in C. - Sarthaks eConnect | Largest  Online Education Community](https://www.sarthaks.com/?qa=blob&qa_blobid=1529820056327819138 align="center")

1. Preprocessing: The C preprocessor performs tasks like macro expansion, file inclusion, and conditional compilation. It processes the #define, #include and #if directives and generates preprocessed source code.
    
2. Compilation: The preprocessed source code is compiled by the compiler to generate object code. The compiler checks the syntax, and semantics and generates object code (machine code + symbol table).
    
3. Assembly: The object files generated by the compiler are assembled by the assembler to produce the executable file. The assembler resolves external references and links object files.
    
4. Linking: The linker combines multiple object files and library files and generates an executable file. It resolves external function calls and variable uses.
    
5. Program Execution: The generated executable file is executed on the system. The operating system loads the executable into memory and the CPU starts executing the machine instructions.
    

## History

* 1969 - Dennis Ritchie starts working at Bell Labs. He started developing the B programming language as an improved version of Thompson's BCPL language.
    
* 1970 - Ken Thompson starts developing the Unix operating system at Bell Labs.
    
* 1971 - The first version of Unix is written in assembly language.
    
* 1972 - Ritchie develops a C compiler to allow Unix to be written in a higher-level language. The language is initially called "B" and then renamed to "C".
    
* 1972 - The first C compiler and Unix written in C are released.
    
* 1973 - Version 6 Unix is the first to be written almost entirely in C. This starts the close relationship between C and Unix.
    
* 1974 - The C language is described in Ritchie's paper "The Development of the C Language".
    
* 1978 - Brian Kernighan and Dennis Ritchie publish "The C Programming Language" book. This popularizes C and establishes its syntax and semantics.
    
* 1983 - C Standardization committee formed. The ANSI X3J11 committee works to standardize C.
    
* 1989 - The ANSI X3.159-1989 standard for C is published and widely adopted. This makes C a truly portable language.
    
* 1990 - The ISO C standard ISO/IEC 9899 is published.
    
* In the 1990s - C became extremely popular and is used to write many important applications and operating systems like Linux kernel.
    
* 1994 - ISO publishes C9X to add features to C like function prototypes.
    
* 1999 - ISO publishes the C99 standard with many new features.
    
* 2011 - The current C11 standard is published with further improvements.
    
* Today - C remains an important programming language due to its performance, portability and ability to interface with hardware. It is used for systems programming, embedded systems and low-level applications.
    

## Operators and Expressions

### Variable

Variables are used to store values that can change during the execution of a program.

* A variable is a named memory location that can store different values at different times during the execution of a program.
    
    Syntax: `datatype variablename;`
    
* They are declared with a name and a data type. Some examples of variable declarations are:
    
    ```c
    int x;  
    float y;
    char name;
    ```
    
* Variables are then assigned a value using the assignment operator (=). For example:
    
    ```c
    x = 5;  
    y = 3.14;
    name = 'John';
    ```
    
* The data type of a variable determines the type of values it can store. Common data types are int, float, char, double, boolean, etc.
    
* Variables are allocated memory during compilation. The amount of memory allocated depends on the data type.
    
* Variables allow us to store data and manipulate them to perform various computations in a program. They are fundamental to programming.
    

### Data Types

Data types determine

* Type of Data
    
* Size of memory
    
* Range of data
    
* Operations that can be performed on data
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695178206786/ffbbf587-7757-42dd-b85a-c4cffe0054f0.png align="center")

### Modifiers

Modifiers specify the scope, storage duration and other properties of variables and functions in C.

The main modifiers in C are:

1. static - Specifies that a variable has static storage duration. The variable exists and retains its value for the lifetime of the program.
    
2. extern - Specifies an external variable or function. It allows a variable/function to be accessed from other files.
    
3. auto - Specifies a local variable with automatic storage duration. The variable is destroyed when the function exits. This is the default for variables.
    
4. register - Specifies that a variable should be stored in a register. It hints to the compiler to optimize the variable.
    
5. const - Specifies a constant variable. The value of a const variable cannot be changed.
    
6. volatile - Specifies that a variable can be modified by external factors. The compiler should not optimize access to it.
    

For functions, the main modifiers are:

1. static - Specifies a local function. The function is only visible within the file.
    
2. inline - Suggests to the compiler to replace calls to the function with the actual code. It optimizes the function.
    

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
| **\[\]** | Array Subscript (Square Brackets) |
| **.** | Dot Operator |
| **\-&gt;** | Structure Pointer Operator |
| **++ , —** | Postfix increment, decrement |
| 2 | **++ / —** | Prefix increment, decrement | Right-to-Left |
| **\+ / –** | Unary plus, minus |
| **! , ~** | Logical NOT,  Bitwise complement |
| **(type)** | Cast Operator |
| **\*** | Dereference Operator |
| **&** | Addressof Operator |
| **sizeof** | Determine size in bytes |
| 3 | **\*,/,%** | Multiplication, division, modulus | Left-to-Right |
| 4 | **+/-** | Addition, subtraction | Left-to-Right |
| 5 | **&lt;&lt; , &gt;&gt;** | Bitwise shift left, Bitwise shift right | Left-to-Right |
| 6 | **&lt; , &lt;=** | Relational less than, less than or equal to | Left-to-Right |
| **\&gt; , &gt;=** | Relational greater than, greater than or equal to |
| 7 | **\== , !=** | Relational is equal to, is not equal to | Left-to-Right |
| 8 | **&** | Bitwise AND | Left-to-Right |
| 9 | **^** | Bitwise exclusive OR | Left-to-Right |
| 10 | **|** | Bitwise inclusive OR | Left-to-Right |
| 11 | **&&** | Logical AND | Left-to-Right |
| 12 | **||** | Logical OR | Left-to-Right |
| 13 | **?:** | Ternary conditional | Right-to-Left |
| 14 | **\=** | Assignment | Right-to-Left |
| **+= , -=** | Addition, subtraction assignment |
| **\*= , /=** | Multiplication, division assignment |
| **%= , &=** | Modulus, bitwise AND assignment |
| **^= , |=** | Bitwise exclusive, inclusive OR assignment |
| **&lt;&lt;=, &gt;&gt;=** | Bitwise shift left, right assignment |
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

# C-Statements

In C Programming, instructions are written in the form of statements.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695182521310/282166a7-de49-4838-a1b4-2eb7196b1a7e.png align="center")

## Expression Statements

Expression statements in C are statements that contain expressions but do not return a value.

Some examples of expression statements in C are:

* Assignment expressions: `x = 5;`
    
* Function calls: `printf("Hello");`
    
* Increment/decrement expressions: `i++;` `j--;`
    
* Comma expressions: `x = (y, z);`
    

## Compound Statements

Compound statements in C are statements that group multiple statements into a block. They are defined within curly braces { }.

The basic syntax of a compound statement is:

`{ statement1; statement2; ... statementn; }`

For example:

```c
  {
      int x = 5;  
      printf("x = %d", x);
      x++;
  }
```

## Control Statements

Control statements are programming constructs that allow us to control the flow of execution in a program. They change the normal sequential flow of execution and make decision-based executions possible.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695183068768/f15d0937-44dc-442b-8be4-4e885d24ffbf.png align="center")

### Sequential Statements

Sequential control statements are control statements that execute code in a linear, sequential order. They follow the normal, top-to-bottom flow of execution in a program.

Some examples of sequential control statements are:

* Simple statements - Assignments, function calls, etc. These execute one after the other in the order they are written.
    
    ```c
    int x = 5;  
    int y = 10;
    int z = x + y;
    ```
    
* Compound statements - Groups of statements enclosed in curly braces. These also execute sequentially from top to bottom.
    
    ```c
    {
        int x = 5; 
        int y = 10;  
        int z = x + y; 
    }
    ```
    

### Selection Statements

**if:** A simple selection/decision statement

```c
  if (condition) {
      // code executes if condition is true  
  }
```

**if-else:** A bi-directional control statement

```c
  if (condition) {
      // code executes if condition is true    
  }
  else {
     // code executes if condition is false
  }
```

**nested if:** if constructs can also be nested

```c
  if (condition1) {
      if (condition2) {
           // code
      }
  }
```

**else if ladder:**

```c
  if (condition1) {
      // code
  }  
  else if (condition2) {
      // code 
  }
  else if (condition3) {
     // code
  }
  else {
     // default case  
  }
```

**switch:** The switch statement allows you to select one of many code blocks to execute based on different cases.

* It provides an efficient alternative to multiple if-else if statements.
    
* The expression is evaluated only once.
    
* The case values must be constants, not variables or expressions.
    
* You must include a break statement at the end of each case, otherwise, execution will "fall through" to the next case.
    
* The default case is optional and acts as a catch-all if no cases match.
    

```c
  switch(n) {
      case 1: 
          // code
          break; 

      case 2:  
          // code    
          break;

      default:
         // code  
  }
```

**\*Dangling else**

The dangling else issue refers to ambiguity in the parsing of nested if-else statements. It occurs when an else clause can potentially belong to multiple if statements.

For example, consider this code:

```c
  if (condition1)
      if (condition2)
          statement1;  
      else   
          statement2;
```

Here, the else clause could belong to either the inner if or the outer if. The compiler does not know for sure which if the else matches. This is called a dangling else.

There are two ways this ambiguity can be resolved:

1. The else binds to the nearest if - this is known as the "greedy" or "dangling" else solution. In the above example, the else would bind to the inner if.
    
2. The else binds to the logically corresponding if - this is known as the "non-dangling" else solution. Here, the else would bind to the outer if.
    

Most compilers, including C and Java, use the "dangling" else solution - the else matches the closest if.

### Iterative Statements

Iterative statements allow us to repeat a block of code a specified number of times. The main iterative statements in C are:

**while loop (entry-controlled loop):**

![while loop in C - GeeksforGeeks](https://media.geeksforgeeks.org/wp-content/uploads/20220927171802/WhileloopinC2.png align="center")

```c
  while (condition) {
      // code repeats while condition is true
  }
```

**do-while loop (exit-controlled loop):**

* In a do-while loop, the condition is tested at the end of the loop.
    
* This loop is executed at least once
    

![do...while Loop in C - GeeksforGeeks](https://media.geeksforgeeks.org/wp-content/uploads/20221006152307/dowhileloopinc.png align="center")

```c
  do {
      // code 
  } while (condition);
```

**for loop:**

* init - Initialize the loop counter variable, usually setting it to 0.
    
* condition - The condition to be checked before each loop iteration.
    
* increment - How the counter variable changes after each iteration.
    

![C for Loop - GeeksforGeeks](https://media.geeksforgeeks.org/wp-content/uploads/20230627104742/C-for-Loop.png align="center")

```c
  for (init; condition; increment) {
      // code 
  }
```

### Jump Statements / Unconditional branch/control statements:

Jump statements, also known as unconditional branch statements, allow the program flow to jump to a different part of the code, bypassing any intermediate statements.

1. **goto**
    
    The goto statement allows the program to jump to a labelled statement. For example:
    
    ```c
      goto start;
    
      // ... some code
    
      start:  
         printf("Control has jumped to this point using goto");
    ```
    
    Here the goto statement will jump control to the label start, bypassing any intermediate code.
    
2. **continue**
    
    The continue statement skips the remaining code in the current iteration of a loop and continues with the next iteration. For example:
    
    ```c
      for (int i = 0; i < 10; i++) {
         if (i == 5) {
             continue;
         }
         printf("%d", i);
      }
      // Prints 01234 6789
    ```
    
    Here the continue statement skips printing 5 and continues with the next iteration.
    
3. **break**
    
    The break statement exits the innermost switch or loop immediately, transferring control to the statement following the block. For example:
    
    ```c
      for (int i = 0; i < 10; i++) {
         if (i == 5) {
             break;  
         }
         printf("%d", i);
      }
      // Prints 01234
    ```
    
    Here the break statement exits the for loop when i becomes 5.
    
4. **return**
    
    The return statement causes an immediate jump from the current function to the caller.
    
    For example:
    
    ```c
      int sum(int a, int b) {
         if (a > 100) {
             return a;  // return a and exit the function
         }
         return a + b; // return the sum and exit the function   
      }
    
      int result = sum(200, 50);
      printf("Result is %d", result);
      // Prints Result is 200
    ```