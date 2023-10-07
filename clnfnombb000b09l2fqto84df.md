---
title: "Strings"
seoTitle: "A Complete Guide to Strings | String Functions, Pointers & Arrays"
seoDescription: "String constants, Library functions, Pointers to Strings, Multidimensional Strings, Passing Strings to Functions and Arrays of String Pointers"
datePublished: Sat Oct 07 2023 06:30:12 GMT+0000 (Coordinated Universal Time)
cuid: clnfnombb000b09l2fqto84df
slug: strings
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1696658115733/4c2289d8-8bb4-4bbe-ad79-d65032b49409.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1696658358555/719904ec-2852-4a0f-bafd-44b5949b3330.png
tags: strings, 2articles1week, multidimensional-strings, string-pointers, array-of-pointers

---

## String Constants:

String constants are declared using double quotes. They are initialized with the string literal inside the quotes. Individual characters within a string constant can be accessed using the \[\] operator. String constants are immutable and stored in read-only memory.

Eg.  
"Programming", "Data Structures"

## String:

![C - Strings](https://www.tutorialspoint.com/cprogramming/images/string_representation.jpg align="center")

### Declaring strings

Strings can be declared using character arrays:

```c
  char name[20];   // character array of size 20
```

### Initializing strings

Strings can be initialized using:

* String literal:
    
    ```c
    char name[] = "John";
    ```
    
* Character array:
    
    ```c
    char name[] = {'J', 'o', 'h', 'n', '\0'};
    ```
    

The null character '\\0' is required to indicate the end of the string.

### Accessing Characters

Individual characters can be accessed using the \[\] operator:

```c
  char first = name[0];   // 'J'
  char last = name[3];   // 'n'
```

### Example

```c
  #include <stdio.h>

  int main() {

    char string[100];

    // Taking string as input using scanf() 
    printf("Enter a string: "); 
    scanf("%s", string);

    // Printing string using printf()  
    printf("You entered: %s\n", string);  

    // Taking string as input using gets() 
    printf("Enter another string: ");
    gets(string);

    // Printing string using puts()
    puts(string);  

    // Initializing string  
    strcpy(string, "Hello");  

    // Printing string using while loop
    int i = 0; 
    while (string[i] != '\0') {
        printf("%c", string[i]); 
        i++;
    }
    printf("\n");

    return 0;
  }
```

## String Library Functions:

The string library functions make it easy to perform common string operations in C like copying, concatenating, comparing, searching and manipulating strings.

**strlen()** - Returns the length of a string

```c
  int len = strlen(string);
```

**strcpy()** - Copies one string to another

```c
  strcpy(dest, source);
```

**strcat()** - Concatenates two strings

```c
  strcat(string1, string2);
```

**strcmp()** - Compares two strings

```c
  int result = strcmp(string1, string2);
```

**strchr()** - Finds the first occurrence of a character in a string

```c
  char *p = strchr(string, 'c');
```

**strstr()** - Finds the first occurrence of a substring

```c
  char *p = strstr(string, "sub");
```

**Example:**

```c
  char str1[20] = "Hello";
  char str2[20] = "World";

  int len = strlen(str1);   
  // len = 5

  strcpy(str1, str2);       
  // str1 = "World"

  strcat(str1, str2);       
  // str1 = "WorldWorld"

  int result = strcmp(str1, str2);  
  // result < 0 as str1 is lexicographically less than str2

  char *p = strchr(str1, 'r');
  // p points to the first occurrence of 'r' in str1

  char *p = strstr(str1, "orl");
  // p points to the first occurrence of "orl" in str1
```

## String Pointers:

### Declaring string pointers

A string pointer is declared just like any other pointer but it points to a string (array of characters).

```c
  char *str;
```

### Initializing string pointers

A string pointer can be initialized in two ways:

1. Pointing to a string literal:
    
    ```c
    char *str = "Hello";
    ```
    
2. Pointing to an array name:
    
    ```c
    char array[100];
    char *str = array;
    ```
    

### Example

```c
  #include <stdio.h>

  int main() {

    char *str = "Hello"; 

    printf("Length: %d\n", strlen(str));

    char array[100]; 
    char *ptr = array;

    printf("Enter a string: ");
    gets(array);  

    printf("You entered: ");
    puts(ptr);

    strcpy(ptr, "How are you?");
    printf("%s\n", ptr);

    char *sub = strstr(ptr, "are");
    printf("%s\n", sub); 

    char *ch = strchr(ptr, 'u');
    printf("%c", *ch);

    return 0;
  }
```

## Multidimensional String Arrays:

2D Character arrays can be used to store strings.

For eg.

```c
char names[4][20] = {"Mathematics", "Algorithms", "Programming", "TOC"} 
```

## Passing Strings to Functions:

### Passing string constants

We can pass string constants to functions like this:

```c
  void printString(char* str){
    printf("%s", str);
  }

  int main(){
    printString("Hello");  
  }
```

Here we are passing the string literal "Hello" to the printString() function.

### Passing character arrays

We can also define a character array and pass it to a function:

```c
  #include <stdio.h>
  void printString(char str[]){
    printf("%s", str);  
  }

  int main(){
    char str[6] = "Hello";
    printString(str); 
    return 0;   
  }
```

Here we are passing the character array `str` to the function.

### Passing string pointers

```c
  #include <stdio.h>

  void printString(char *str){
    printf("%s", str);
  }

  int main(){
    char *str = "Hello";
    printString(str);    
  }
```

## Array of String Pointers:

### Declaring an array of string pointers

We declare an array of string pointers like this:

```c
  char *strings[n];
```

Here `strings` is an array of `n` string pointers.

### Initializing array of string pointers

We can initialize an array of string pointers like this:

```c
  char *strings[3] = {"Hello", "World", "C"};
```

Here we are initializing the string pointers to point to string literals.

### Accessing elements

We access elements of an array of string pointers using the \[\] operator:

```c
  printf("%s", strings[0]); // Prints Hello
  printf("%s", strings[1]); // Prints World
```

### Example

```c
  #include <stdio.h>

  int main() {
    char *strings[3];

    strings[0] = "Hello";
    strings[1] = "World"; 
    strings[2] = "C";

    for (int i = 0; i < 3; i++)
      printf("%s\n", strings[i]); 

    return 0;
  }
```

Output:

```plaintext
  Hello  
  World
  C
```