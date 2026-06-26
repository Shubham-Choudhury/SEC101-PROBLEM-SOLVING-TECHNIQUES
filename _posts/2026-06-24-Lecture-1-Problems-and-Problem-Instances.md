---
layout: base
title: "Lecture 1: Problems and Problem Instances"
date: 2026-06-24 00:00:00 +0530
categories: jekyll update
permalink: "/lecture-1-problems-and-problem-instances/"
---

# {{ page.title | escape }}

## 1. What is a Problem?

A problem is a task or objective that requires a solution.

In computer science, a problem is a general description of a task that specifies:

- What information is given (Input)
- What result is expected (Output)

**Definition**: A problem is a computational task that transforms input into output according to a set of rules.

#### **Example 1:** Addition

Problem: Add two numbers.

Input: `Two numbers A and B`

Output: `Sum of A and B`

#### **Example 2:** Largest Number

Problem: Find the largest among three numbers.

Input: `Three numbers`

Output: `Largest number`

## 2. Characteristics of a Good Problem Statement

A well-defined problem should clearly specify:

1. Input: Data supplied to the system.

   Example:

   ```
   Roll Number
   Marks
   Age
   ```

2. Output: Expected result.

   Example:

   ```
   Grade
   Average
   Maximum value
   ```

3. Constraints: Conditions that inputs must satisfy.

   Example:

   ```
   Marks must be between 0 and 100
   ```

#### **Example**

Problem: `Find square root of a number.`

Input: `A positive number`

Output: `Square root`

Constraint: `Number ≥ 0`

## 3. What is a Computational Problem?

A computational problem is a problem that can be solved by a computer through a sequence of steps.

Computers cannot understand vague instructions such as: `Make me happy` or `Write something beautiful`, because they lack precise input-output specifications. Computational problems must be clearly defined.

#### **Example:**

Problem: `Calculate factorial of a number.`

Input: `Integer n`

Output: `n!`

## 4. Problem vs Solution

The problem tells us what needs to be done. The solution tells us how it will be done.

#### **Example:**

Problem: `Find largest among three numbers.`

Solution: `Compare numbers and return the maximum.`

## 5. What is a Problem Instance?

A problem instance is a specific example of a problem obtained by supplying actual input values.

**Definition:** A problem instance is a particular case of a problem with concrete input data.

#### **Example 1:**

Problem: `Add two numbers.`

Problem Instances:

```
5 + 10
100 + 250
7 + 3
```

All are different instances of the same problem.

#### **Example 2:**

Problem: `Find maximum among three numbers.`

Instances:
```
10, 20, 15
50, 12, 7
90, 90, 20
```