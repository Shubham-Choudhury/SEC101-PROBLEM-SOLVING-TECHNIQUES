---
layout: base
title: "Lecture 9: Breaking Problems into Subproblems (Problem Decomposition)"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/lecture-9-breaking-problems-into-subproblems--problem-decomposition/"
---

# {{ page.title | escape }}

## 1. What is Problem Decomposition?

Problem Decomposition is the process of breaking a large and complex problem into smaller, simpler, and independent subproblems.

Each subproblem can be solved separately and later combined to solve the complete problem.

### # General Idea

```
Large Problem
      │
      ▼
Divide into Smaller Problems
      │
      ▼
Solve Each Subproblem
      │
      ▼
Combine Solutions
      │
      ▼
Complete Solution
```

## 2. Why Decompose a Problem?

- Easier understanding.
- Easier programming.
- Easier testing.
- Easier debugging.
- Easier maintenance.
- Better teamwork.

## 3. Functional Decomposition

Functional Decomposition means dividing a system according to its functions or operations. Each function performs one specific task.

#### **Example:** Calculator

Main Problem

```
Calculator
```

Subproblems

```
Addition()

Subtraction()

Multiplication()

Division()
```

Each function solves one small problem.

## 4. Top-Down Decomposition

Top-down decomposition starts with the complete problem and gradually divides it into smaller modules.

#### **Example:** Student Result System

Main Problem

```
Student Result Management
```

Smaller Problems:

```
Input Student Data

↓

Calculate Total

↓

Calculate Average

↓

Assign Grade

↓

Display Report
```

Each module can be developed separately.

## 5. Modular Programming

Modular Programming is a programming technique in which a program is divided into separate modules or functions.

Each module performs one well-defined task.

### # Characteristics of a Good Module

A good module should have the following properties.

1. Single Responsibility:

   One module should perform one task.

   Good:

   ```c
   CalculateAverage()
   ```

   Bad:

   ```c
   CalculateAverageAndPrintResultAndStoreData()
   ```

2. Independent

   One module should not unnecessarily depend on another. Independent modules are easier to test.

3. Reusable

   The module should be usable in different programs.

   Example:

   ```c
   SortArray()
   ```

   can be used in many projects.

4. Easy to Understand

   Module names should clearly indicate their purpose.

   Good:

   ```c
   FindMaximum()
   ```

   Poor:

   ```c
   Function1()
   ```

5. Small Size

   Smaller modules are easier to maintain.

### # Advantages of Modular Design

| Advantage        | Description                                     |
| ---------------- | ----------------------------------------------- |
| Simplicity       | Easier to understand                            |
| Reusability      | Modules can be reused                           |
| Easy Testing     | Test modules independently                      |
| Easy Debugging   | Errors are isolated                             |
| Maintainability  | Easy to update                                  |
| Team Development | Different programmers work on different modules |
