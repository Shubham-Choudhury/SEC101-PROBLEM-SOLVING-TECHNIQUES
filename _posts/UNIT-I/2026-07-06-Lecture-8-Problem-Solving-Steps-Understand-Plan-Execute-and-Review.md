---
layout: base
title: "Lecture 8: Problem-Solving Steps – Understand, Plan, Execute, and Review"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/lecture-8-problem-solving-steps-understand-plan-execute-and-review/"
---

# {{ page.title | escape }}

## 1. Problem-Solving Process

The standard problem-solving process consists of four major steps.

```
Understand the Problem
          ↓
Plan the Solution
          ↓
Execute the Plan
          ↓
Review and Improve
```

Each step is equally important. Skipping any step may result in incorrect or inefficient solutions.

## **Step 1:** Understand the Problem

The first step is to clearly understand what needs to be solved.

Many programming errors occur because programmers misunderstand the problem.

### # Questions to Ask

Before writing any algorithm, ask the following questions:

- What is the problem?
- What is the objective?
- What are the inputs?
- What outputs are expected?
- Are there any constraints?
- Are there exceptional cases?
- What assumptions can be made?

## **Step 2:** Plan the Solution

Once the problem is understood, we plan how to solve it.

### # Planning Includes

- Selecting an appropriate algorithm.
- Choosing suitable data structures.
- Dividing the problem into smaller parts.
- Preparing pseudocode.
- Drawing flowcharts.

#### **Example**

Problem: `Find the largest of three numbers.`

Possible plans:

- Plan A:

  Compare numbers one by one.

- Plan B:

  Store numbers in an array and search for the maximum.

Both work, but Plan A is simpler.

### # Choosing the Best Solution

Suppose there are three possible algorithms.

| Algorithm | Time Complexity |
| --------- | --------------- |
| A         | O(N²)           |
| B         | O(N log N)      |
| C         | O(N)            |

The best choice is Algorithm C, because it is the most efficient.

## **Step 3:** Execute the Plan

After planning, the next step is implementation. This involves converting the algorithm into a programming language.

#### **Example**

Algorithm:

```
Read two numbers.

Add them.

Print the sum.
```

Implementation in C:

```c
#include <stdio.h>

int main()
{
    int a, b;

    scanf("%d %d", &a, &b);

    printf("%d", a + b);

    return 0;
}
```

### # Testing During Execution

After implementation, test with:

- Normal inputs
- Boundary values
- Invalid inputs
- Large inputs

#### **Example**

Program: `Division`

Test cases:

| Input | Expected Output |
| ----- | --------------- |
| 10 2  | 5               |
| 5 0   | Error           |
| -20 4 | -5              |

## **Step 4:** Review and Improve

After execution, evaluate the solution. This is often called review, evaluation, or refinement.

### # Questions to Ask

- Is the output correct?
- Does the program work for all valid inputs?
- Is it efficient?
- Can memory usage be reduced?
- Can execution time be improved?
- Is the code readable?
- Is maintenance easy?

## Debugging

During review, programmers identify and fix errors.

### # Types of Errors:

1. Syntax Errors

   Example:

   ```c
   printf("Hello")
   ```

   Missing semicolon.

2. Logical Errors

   Example:

   ```c
   Average = Sum / 4;
   ```

   instead of

   ```c
   Average = Sum / 5;
   ```

   Program executes but gives incorrect results.

3. Runtime Errors

   Example:

   ```
   Division by zero
   ```

   Program crashes during execution.

## Optimization

After reviewing correctness, improve efficiency.

### # Possible improvements:

- Better algorithm
- Better data structure
- Remove unnecessary calculations
- Reduce memory usage
