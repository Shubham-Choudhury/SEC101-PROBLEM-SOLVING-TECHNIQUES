---
layout: base
title: "Lecture 7: Analysis of Algorithms – Efficiency, Correctness, and Role of Data Structures"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/lecture-7-analysis-of-algorithms-efficiency-correctness-and-role-of-data-structures/"
---

# {{ page.title | escape }}

## 1. What is Algorithm Analysis?

Algorithm Analysis is the process of evaluating an algorithm to determine:

- How fast it runs.
- How much memory it uses.
- Whether it always produces the correct output.

### # Why is Algorithm Analysis Important?

Algorithm analysis helps us:

- Compare multiple algorithms.
- Reduce execution time.
- Reduce memory usage.
- Improve software performance.
- Design scalable applications.
- Solve large problems efficiently.

## 2. Measuring Algorithm Efficiency

Algorithm efficiency is mainly measured using two resources:

- Time
- Memory

Therefore, there are two important types of complexity:

- Time Complexity
- Space Complexity

## I. Time Complexity

Time Complexity measures how the running time of an algorithm increases as the input size increases.

It does not measure actual seconds. Instead, it measures the number of basic operations performed.

#### **Example 1:** Add two numbers

```
Read A
Read B

Add

Print
```

Number of operations remains almost constant.

Time Complexity:

```
O(1)
```

(Constant Time)

#### **Example 2:** Find the largest number in an array.

Suppose:

```
N = 5
```

Comparisons:

```
4
```

If

```
N = 1000
```

Comparisons:

```
999
```

Time increases with input size.

Time Complexity:

```
O(N)
```

### Common Time Complexities

| Complexity | Name         | Example                        |
| ---------- | ------------ | ------------------------------ |
| O(1)       | Constant     | Array indexing                 |
| O(log N)   | Logarithmic  | Binary Search                  |
| O(N)       | Linear       | Linear Search                  |
| O(N log N) | Linearithmic | Merge Sort                     |
| O(N²)      | Quadratic    | Bubble Sort                    |
| O(2ᴺ)      | Exponential  | Recursive subset generation    |
| O(N!)      | Factorial    | Brute-force Traveling Salesman |

## II. Space Complexity

Space Complexity measures the amount of memory required by an algorithm during execution.

Memory includes:

- Variables
- Arrays
- Function calls
- Temporary storage

#### **Example 1:** Add two numbers.

Variables:

```
A
B
SUM
```

Only three variables.

Space Complexity:

```
O(1)
```

#### **Example 2:** Store 1000 student marks.

Need an array of size:

```
1000
```

Space Complexity:

```
O(N)
```

### Time vs Space

| Time Complexity         | Space Complexity      |
| ----------------------- | --------------------- |
| Measures execution time | Measures memory usage |
| Faster is better        | Less memory is better |
| Depends on operations   | Depends on storage    |

## 3. Best, Average, and Worst Case Analysis

### # Best Case

The most favorable situation.

#### **Example:** Linear Search

Find:

```
10
```

Array:

```
10 20 30 40 50
```

Element found immediately.

Comparisons:

```
1
```

Best Case:

```
O(1)
```

### # Average Case

Typical performance over many possible inputs.

#### **Example:** Linear Search

Element found somewhere in the middle.

Average comparisons:

```
Approximately: N/2
```

Time Complexity:

```
O(N)
```

### # Worst Case

The least favorable situation.

#### **Example:** Linear Search

Search for:

```
50
```

Array:

```
10 20 30 40 50
```

or

Element not present.

Need to examine every element.

Time Complexity:

```
O(N)
```

## 4. Algorithm Correctness

An algorithm is correct if it produces the correct output for every valid input.

Correctness is more important than efficiency. A fast algorithm that gives wrong answers is useless.

### Conditions for Correctness

A correct algorithm should:

- Accept valid inputs.
- Follow the required logic.
- Handle boundary cases.
- Terminate properly.
- Produce correct output every time.

## 5. Role of Data Structures in Problem Solving

### # What is a Data Structure?

A Data Structure is a way of organizing and storing data so that it can be accessed and modified efficiently.

Algorithms and data structures work together: `Good algorithms require appropriate data structures.`

### # Why Are Data Structures Important?

They help to:

- Store data efficiently.
- Reduce execution time.
- Reduce memory usage.
- Simplify programming.
- Improve algorithm performance.

### Common Data Structures

| Data Structure | Description                                              |
| -------------- | -------------------------------------------------------- |
| Array          | Stores elements in contiguous memory locations.          |
| Linked List    | Dynamic collection of nodes connected by pointers.       |
| Stack          | Follows Last-In, First-Out (LIFO).                       |
| Queue          | Follows First-In, First-Out (FIFO).                      |
| Tree           | Hierarchical organization of data.                       |
| Graph          | Represents relationships between interconnected objects. |
| Hash Table     | Provides fast searching using key-value pairs.           |
