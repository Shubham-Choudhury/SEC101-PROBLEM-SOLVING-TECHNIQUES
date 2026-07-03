---
layout: base
title: "Lecture 2: Generalization and Special Cases of Problems"
date: 2026-06-25 00:00:00 +0530
categories: jekyll update
permalink: "/lecture-2-generalization-and-special-cases-of-problems/"
---

# {{ page.title | escape }}

## 1. What is Generalization?

**Definition:** Generalization is the process of expanding a problem so that it can handle a broader range of inputs or situations.

A generalized problem represents a family of similar problems.

#### **Example 1:** Addition

Specific Problem: `Add 5 and 10`

Generalized Problem: `Add any two numbers`

Input: `A, B`

Output: `A + B`

#### **Example 2:** Area of Circle

Specific Problem: `Radius = 7`

Generalized Problem: `Find area for any radius r.`

Formula: `Area = πr²`

## 2. Why Generalize Problems?

Generalization provides:

1. Reusability: One solution can solve many instances.

   Example:

   ```
   Sort any list of numbers.
   ```

   instead of

   ```
   Sort exactly [5,4,3]
   ```

2. Scalability: The solution works for larger inputs.

   Example:

   ```
   Find maximum among N numbers.
   ```

   instead of

   ```
   Find maximum among 3 numbers.
   ```

3. Better Algorithm Design: Professional programmers design algorithms for generalized problems.

   Example:

   Google Search does not search only one webpage. It searches billions of webpages.

## 3. What is a Special Case?

**Definition:** A special case is a restricted or simplified version of a general problem.

It represents a smaller subset of the generalized problem.

#### **Example 1**

General Problem: `Add any two integers.`

Special Case: `Add 5 and 10.`

#### **Example 2**

General Problem: `Find factorial of any positive integer.`

Special Case: `Find factorial of 5`

## 3. Generalization in Programming

Consider this program:

### Non-Generalized

```c
printf("%d", 5 + 10);
```

Output:

```
15
```

Only works for one case.

### Generalized

```c
int a, b;
scanf("%d%d",&a,&b);
printf("%d",a+b);
```

Now it works for:

```
2 + 3
10 + 20
100 + 500
```

without changing the program.

## 4. Generalization and Algorithm Design

Algorithms should solve the general problem.

### Problem

```
Find maximum number.
```

### Special Case Algorithm

```
Input A,B,C

Max = A

If B > Max
   Max = B

If C > Max
   Max = C
```

Works only for 3 numbers.

### Generalized Algorithm

```
Input N numbers

Max = First Number

For each remaining number
    If number > Max
         Max = number

Display Max
```

Works for any number of inputs.

## 5. Advantages of Studying Special Cases

Sometimes special cases are easier to solve.

Studying special cases helps us:

- Understand the larger problem.
- Test algorithms.
- Debug solutions.
