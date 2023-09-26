---
title: "Recursion"
seoTitle: "Complete Guide to Recursion in C | Recursive Functions and Types"
seoDescription: "Recursive functions, base cases, recursive calls, types of recursion like direct, indirect, tail, non-tail and nested recursion"
datePublished: Tue Sep 26 2023 06:30:09 GMT+0000 (Coordinated Universal Time)
cuid: clmzxu70v000909lc85sra1cb
slug: recursion
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1695693811228/5675d87d-08b2-4c0a-8acd-7a908e3dabe3.gif
tags: c, recursion, recursion-types

---

# Recursion

Recursion is a technique where the solution to a problem depends on solutions to smaller instances of the same problem.

Recursion has two cases:

1. Base Case
    
2. Recursion Case
    

Example:  
The sum of the first n natural numbers  

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695694752283/ea8f5d27-a2dd-4105-9cae-8d3dad5068ac.png align="center")

### **Base Case**

The base case is a condition that stops the recursion by returning a value. It is needed to avoid infinite recursion.

For example, in a factorial function:

```c
  if (n == 1) { 
     return 1;  // base case
  }
```

The base case returns the factorial of 1, which is 1.

### **Recursive Call**

The recursive call is where the function calls itself, passing new input that moves closer to the base case.

For example, in a factorial function:

```c
  return n * factorial(n-1);  // recursive call
```

Each recursive call pushes a new stack frame onto the call stack. This contains:

* Function parameters
    
* Local variables
    
* Return address
    

When the base case is reached, stack frames start popping and the return values are combined.

## **What is a Recursive Function?**

A recursive function is a function that calls itself during its execution. It has the following phases:

* Winding Phase
    
* Unwinding phase
    

### **The Winding Phase**

The winding phase is when recursive calls are made by passing smaller inputs.

In this phase:

* New stack frames are pushed onto the call stack for each recursive call
    
* Local variables are initialized
    
* Function parameters are passed
    

For example:

```c
  factorial(5);  // First call

  factorial(4);  // Second call, winding phase continues

  factorial(3);  
  factorial(2);
  factorial(1); // Base case reached
```

### **The Unwinding Phase**

The unwinding phase is when the base case is reached and return values start getting combined.

In this phase:

* Stack frames start popping off the call stack
    
* Return values from each recursive call are combined
    

For example:

```c
  return 1; // Base case returns 1

  return 2 * 1 = 2;  
  return 3 * 2 = 6;
  return 4 * 6 = 24;
  return 5 * 24 = 120; // Final result
```

## **Types of Recursion**

There are different types of recursion based on how the recursive call is used:

1. Direct Recursion
    
2. Indirect Recursion
    
3. Tail Recursion
    
4. Non-Tail Recursion
    
5. Excessive Recursion
    
6. Nested Recursion
    

### **Direct Recursion**

In direct recursion, a function calls itself directly. This is the simplest form of recursion.

For example, the factorial function uses direct recursion:

```c
  int factorial(int n) {
     if (n == 1)  
         return 1;
     return n * factorial(n - 1);  
  }
```

Here, `factorial()` calls itself directly.

When this function is called as `factorial(5)`, the following happens:

```plaintext
  factorial(5) calls factorial(4) 
  factorial(4) calls factorial(3)
  factorial(3) calls factorial(2)
  factorial(2) calls factorial(1) 
  factorial(1) returns 1
  factorial(2) returns 2 
  factorial(3) returns 6
  factorial(4) returns 24
  factorial(5) returns 120
```

The base case is needed to stop infinite recursion:

```c
  if (n == 1)  
       return 1;  // base case
```

### **Indirect Recursion**

In indirect recursion, two or more functions call each other recursively. This is also known as mutual recursion.

For example:

```c
  void func1() {
     // some statements
     func2();
  }

  void func2() {
     // some statements
     func1(); 
  }
```

Here, `func1()` calls `func2()` and `func2()` calls `func1()`. They recursively call each other, hence the name indirect recursion.

When `func1()` is first called:

* `func1()` calls `func2()`
    
* `func2()` then calls `func1()`
    
* `func1()` again calls `func2()`
    
* And so on...
    

Both functions share the same call stack.

Base cases are needed for both functions:

```c
  void func1() {
     if(some_base_case) return;
     func2();
  }

  void func2() {
     if(some_other_base_case) return;
     func1();
  }
```

### Tail Recursion

Tail recursion is a type of recursion where the recursive call is the last thing the function does before returning.

This means there is no operation after the recursive call, before returning the result.

For example:

```c
  int factorial(int n) {
     if (n == 1)  
         return 1;
     int result = n * factorial(n-1);
     return result;  
  }
```

Here, the recursive call `factorial(n-1)` is the last thing before returning the result.

### Non-Tail Recursion

Non-tail recursion is when the recursive call is not the last thing the function does before returning.

There are operations after the recursive call, before returning the result.

For example:

```c
  int factorial(int n) {
     if (n == 1)  
         return 1;
     int result = factorial(n-1);
     result = n * result;  
     return result;
  }
```

Here, after the recursive call `factorial(n-1)`, there is an operation `result = n * result` before returning the result.

### Excessive Recursion

Excessive recursion occurs when the recursion depth becomes too large, leading to stack overflow.

Reasons for excessive recursion:

* No base case condition
    
* Base case condition not met soon enough
    
* Very large input size
    

Symptoms of excessive recursion:

* Stack overflow error
    
* Program crash
    

For example:

```c
  int factorial(int n) {
     return n * factorial(n-1); 
  }
```

This has no base case, so for any input, it will recurse indefinitely, eventually causing a stack overflow.

### Nested Recursion

Nested recursion occurs when a recursive function calls another recursive function. This creates a nested stack of function calls.

For example:

```c
  int nestedRecursion(int n) {
     if (n == 1)  
        return 1;
     return n + nestedRecursion(n-1);
  }

  int main() {
     int result = nestedRecursion(5); 
     return 0;
  }
```

Here `nestedRecursion()` calls itself recursively. When `n` becomes 1, the base case is met and it returns 1.

The stack frame would look like this:

```plaintext
  main()
     nestedRecursion(5)
        nestedRecursion(4)
           nestedRecursion(3)
              nestedRecursion(2)
                 nestedRecursion(1)
```

## **Advantages and Disadvantages**

### **Pros**

1. An elegant and simple solution for recursive problems. It models the recursive nature of the problem nicely.
    
2. Modular - Recursive functions can break down complex problems into smaller sub-problems, making the code modular.
    
3. Easy to implement and debug.
    

### **Cons**

1. Excessive recursion can cause stack overflow for large inputs. This limits the maximum problem size that can be solved.
    
2. Performance issues - Each recursive call has an overhead for pushing function parameters and return addresses onto the stack. This adds up for deeper recursions.
    
3. Space issues - Each recursive call uses stack space until the function returns. This can be a problem for deeply nested recursions.
    
4. Difficult to optimize - Recursive solutions are often harder to optimize for performance compared to iterative solutions.
    
5. Non-intuitive for beginners - Recursive solutions can be difficult for beginners to understand and follow.
    
6. Potential for infinite recursion bugs - If the base case is missing, recursion will never terminate.