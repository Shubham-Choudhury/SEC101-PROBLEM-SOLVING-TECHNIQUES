---
layout: base
title: "Lecture 6: Solution Approaches and Algorithm Development"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/lecture-6-solution-approaches-and-algorithm-development/"
---

# {{ page.title | escape }}

## 1. What is a Solution Approach?

A solution approach is the strategy or method used to solve a computational problem.

### General Problem-Solving Process

![General Problem-Solving Process]({{ '/assets/images/General-Problem-Solving-Process.png' | relative_url }})

## 2. Common Solution Approaches

<ol type="I">
<li>Top-Down Design</li>
<li>Bottom-Up Design</li>
<li>Brute Force Method</li>
<li>Divide and Conquer</li>
<li>Greedy Method</li>
<li>Dynamic Programming</li>
</ol>

## I. Top-Down Design

Top-down design starts with the overall problem and gradually breaks it into smaller, manageable subproblems.

This process is also known as stepwise refinement.

### Steps

```
Main Problem
      ↓
Subproblem 1
Subproblem 2
Subproblem 3
      ↓
Smaller Tasks
```

#### **Example:** Student Management System

Main Problem:

```
Manage Student Records
```

Break into modules:

```
a. Add Student
b. Search Student
c. Update Student
d. Delete Student
f. Display Student List
```

Each module can then be divided further.

### Advantages

- Easy to understand.
- Modular design.
- Easier debugging.
- Easier maintenance.
- Suitable for large software projects.

### Disadvantages

- Requires careful planning.
- May delay implementation until the complete design is finished.

## II. Bottom-Up Design

Bottom-up design starts by developing small, reusable components and then combines them to build the complete system.

#### **Example:**

Develop individual functions:

```
Calculate Grade()
Calculate GPA()
Display Result()
Store Student Data()
```

Then combine them into:

```
Student Result Management System
```

### Advantages

- Encourages code reuse.
- Individual modules can be tested independently.
- Easier maintenance.

### Disadvantages

- Overall system design may be difficult initially.
- Integration may require additional effort.

## Top-Down vs Bottom-Up

| Top-Down                     | Bottom-Up                    |
| ---------------------------- | ---------------------------- |
| Starts from the whole system | Starts from small modules    |
| Decomposition                | Composition                  |
| Focus on overall design      | Focus on reusable components |
| Better for planning          | Better for implementation    |

## III. Brute Force Approach

The brute force approach solves a problem by trying all possible solutions until the correct one is found.

It is the simplest problem-solving strategy.

#### **Example:** Linear Search

Given:

```
[15, 8, 21, 6, 10]
```

Search for:

```
21
```

Method:

```
Compare:
15 ❌
8 ❌
21 ✅
```

### Advantages

- Easy to understand.
- Easy to implement.
- Always works if enough time is available.

### Disadvantages

- Very slow for large problems.
- May examine many unnecessary possibilities.

## IV. Divide and Conquer

Divide and Conquer is a strategy in which a large problem is divided into smaller independent subproblems.

Each subproblem is solved separately, and the solutions are combined.

### Steps

![Divide and Conquer Steps]({{ '/assets/images/Divide-and-Conquer-Steps.png' | relative_url }})

#### **Example:** Binary Search

Suppose the sorted list is:

```
10 20 30 40 50 60 70
```

Search for:

```
50
```

Step 1:

Check the middle element:

```
40
```

Since:

```
50 > 40
```

Ignore the left half.

Search only the right half:

```
50 60 70
```

Again, choose the middle element:

```
60
```

Now search:

```
50
```

Element found.

Instead of checking every element, Binary Search repeatedly divides the search space into halves.

### Applications

- Binary Search
- Merge Sort
- Quick Sort
- Matrix Multiplication
- Closest Pair of Points

### Advantages

- Faster than brute force.
- Efficient for large datasets.
- Reduces problem size quickly.

### Disadvantages

- Not suitable for every problem.
- Some algorithms require sorted data.

## V. Greedy Method

The Greedy Method makes the best possible choice at each step, hoping that these local decisions lead to the overall best solution.

#### **Example:** Coin Change

Suppose coins available are:

```
₹10
₹5
₹2
₹1
```

Amount:

```
₹18
```

Greedy solution:

```
₹10
₹5
₹2
₹1
```

Total:

4 coins

At each step, choose the largest coin that does not exceed the remaining amount.

### Applications

- Currency systems
- Minimum spanning tree
- Huffman coding
- Job scheduling
- Network routing

### Advantages

- Simple.
- Fast.
- Often produces excellent results.

### Disadvantages

- Does not always produce the optimal solution.
- Works only for specific classes of problems.

## VI. Dynamic Programming

Dynamic Programming (DP) is a technique used when a problem contains repeated subproblems.

Instead of solving the same subproblem multiple times, its result is stored and reused.

#### **Example:** Fibonacci Numbers

![Fibonacci Numbers]({{ '/assets/images/Fibonacci-Numbers.png' | relative_url }})

Notice: `F(3)` is calculated more than once.

Dynamic Programming stores the value of `F(3)` after computing it the first time and reuses it.

### Applications

- Fibonacci sequence
- Shortest path
- Knapsack problem
- Matrix chain multiplication
- Longest common subsequence

### Advantages

- Avoids repeated computations.
- Improves efficiency.
- Suitable for optimization problems.

### Disadvantages

- Requires additional memory.
- More complex to design than brute force.

## 3. What is an Algorithm?

An algorithm is a finite sequence of well-defined instructions used to solve a computational problem.

An algorithm accepts input, processes it, and produces the required output.

## 4. Characteristics of a Good Algorithm

A good algorithm should have the following properties:

1. **Input:** Accepts zero or more inputs.
2. **Output:** Produces at least one output.
3. **Definiteness:** Each step must be clear and unambiguous.
4. **Finiteness:** The algorithm must terminate after a finite number of steps. Infinite loops are not acceptable.
5. **Effectiveness:** Each instruction should be simple and executable.
6. **Correctness:** Produces the correct output for every valid input.
7. **Efficiency:** Uses minimum time and memory.

### Steps in Algorithm Development

![Steps in Algorithm Development]({{ '/assets/images/Steps-in-Algorithm-Development.png' | relative_url }})

### Example Algorithm

#### Problem

```
Find the largest of two numbers.
```

#### Algorithm

```
Step 1: Start

Step 2: Read A and B

Step 3: If A > B

            Max = A

        Else

            Max = B

Step 4: Display Max

Step 5: Stop
```

## 5. Representing Algorithms
Algorithms can be represented in three common ways:

### I. Natural Language

Example:
```
Read two numbers.
Add them.
Display the sum.
```

### II. Pseudocode

Example:
```
START

INPUT A, B

SUM ← A + B

PRINT SUM

STOP
```
Pseudocode resembles programming language but does not follow strict syntax rules.

### III. Flowchart

A flowchart is a graphical representation of an algorithm.

#### Basic Flowchart symbols:

![Basic Flowchart symbols]({{ '/assets/images/Basic-Flowchart-symbols.png' | relative_url }})

Example (Add Two Numbers):

![Add Two Numbers]({{ '/assets/images/Add-Two-Numbers.png' | relative_url }})