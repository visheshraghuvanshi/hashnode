---
title: "Introduction to functions in C"
seoTitle: "A Complete Guide to Functions in C | Library Functions, User Defined F"
seoDescription: "Learn about library functions, user defined functions, function parameters, return values, call by value and call by reference in C."
datePublished: Sat Sep 23 2023 06:30:10 GMT+0000 (Coordinated Universal Time)
cuid: clmvnincn000b08jte6njhd82
slug: c-functions
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1695278453239/aa27bf50-8356-47a3-a7e6-1eef5cad0e5d.png
tags: c, functions, user-defined-functions, call-by-reference

---

Functions are a block of code that performs a specific task. They allow us to split up our code into smaller, reusable pieces.

* They allow code reusability. The same function can be called multiple times from different parts of the code.
    
* They make our code modular and organized. Related code is bundled into a function.
    
* They can make our code more readable and maintainable.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695277051187/27fead22-c65d-4d1c-b6e3-7d434433d9ca.png align="center")

## Library Functions

Library functions are pre-defined functions that are available in the standard library. We can use these functions in our C programs without defining them ourselves.

Some examples of library functions are:

* printf() and scanf() for input/output
    
* strlen() to find the length of a string
    
* strcpy() to copy a string
    
* malloc() and free() for memory allocation and deallocation
    
* sin(), cos() and tan() for trigonometric functions
    
* sqrt() for square root
    
* abs() for absolute value
    

In order to use a library function in our code, we need to include the corresponding header file. For example:

* To use printf(), we need to #include &lt;stdio.h&gt;
    
* To use strlen(), we need #include &lt;string.h&gt;
    
* To use malloc(), we need #include &lt;stdlib.h&gt;
    
* assert.h, math.h, etc.
    

## User-Defined Functions

User-defined functions are functions that we define ourselves in our C program. As opposed to library functions which are pre-defined in the standard library.

Some reasons to define our own functions are:

1. Custom functionality - We need to implement some functionality that is not provided by library functions.
    
2. Modularity - Splitting our code into functions based on functionality makes it better organized and modular.
    
3. Reusability - We can call the function whenever we need that specific functionality in our program.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695277365762/d89809a6-0e6b-43c1-b9d9-d3efb603d2f3.png align="center")

**Function Declaration:** The function should be declared prior to its usage.

Syntax: `return_type func_name(type1 var1, ...);`

**Function Definition:** Implementation of the function.

**Function Call:** A function is called by giving its name and passing the required arguments.

## Function returning pointers

Functions can return pointers just like any other data type. The return type of the function is simply defined as the pointer data type.

For example:

```c
  int *add(int a, int b) { ... } // Function returns an int pointer
  char *concat(char *a, char *b) { .. } // Returns char pointer
```

## Passing parameters to functions

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695277872189/64bb7fe3-7d50-4c1c-8e29-82fd66db5de7.png align="center")

### Call by Value

Call by value is a method of passing arguments to functions where the value of an argument is copied when the function is called.

* The function receives a copy of the actual argument.
    
* Any changes made to the parameter (copy) inside the function do not affect the original argument.
    
* The original argument remains unchanged.
    

For example:

```c
  void func(int a) {
      a++;  // Increments the local copy 'a'
  }

  int main() {
      int x = 10; 
      func(x);   // Passes the value 10 to func()
      printf("x is %d\n", x); // Prints x is 10, since x was not changed
      return 0;
  }
```

### Call by Reference

Call by reference is a method of passing arguments to a function where the argument's actual memory address is passed to the function.

* The function receives the memory address of the argument.
    
* Any changes made to the parameter (which points to the same memory location) inside the function, reflect outside the function.
    
* The original argument is changed.
    

For example:

```c
  void func(int *a) {
      (*a)++;  // Increments the value at the address *a
  }

  int main() {
      int x = 10;
      func(&x);     // Pass the address of x
      printf("x is %d\n", x); // Prints x is 11
      return 0;
  }
```