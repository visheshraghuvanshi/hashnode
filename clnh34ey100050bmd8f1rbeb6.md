---
title: "Dynamic Memory Allocation in C"
seoTitle: "Dynamic Memory Allocation in C | malloc(), calloc(), realloc(), free()"
seoDescription: "Dynamic Memory Allocation in C using functions like malloc(), calloc(), realloc() and free().Memory leaks, dangling pointers and examles."
datePublished: Sun Oct 08 2023 06:30:09 GMT+0000 (Coordinated Universal Time)
cuid: clnh34ey100050bmd8f1rbeb6
slug: dynamic-memory-allocation
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1696668925225/fa440e4f-a5a2-4ed2-ab06-00923bdd223d.png
tags: c-programming, memory-leak, dynamic-memory-allocation, dangling-pointers

---

## Memory Allocation Types

1. Static Memory Allocation
    
2. Automatic Memory Allocation
    
3. Dynamic Memory Allocation
    

![FreeRTOS Memory Management](https://www.digikey.com/maker-media/60c3b8b7-f4af-4a07-b139-0acae5a846fb align="center")

### Comparison

| **Static** | **Dynamic** |
| --- | --- |
| Memory allocated at compile time | Memory allocated at runtime |
| Fixed memory size | Flexible memory size |
| No overhead | Memory management overhead |
| Simple | More complex |
| No memory leaks | Potential for memory leaks |

## Dynamic Memory Allocation

### Need for dynamic memory allocation

* Static memory allocation allocates memory at compile time which has a fixed size
    
* The size remains the same throughout the lifetime of the program
    
* This can lead to a waste of memory if the allocated size is more than the actual requirement
    
* It can also cause issues if the allocated size is less than the actual requirement
    

To solve these issues, C provides functions for dynamic memory allocation:

* Memory is allocated at runtime based on the actual requirements of the program
    
* The allocated memory size can grow and shrink as needed
    

### Memory allocation functions in C

* **malloc():** Allocates a block of memory of the specified size and returns a pointer to the allocated memory. If memory cannot be allocated, it returns NULL.
    
* **calloc():** Similar to malloc() but initializes all the bytes of the allocated memory block to 0.
    
* **realloc():** Changes the size of the memory block pointed to by the given pointer. If the area pointed by the pointer is larger, the extra memory is not changed. If the new size is larger, the extra memory has an indeterminate value.
    
* **free():** Frees the memory block pointed to by the given pointer. The pointer becomes invalid after calling free().
    

## Malloc()

### Syntax of malloc()

```c
  pointer_variable = malloc(size);
```

Here,

* `pointer_variable` is a pointer variable of the required type (int*, float* etc)
    
* `size` is the number of bytes to allocate
    

### Usage

```c
  int *ptr = malloc(sizeof(int) * n);  // Allocate memory for n integers

  float *fptr = malloc(sizeof(float) * m); // Allocate memory for m floats
```

Here `ptr` and `fptr` will point to the allocated memory blocks of the specified sizes.

### Example

Allocating memory for an array:

```c
  #include <stdio.h> 
  #include <stdlib.h>

  int main() {
    int n;
    printf("Enter number of integers: ");
    scanf("%d", &n);

    int *ptr = malloc(sizeof(int) * n);

    if (ptr == NULL) {
      printf("Error! Unable to allocate memory\n");
      exit(0);  
    }

    // Use ptr array

    free(ptr);
    return 0;
  }
```

## Calloc()

### Syntax of calloc()

```c
  pointer_variable = calloc(n, size);
```

Here,

* `pointer_variable` is a pointer variable of the required type (int*, float* etc.)
    
* `n` is the number of elements to allocate memory for
    
* `size` is the size of each element in bytes
    

calloc() allocates memory for an array of `n` elements of size `size` each and initialize all bytes to 0.

### Differences between malloc() and calloc()

* malloc() just allocates raw memory without initializing
    
* calloc() allocates memory and initializes all bytes to 0 (or NULL)
    
* calloc() takes the number of elements and size, while malloc() takes only total size
    

### Example

```c
  #include <stdio.h>
  #include <stdlib.h>

  int main() {
    int *ptr, n, i;

    printf("Enter number of integers: ");
    scanf("%d", &n);

    ptr = calloc(n, sizeof(int));

    if (ptr == NULL) {
      printf("Error! Unable to allocate memory.");
      exit(0);
    }  

    // Use allocated memory 

    for (i = 0; i < n; i++)
      printf("%d ", ptr[i]);  // Prints 0 0 0 ...  

    free(ptr);
    return 0;  
  }
```

## Realloc():

### Syntax of realloc()

```c
  pointer_variable = realloc(pointer_variable, new_size);
```

Here,

* `pointer_variable` is the pointer to the previously allocated memory block
    
* `new_size` is the new size in bytes to resize the memory block to
    

### Usage

```c
  int *ptr = malloc(sizeof(int) * 10);

  // Resize the memory block to hold 20 integers
  ptr = realloc(ptr, sizeof(int) * 20);
```

### Example

```c
  #include <stdio.h>
  #include <stdlib.h>

  int main() {
    int *ptr, n = 10, i;

    ptr = malloc(n * sizeof(int));

    // Taking input and storing in array 
    for (i = 0; i < n; i++) {
      scanf("%d", &ptr[i]);  
    }

    n = n + 5;  // Increase array size by 5

    ptr = realloc(ptr, n * sizeof(int));

    if (ptr == NULL) {
      printf("Error! Unable to allocate memory.");
      exit(0); 
    }

    // Taking 5 more inputs  
    for (i = 10; i < n; i++) {
      scanf("%d", &ptr[i]);  
    }

    // Print all elements  
    for (i = 0; i < n; i++) {
      printf("%d", ptr[i]);  
    }

    free(ptr);
    return 0;
  }
```

## Free():

### Syntax of free()

```c
  free(pointer_variable);
```

Here, `pointer_variable` is the pointer to the memory block that was allocated using malloc(), calloc() or realloc().

### Usage

```c
  int *ptr = malloc(sizeof(int) * 10);

  // Use ptr...

  free(ptr);  // Free the memory block pointed to by ptr
```

### Example

```c
  #include <stdio.h> 
  #include <stdlib.h>

  int main()  {
    int *ptr, n, i;

    printf("Enter number of integers: "); 
    scanf("%d", &n);

    ptr = malloc(n * sizeof(int));

    if (ptr == NULL) {
      printf("Error! Unable to allocate memory.");
      exit(0);
    }

    // Take input and store in array
    for (i = 0; i < n; i++) {
      scanf("%d", &ptr[i]);  
    }

    // Use allocated memory

    free(ptr);  // Free the memory block pointed to by ptr

    return 0;
  }
```

## Memory Leak

### What is memory leak?

A memory leak occurs when a program allocates memory but fails to free it after use. This leads to a gradual buildup of unused memory blocks over time.

### Causes of memory leak

The main causes of memory leaks are:

* Forgetting to free allocated memory. For example, by losing the pointer to the allocated memory.
    
* Holding onto pointers longer than necessary. For example, storing pointers in global variables.
    
* Creating reference cycles between data structures that point to each other.
    
* Handling allocation failure incorrectly and not freeing previously allocated memory.
    

### How to avoid memory leak

Some ways to avoid memory leaks are:

* Free all allocated memory using free().
    
* Set pointers to NULL after freeing to avoid accidental reuse.
    
* Limit the scope of pointers as much as possible.
    
* Use tools like Valgrind to detect memory leaks and debug memory issues.
    

## Dangling Pointer

### What is a dangling pointer?

A dangling pointer is a pointer that references a memory location that may have been deleted or reallocated. This can lead to undefined behaviour and crashes.

### How dangling pointers are created

Dangling pointers are created when:

* A pointer refers to a memory location that is freed. The pointer still refers to the same memory location even though the memory has been freed.
    
    ```c
    int *ptr = malloc(sizeof(int));
    free(ptr); 
    
    // ptr is now a dangling pointer!
    ```
    
* A pointer refers to a local variable that has gone out of scope.
    
    ```c
    int *func() {
      int x = 5;  
      int *ptr = &x;  
      return ptr; 
    }
    
    // ptr now dangles as x is out of scope
    ```
    

### How to avoid dangling pointers

To avoid dangling pointers:

* Set pointers to NULL after freeing. This helps avoid accidental reuse.
    
    ```c
    free(ptr);
    ptr = NULL;
    ```
    
* Do not return pointers to local variables.
    
* Limit the scope of pointers as much as possible.
    

The consequences of dangling pointers are undefined behavior such as program crashes. Dereferencing a dangling pointer may access invalid memory locations.