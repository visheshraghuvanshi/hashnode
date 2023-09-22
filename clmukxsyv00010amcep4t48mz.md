---
title: "A guide to pointers in C"
seoTitle: "A Complete Guide to Pointers in C | Memory Addresses and References"
seoDescription: "Learn about pointer operators, pointer arithmetic, pointer declarations, pointer typecasting and more with examples."
datePublished: Fri Sep 22 2023 12:30:12 GMT+0000 (Coordinated Universal Time)
cuid: clmukxsyv00010amcep4t48mz
slug: c-pointers
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1695276508862/03803ef9-08e9-419f-9a75-abc199e9ecf8.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1695276602783/dba0f624-27bf-4e11-97ab-92e67cd2d6cd.png
tags: c, pointers, memory, address, pointers-in-c

---

## Address of a variable

Every variable in C has a memory location where it is stored. This memory location is called the variable's address.

![Print the memory address of a variable in Go (Golang)](https://gosamples.dev/print-address/pointer.png align="center")

## Pointer

* A pointer is a variable that stores the address of another variable.
    
* We use the \* (asterisk) operator to define pointers and the & (address of) operator to get the address of a variable.
    
* For example:
    
    ```c
    int a = 10;
    int *p;
    
    p = &a;  // p is a pointer to an integer, and now points to address of a
    ```
    
* Here `p` is a pointer that stores the address of `a`.
    
* We use the -&gt; operator to access the value at the address stored in the pointer.
    
    ```c
    int val = *p; // val becomes 10, as p contains address of a which has value 10
    ```
    
* Pointers allow us to pass variables by reference instead of by value. This is useful to modify the original variable.
    

### Pointer Operators

Here are short notes on the main pointer operators in C:

`&` - Address Of Operator

* Returns the memory address of a variable.
    
* Syntax: &variable\_name
    
* Example
    
    ```c
    int a = 10; 
    int *ptr;
    
    ptr = &a; // ptr points to the address of a
    ```
    

`*` Dereference Operator

* Accesses the value at the address stored in a pointer.
    
* Syntax: \*pointer\_name
    
* Example
    
    ```c
    int val = *ptr;  // val becomes 10, as ptr points to address of a which has value 10
    ```
    

`->` - Structure Dereference Operator

* Accesses a member of a structure through a pointer.
    
* Equivalent to using the `.` operator, but dereferences the pointer first.
    
* Example
    
    ```c
    struct student *p;
    p->age = 20; // Accesses the age member through pointer p
    ```
    

### Format Specifiers for pointers

The format specifiers for pointers in C are:

* %p - To print a generic pointer address. This is the preferred way.
    
* %#x - To print a pointer address with 0x prefix.
    
* %x - To print a pointer address as an unsigned hexadecimal integer, without the 0x prefix.
    
* %d would give an `incorrect` result when used to print a pointer address. It may print some decimal number, but that number does not represent the actual pointer address.
    
    Example
    
    ```c
    #include <stdio.h>
    int main()
    {
        int a = 5;
        int *ptr;
        ptr = &a;
        printf("%p\n", ptr);   
        printf("%x\n", ptr);
        printf("%#x\n", ptr);
        return 0;
    }
    ```
    
    OUTPUT:
    
    `0x7fff17337f4c`
    
    `17337f4c`
    
    `0x17337f4c`
    

### Size of pointer variable

The size of a pointer variable depends on the system architecture. It can be 4 bytes or 8 bytes, depending on whether it is a 32-bit or 64-bit system.

* On 32-bit systems, pointers are usually 4 bytes in size
    
* On 64-bit systems, pointers are usually 8 bytes in size
    

The size of a `pointer variable does not depend on the type of data it is pointing` to. A pointer to an int and a pointer to a char will have the same size, depending on the system architecture.