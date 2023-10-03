---
title: "Arrays"
seoTitle: "A Complete Guide to Arrays in C | 1D, 2D & 3D Arrays with Examples"
seoDescription: "Arrays, including 1D, 2D and 3D arrays, pointers to arrays, passing arrays to functions and function pointers."
datePublished: Tue Oct 03 2023 06:30:09 GMT+0000 (Coordinated Universal Time)
cuid: cln9xx5we000109jrfok891oe
slug: arrays
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1696312100769/93f77c93-c435-4f29-9dfe-6fc7b8f91da7.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1696312192959/9e3031a5-73eb-4f95-bb3c-a37cec7331c2.png
tags: c, pointers, arrays, multi-dimensional-arrays, function-pointers

---

## 1D Arrays:

### Declaration and initialization of 1D arrays

1D arrays store a collection of similar type data elements using a single name.

Declaration:

`type array_name[size];`

Where `type` is the data type of the elements and `size` is the total number of elements.

Initialization:

```c
  int marks[5] = {34, 45, 78, 90, 98};
  float prices[4] = {10.5, 20.2, 30.1, 40.0};  
  char names[6] = {'J','o','h','n',' ','D'};
```

### Accessing array elements

Accessing Elements:

Elements are accessed using a subscript (index number) within square brackets `[ ]`. The index starts from 0.

`array_name[subscript]`

```c
  marks[0]  // 34
  marks[1]  // 45
  marks[4]  // 98
```

### Examples:

```c
  int roll_nos[20];  

  char names[5][20]; 

  float temp[10] = {98.6, 99.2, 100.4, 101.0};
```

* Arrays are stored in contiguous memory locations.
    
* The variable name itself represents the base address of the array.
    
* Arrays have a static size that needs to be specified during declaration.
    
* The size of an array must be an integer constant.
    

## Pointers to Arrays:

### Declaring a pointer to an array

A pointer to an array is a variable that stores the base address of an array.

Declaring:

`type *ptr_name = array_name;`

Where `type` is the element type of the array.

Example:

```c
  int marks[5] = {10, 20, 30, 40, 50};

  int *ptr = marks; // ptr points to the first element of marks array
```

Here `ptr` is a pointer to an array of integers that stores the base address of `marks` array.

### Accessing array elements

We can access array elements using:

1. Subscript `[ ]`  
    `marks[i]`
    
2. Pointer arithmetic `*` and `+` `*(ptr + i)`
    

Both are equivalent and yield the `i-th` element.

```c
  marks[0] == 10
  *(ptr + 0) == 10

  marks[1] == 20  
  *(ptr + 1) == 20

  marks[2] == 30
  *(ptr + 2) == 30
```

### Example

```c
  #include <stdio.h>

  int main() {
     int marks[5] = {10, 20, 30, 40, 50};

     int *ptr = marks;  // ptr points to the first element of marks array

     // Accessing elements using subscript    
     printf("Element at index 0: %d\n", marks[0]);
     printf("Element at index 1: %d\n", marks[1]);

     // Accessing elements using pointer arithmetic
     printf("Element at index 0: %d\n", *ptr);
     printf("Element at index 1: %d\n", *(ptr + 1));

     // Traversing the array using pointers
     for (int i = 0; i < 5; i++) {
         printf("%d ", *(ptr + i));
     }   

     return 0;
  }
```

Output:

Element at index 0: 10  
Element at index 1: 20 Element at index 0: 10  
Element at index 1: 20  
10 20 30 40 50

## 2D Arrays:

### Declaration

A 2D array is declared as:

`type array_name[row_size][col_size];`

Where `type` is the data type of elements and `row_size` and `col_size` are the number of rows and columns respectively.

### Initialization

2D arrays can be initialized in two ways:

1. Using Initializer List:
    
    ```c
    int marks[2][3] = {
      {34, 45, 78},
      {90, 98, 67}  
    };
    ```
    
2. Using a For Loop:
    
    ```c
    int numbers[3][4];
    
    for (int i = 0; i < 3; i++) {
      for (int j = 0; j <4; j++) {
          numbers[i][j] = i*j;
      } 
    }
    ```
    

### Accessing elements

Elements are accessed using two subscripts - one for the row and one for the column.

`array_name[row][column]`

Example:

```c
  marks[0][1]  // 45
  marks[1][2]  // 67
```

### Example

Adding Two Matrices:

```c
#include <stdio.h>

int main() 
{
   int r, c, i, j;

   printf("Enter rows and columns: ");
   scanf("%d %d", &r, &c);

   int a[r][c], b[r][c], sum[r][c];

   printf("Enter elements of first matrix: \n"); 
   for (i = 0; i < r; i++)
       for (j = 0; j < c; j++)
           scanf("%d", &a[i][j]);

   printf("Enter elements of second matrix: \n");    
   for (i = 0; i < r; i++)    
       for (j = 0; j < c; j++)      
           scanf("%d", &b[i][j]);

   for (i = 0; i < r; i++) {
       for (j = 0; j < c; j++) {
           sum[i][j] = a[i][j] + b[i][j];
       }
   }

   printf("Sum of the matrices: \n");
   for (i = 0; i < r; i++) {
       for (j = 0; j < c; j++) {
           printf("%d ", sum[i][j]);    
       }
       printf("\n");
   }   
}
```

OUTPUT:

```c
Enter rows and columns: 2 2  
Enter elements of first matrix:
1 2  
3 4
Enter elements of second matrix:    
4 3
2 1

Sum of the matrices:

5 5     
5 5
```

## 3D Arrays:

### Declaration

A 3D array is declared as:

`type array_name[x][y][z];`

Where `type` is the data type of elements and `x`,`y` and `z` are the number of elements in the first, second and third dimensions respectively.

### Initialization

3D arrays can be initialized using initializer lists:

```c
  int marks[2][3][4] = {
      {   
          {1, 2, 3, 4},
          {5, 6, 7, 8},  
          {9, 10, 11, 12}  
      },
      {
          {13, 14, 15, 16}, 
          {17, 18, 19, 20},
          {21, 22, 23, 24}   
      }
  };
```

### Accessing elements

Elements are accessed using three subscripts - one for each dimension.

`array_name[x][y][z]`

Example:

```c
  marks[0][1][2] // 11  
  marks[1][2][3] // 24
```

### Example

```c
  #include <stdio.h>

  int main() {
      int marks[2][3][4] = { ... };

      printf("Element at 0 1 2 is %d", marks[0][1][2]);
  }
```

## Passing Arrays to Functions:

### Passing 1D Arrays:

A 1D array can be passed to a function like this:

```c
  void func(int array[]) {
      // array used here
  }

  int main() {
      int array[5] = {1, 2, 3, 4, 5};

      func(array); 
  }
```

The array name acts as a pointer to its first element. So the function receives a pointer to the first element of the array, not a copy of the whole array.

### Passing 2D Arrays:

A 2D array is passed as:

```c
  void func(int array[][]) {
      // array used here
  }

  int main() {
      int array[3][4] = { ... };

      func(array);
  }
```

Again, the array name acts as a pointer to the first element. The second dimension size can be omitted.

### Passing 3D Arrays:

A 3D array is passed similarly:

```c
  void func(int array[][][]) {
      // array used here
  }

  int main() {
      int array[2][3][4] = { ... };

      func(array); 
  }
```

### Example:

```c
  void sum(int array[][3], int rows) {
      int sum = 0;

      for (int i = 0; i < rows; i++) {
          for (int j = 0; j < 3; j++) {
              sum += array[i][j];   
          }    
      }

      printf("Sum is %d", sum);
  }

  int main() {
      int array[2][3] = { ... };

      sum(array, 2); 
  }
```

## Function Pointers:

### Declaring function pointers

A function pointer is declared as:

`return_type (*function_pointer_name)(arguments);`

For example:

```c
  int (*sum)(int, int); // pointer to a function that returns an int and has 2 int parameters
```

### Defining and initializing function pointers

A function pointer can be initialized to point to an actual function:

```c
  int sum(int a, int b){
      return a + b;
  }

  int main(){
      int (*sum_ptr)(int, int) = &sum;  // initialize pointer to point to sum()
  }
```

### Calling functions using pointers

The function is called using the pointer:

```c
  int result = sum_ptr(10, 20);
```

This calls the `sum()` function.

### Example program

```c
  int sum(int a, int b) { ... }
  int multiply(int a, int b) { ... }

  int main() {
      int (*func_ptr)(int, int);

      func_ptr = sum; 
      func_ptr(10, 20);  // Calls sum()

      func_ptr = multiply;
      func_ptr(10, 20);  // Calls multiply()
  }
```