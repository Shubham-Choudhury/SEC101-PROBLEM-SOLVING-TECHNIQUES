---
layout: base
title: "Lecture 11: Introduction to Structured Programming – Sequence, Selection, and Repetition"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/lecture-11-introduction-to-structured-programming-sequence-selection-and-repetition/"
---

# {{ page.title | escape }}

## 1. What is Structured Programming?

Structured Programming is a programming methodology in which a program is developed using well-defined control structures, such as:

- Sequence
- Selection
- Repetition

The goal is to improve:

- Readability
- Reliability
- Maintainability
- Debugging
- Testing

### # Characteristics of Structured Programming

A structured program should have the following characteristics:

- Simple and logical design.
- Uses only structured control statements.
- Avoids unnecessary GOTO statements.
- Divides the problem into modules.
- Easy to debug.
- Easy to test.
- Easy to maintain.
- Easy to modify.

### # Advantages of Structured Programming

| Advantage       | Explanation                                     |
| --------------- | ----------------------------------------------- |
| Readability     | Code is easier to understand.                   |
| Maintainability | Changes can be made easily.                     |
| Debugging       | Errors are easier to locate.                    |
| Reusability     | Modules can be reused.                          |
| Testing         | Individual modules can be tested independently. |
| Reliability     | Produces more dependable software.              |

## 2. Control Structures

Every structured program is built using only three basic control structures.

<ol type="I">
<li>Sequence</li>
<li>Selection</li>
<li>Repetition</li>
</ol>

According to the **Structured Program Theorem (Böhm–Jacopini Theorem)**, any algorithm can be expressed using combinations of these three control structures.

## I. Sequence Structure

A Sequence is the simplest control structure. Statements execute one after another in the order they appear. No decision is made. No repetition occurs.

#### **Example:** Add two numbers

Program:

```c
#include <stdio.h>

int main(){
    int a = 10;
    int b = 20;

    int sum = a + b;

    printf("The sum of %d and %d is %d\n", a, b, sum);

    return 0;
}
```

## II. Selection Structure

A Selection Structure allows the program to choose one of multiple paths based on a condition. Also called Decision Structure or Conditional Structure.

### # Types of Selection:

1. Single Selection:

   ```
   IF Condition
       Statement
   ```

   Example: `Find whether a number is positive`

   ```c
    #include <stdio.h>

    int main(){
        int num = 10;

        if(num > 0){
            printf("The number is positive.");
        }

        return 0;
    }
   ```

2. Double Selection

   ```
   IF Condition

       Statement 1

   ELSE

       Statement 2
   ```

   Example: `Find whether a number is positive or not`

   ```c
    #include <stdio.h>

    int main(){
        int num = 10;

        if(num > 0){
            printf("The number is positive.");
        }
        else{
            printf("The number is not positive.");
        }

        return 0;
    }
   ```

3. Multiple Selection

   ```
   IF
       Statement 1
   ELSE IF
       Statement 2
   ELSE IF
       Statement 3
   .
   .
   .
   ELSE
       Statement n
   ```

   Example: `Find whether a number is positive or negative or zero`

   ```c
   #include <stdio.h>

   int main(){
       int num = 10;

       if(num > 0){
           printf("The number is positive.");
       }
       if(num < 0){
           printf("The number is negative.");
       }
       else{
           printf("The number is zero.");
       }

       return 0;
   }
   ```

### # Characteristics of Selection

- Uses conditions.
- Executes only one path.
- Makes decisions.
- Increases program flexibility.

## III. Repetition Structure

A Repetition Structure executes one or more statements repeatedly until a specified condition is satisfied. Also called: Loop or Iteration

### # Characteristics of Repetition

- Executes statements multiple times.
- Reduces code duplication.
- Improves efficiency.
- Controlled by conditions.

### # For Loop:

#### **Syntax**

```c
for (initialization; condition; update)
{
    // Statements to execute
}
```

or

```c
for (expression; expression; expression)
{
    // Statements to execute
}
```

#### **Example 1:** Print numbers from 1 to 5

```c
#include <stdio.h>

int main()
{
    int i;

    for (i = 1; i <= 5; i=i+1)
    {
        printf("%d\n", i);
    }

    return 0;
}
```

#### **Example 2:** Count down from 5 to 1

```c
#include <stdio.h>

int main()
{
    int i;

    for (i = 5; i >= 1; i=i-1)
    {
        printf("%d\n", i);
    }

    return 0;
}
```

### # While Loop

#### **Syntax**

```c
while (condition)
{
    // Statements to execute
}
```

#### **Example:** Print numbers from 1 to 5

```c
#include <stdio.h>

int main()
{
    int i = 1;

    while (i <= 5)
    {
        printf("%d\n", i);
        i++;
    }

    return 0;
}
```
