---
title: "C-Programming Operators and Keywords"
seoTitle: "C Operators, Keywords and Preprocessor | A Complete Guide"
seoDescription: "A complete guide to C operators, keywords and the preprocessor. Learn about C operators, reserved words, preprocessor directives like #define, #include"
datePublished: Wed Sep 20 2023 12:30:09 GMT+0000 (Coordinated Universal Time)
cuid: clmrq21fx000009jx36xo2nhh
slug: c-operators-keywords-preprocessor
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1695186375111/c44fad90-a95a-422f-9739-80209dd24020.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1695186495577/b2f4b5f5-69fd-41e0-9d58-54c020e64911.png
tags: c, macros, preprocessor, operators, keywords

---

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