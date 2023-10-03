---
title: "C-Programming Execution and Expressions"
seoTitle: "The C Program Execution Process | Preprocessing, Compilation, Assembly"
seoDescription: "A detailed look at the C program execution process from preprocessing to program execution. Learn about the roles of the preprocessor, compiler, ..."
datePublished: Thu Sep 21 2023 06:30:09 GMT+0000 (Coordinated Universal Time)
cuid: clmssmxbg000209mc2gh9duyx
slug: c-program-execution-process
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1695186759985/cc47420b-84b6-4392-8765-4cb789f41196.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1695186776627/2ef407e3-19f0-47cc-b8af-65d72e4fc0e4.png
tags: c, history, compiler, assembler, linker

---

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