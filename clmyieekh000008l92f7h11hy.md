---
title: "A guide to Memory Organisation and Storage Classes in C"
seoTitle: "A Complete Guide to C Memory Organisation | Storage Classes in C"
seoDescription: "Code Segment, Data Segment, Stack Segment and Heap Segment | Storage Classes in C - auto, static, register and external"
datePublished: Mon Sep 25 2023 06:30:12 GMT+0000 (Coordinated Universal Time)
cuid: clmyieekh000008l92f7h11hy
slug: c-memory-organization
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1695622169591/0981f996-325b-439b-bf34-2a5de5a6567f.gif
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1695622340037/460ce416-6029-49d3-aafd-dc60703551c9.gif
tags: memory, static, register, heap, storage-classes

---

## Memory Organisation

When a C program is executed, it is loaded into the memory of the computer. This loaded program is called a process. The memory allocated to a process is called its process address space or memory layout.

The memory layout of a C program is organized into four distinct segments:

1. Code Segment
    
2. Data Segment
    
3. Stack Segment
    
4. Heap Segment
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695618491351/df4a121a-25a9-4cff-9688-c0d7f23d3f85.webp align="center")

### Code Segment

The code segment, also known as the text segment, contains the executable machine code instructions of the functions defined in the program. It forms an important part of the memory organization of a program.

* The code segment contains the actual machine instructions (binary code) of all the functions defined in the program.
    
* It is a read-only memory. This means that the instructions in the code segment cannot be modified at runtime. This protects the program from accidentally modifying its own code while executing.
    
* The code segment is allocated when the program is compiled and linked. During linking, external references are resolved and the machine code is placed in the appropriate memory locations, forming the code segment.
    
* The size of the code segment depends on the number and size of functions defined in the program. Larger programs with more functions will have a larger code segment.
    
* The code segment resides in the text segment of memory. Hence it is also referred to as the text segment.
    

### Data Segment

The data segment contains all global variables and static variables declared in the program. It consists of two subsections:

1. Initialized data: This subsection contains both static and global variables that are initialized with non-zero values. For example:
    
    ```c
    int x = 10;   // Initialized data  
    static int y = 20;  // Initialized data
    ```
    
2. Uninitialized data (or bss segment): This subsection contains all global and static variables that are initialized to zero or do not have explicit initialization in the source code.
    
    The name BSS stands for "Block Started by Symbol". It contains variables that are not explicitly initialized and are thus initialized to zero by default. For example:
    
    ```c
      int a;  // Uninitialized data  
      static int b;  // Uninitialized data
    ```
    

* The data segment is read-write memory. This means that the variables in it can be both read and modified during program execution.
    
* The data segment is allocated when the program is linked. The linker resolves external references and places the variables in the appropriate memory locations.
    
* The size of the data segment depends on the number and size of global/static variables in the program.
    

### Heap

The heap segment is a region of memory used for dynamic memory allocation.

* Everything in the heap is anonymous, meaning it can only be accessed through pointers. Variables allocated on the heap do not have names, they are only identified by the pointers used to access them.
    
* The heap segment is the area where dynamically allocated memory resides. Memory is allocated on the heap using functions like malloc(), calloc(), realloc() and new (for C++).
    
* The heap typically grows upward in memory, meaning as more memory is allocated to the heap, the heap's base address increases.
    
* As memory is allocated on the heap, the process's virtual address space grows. The operating system has to allocate more physical memory to back the process's growing heap.
    
* Memory on the heap persists until it is explicitly freed using free() or delete (in C++).
    
* Fragmentation can occur on the heap over time, leaving "holes" of free memory between allocated blocks. This can lead to performance issues.
    
* The heap memory allocator is responsible for managing the allocation and deallocation of memory on the heap. It keeps track of free and allocated memory blocks.
    
* Memory allocated on the heap is not initialized, it contains whatever data was previously at that memory location.
    
* The heap segment grows and shrinks dynamically as memory is allocated and freed. It has no fixed size.
    

### Stack Segment

* The stack segment is where local (automatic) variables are allocated. In C, local variables are variables declared inside a function body that are not declared as static.
    
* When a function returns, its stack frame is popped up (destroyed) from the stack in a LIFO (Last In First Out) manner. The last function called is the first to be removed when it returns.
    
* When a function is called, a stack frame is created and pushed onto the stack segment. The stack frame contains space for the function's local variables, parameters and return address.
    
* The stack segment grows downward in memory, from higher addresses to lower addresses. As stack frames are pushed, the stack pointer (SP) decreases to make space.
    
* The stack segment has a fixed size. When the stack pointer reaches the bottom of the stack, a stack overflow occurs, crashing the program.
    
* The size of the stack segment depends on the number and size of local variables in functions and the maximum recursive depth of functions.
    
* Local variables on the stack can be read from and written to - the stack is a read-write segment of memory.
    
* The base pointer (
    
* BP) register points to the base of the current stack frame and is used to access local variables and parameters within that stack frame.
    
* When a function calls another, it pushes its return address, base pointer and register values onto the stack, and then sets up a new stack frame.
    

## Storage Classes

Storage classes determine four aspects of a variable:

1. Storage: Where the variable is stored in memory (stack, heap, static memory area)
    
2. Initial value: The default value of an uninitialized variable (zero or garbage value)
    
3. Scope: The range of statements over which the variable is visible
    
4. Lifetime: How long the variable exists, from creation to destruction
    

4 storage classes are:

* auto: Variables are stored on the stack. They are initialized to garbage values. They have block scope and exist for the duration of the block. Used for local variables by default.
    
* register: Tells the compiler to store the variable in a processor register if possible. Otherwise, it is like auto.
    
* static: Variables are stored in a static memory area. They are initialized to zero. They have file scope and exist for the duration of the program.
    
* extern: Declares a variable defined in another scope. Gives it external linkage and file scope.
    

### Auto Storage Class

Automatic variables are local variables declared within a function or block using the auto storage class. If no storage class is specified, variables are automatically auto by default in C.

* **Storage:**
    
    Automatic variables are stored on the stack frame of the function. Space is allocated when the function is called and freed when it returns.
    
* **Scope:**
    
    Automatic variables have block or function scope. They are only visible and accessible within the block or function they are declared in.
    
* **Lifetime:**
    
    The lifetime of automatic variables is from the point of declaration to the end of the block. They cease to exist once the block is exited.
    
* **Initial Values:**
    
    Automatic variables are initialized to garbage values by default. They contain indeterminate values until explicitly initialized.
    

Automatic variables are well suited for temporary storage of local data within functions. They demonstrate LIFO behavior as the last declared variable goes out of scope first.

Automatic variables are called "automatic" because storage is allocated automatically when the function is called and freed automatically when the function returns.

Automatic variables are efficient as they do not occupy memory for the entire duration of the program.

Example:

```c
  void func() {
    int x = 5;   // x is an automatic variable

    printf("x is: %d\n", x);
  }

  int main() {
    func();  
    func();  
  }
```

## Register Storage Class

Register variables are local variables declared within a function using the register storage class specifier.

```c
register int x;
```

* **Storage:**
    
    Register variables are stored in CPU registers instead of RAM. This provides faster access time.
    
    However, if there are not enough CPU registers available, register variables are treated as auto variables and stored in memory.
    
* **Scope:**
    
    Register variables have block or function scope, just like auto variables. They are visible only within the block or function they are declared in.
    
* **Lifetime:**
    
    The lifetime of register variables is from the point of declaration to the end of the block, just like auto variables.
    
* **Initial Values:**
    
    Like auto variables, register variables are initialized to garbage values by default. They contain indeterminate values until explicitly initialized.
    

Register variables should be used for variables that are frequently used to gain performance benefits from CPU registers.  
However, since the number of CPU registers is limited, not all variables can actually be stored in registers.

Register variables are called "register" because the compiler attempts to store them in CPU registers for faster access.

### External Storage Class

External variables are variables declared outside all functions using the extern storage class specifier.  
They have a global scope and lifetime, meaning they are visible to all functions and exist throughout the program execution.

* Declaration: Simply declare the variable name and type. `extern int a;`
    
* Definition: Declares the variable name, and type and allocates storage. `int a;`
    

**Storage:**

* External variables are stored in the data segment (static memory).
    
* They retain their value throughout the program execution.
    

**Scope:**

* External variables have a global scope, meaning they are visible to all functions in the program.
    

**Lifetime:**

* External variables come into existence as soon as the program starts and cease to exist when the program ends. They have the lifetime of the entire program.
    

**Initialization:**

* External variables are initialized to zero/null by default if not explicitly initialized.
    

External variables are used to share data between functions and source files.

Using too many external variables can cause memory wastage and namespace pollution.  
External variables make a program harder to understand and modify.

### Static Storage Class

Static variables are variables declared with the static storage class specifier.

They are of two types:

* Static internal variables - Declared inside a function
    
* Static external variables - Declared outside of all functions
    

Static Internal Variables:

* Declared within a function using the static keyword.
    
* Have function scope (local to the function).
    
* Retain their value between function calls. That is, they preserve their value even after the function returns.
    
* Are initialized only once, at the start of the program.
    
* Example:
    
    ```c
      void func() {
         static int count = 0; 
         count++;
         printf("Count is %d\n", count);
      }
    
      int main() {
         func();
         func();   // Count is 2
         func();   // Count is 3
      }
    ```
    

Static External Variables:

* Declared outside of all functions using static.
    
* Have file scope, i.e. visible within the file.
    
* Are initialized to 0.
    
* Have the lifetime of the program.
    
* Example
    
    ```c
      static int count;
    
      void func1() {
         count++;
      }
    
      void func2() {
         count--; 
      }
    
      int main() {
         func1();
         func2();
      }
    ```
    

**Storage:**

* Static variables are stored in the data segment.
    

**Initialization:**

* Static variables are initialized to 0 by default if not explicitly initialized.
    

Static variables are used to retain data between function calls and across the program.