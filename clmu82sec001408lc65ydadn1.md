---
title: "C-Programming Statements"
seoTitle: "A Guide to C Statements|Expression, Compound, Control, Jump Statements"
seoDescription: "Different types of statements in the C programming language - expression statements, compound statements, control statements and jump statements"
datePublished: Fri Sep 22 2023 06:30:09 GMT+0000 (Coordinated Universal Time)
cuid: clmu82sec001408lc65ydadn1
slug: c-statements
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1695187642503/7de24c7e-4297-4d78-aa70-30eea861d556.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1695187723988/a01ca0a7-2f53-4b86-8ec2-4e908b775a74.png
tags: c, loops, if-else, control-flow, statements

---

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