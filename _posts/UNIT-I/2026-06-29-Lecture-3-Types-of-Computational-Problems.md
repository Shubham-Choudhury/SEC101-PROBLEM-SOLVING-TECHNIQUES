---
layout: base
title: "Lecture 3: Types of Computational Problems"
date: 2026-06-29 08:50:00 +0530
categories: jekyll update
permalink: "/lecture-3-types-of-computational-problems/"
---

# {{ page.title | escape }}

## 1. What is a Computational Problem?

A computational problem is a problem that can be solved by a computer using a sequence of logical steps (an algorithm).

A computational problem consists of:

- **Input:** Data provided to the program.
- **Processing:** Operations performed on the input.
- **Output:** Desired result.

#### **Example**

Problem: `Find the largest number among three integers.`

Input: `10 25 15`

Output: `25`

## 2. Why Classify Problems?

Different problems require different solving techniques. Understanding the type of problem helps us choose the most suitable algorithm. Consider these examples:

| Problem                     | Best Technique |
| --------------------------- | -------------- |
| Find a word in a dictionary | Searching      |
| Arrange numbers             | Sorting        |
| Find shortest route         | Optimization   |
| Calculate GPA               | Arithmetic     |
| Check password              | Decision       |

## 3. Major Types of Computational Problems

There are five major categories commonly studied in computer science:

<ol type="I">
<li>Decision Problems</li>
<li>Search Problems</li>
<li>Optimization Problems</li>
<li>Counting Problems</li>
<li>Function (Computation) Problems</li>
</ol>

## I. Decision Problems

**Definition:** A Decision Problem is a computational problem where the answer is limited to Yes/No, True/False, or Accept/Reject.

The computer only decides whether a condition is satisfied.

#### **Example 1**

Problem: `Is the number prime?`

Input: `17`

Output: `YES`

#### **Example 2**

Problem: `Is the student eligible for an exam?`

Condition: `Attendance ≥ 75%`

Input: `Attendance = 82%`

Output: `YES`

#### **Algorithm Example**

```
Input Number

If Number is Even

    Print YES

Else

    Print NO
```

Real-Life Applications:

- Login authentication
- CAPTCHA verification
- Fingerprint verification
- Loan approval
- Medical diagnosis (positive/negative)

## II. Search Problems

**Definition:** A Search Problem requires finding one or more objects satisfying certain conditions.

Instead of answering Yes or No, we must locate something.

#### **Example 1**

Problem: `Find student Roll No. 101.`

Input: `Roll Number`

Output: `Student Record`

#### **Example 2**

Problem: `Find a contact in a mobile phone.`

Input: `Name`

Output: `Phone Number`

Common searching algorithms include:

- Linear Search
- Binary Search
- Hash-based Search
- Graph Search

Real-Life Applications:

- Search engines
- Library management
- Contact lists
- Database queries
- GPS location search

## III. Optimization Problems

**Definition:** An Optimization Problem asks us to find the best solution among many possible solutions.

The best solution may mean:

- Minimum cost
- Maximum profit
- Shortest distance
- Fastest time
- Lowest energy consumption

#### **Example 1**

Problem: `Find the shortest route between two cities.`

Input:

```
City A
City B
```

Output: `Shortest path.`

#### **Example 2**

A company wants to maximize profit. Possible production plans exist. Find the one giving highest profit.

Real-Life Examples:

- Google Maps
- Airline scheduling
- Delivery route planning
- Network routing
- Investment planning

### **Why Optimization is Difficult**

Many optimization problems have thousands or even millions of possible solutions.

#### **Example:**

- Traveling Salesman Problem (TSP):

  Suppose a salesman visits 10 cities.

- Possible routes:

  More than 3.6 million possibilities.

The computer must determine the shortest one.

## IV. Counting Problems

A Counting Problem asks: `How many solutions exist?` Instead of finding one solution, we count all valid solutions.

#### **Example 1**

Problem: `How many students passed?`

Input: `Marks of students.`

Output: `Passed Students = 42`

#### **Example 2**

Problem: `How many paths exist from one city to another?`

Output: `25 possible paths`

Real-Life Applications:

- Combinatorics
- Cryptography
- Scheduling
- Statistics
- Probability

## V. Function (Computation) Problems

**Definition:** A Function Problem requires computing a specific output value from given inputs.

Most mathematical calculations belong to this category.

#### **Example 1**

Problem: `Addition`

Input: `15 20`

Output: `35`

#### **Example 2**

Problem: `Factorial`

Input: `5`

Output: `120`

Real-Life Applications:

- Scientific calculators
- Banking software
- Payroll systems
- Tax calculations
- GPA computation

## Comparison of Problem Types

| Problem Type | Main Objective                        | Example                   | Typical Output |
| ------------ | ------------------------------------- | ------------------------- | -------------- |
| Decision     | Determine whether a condition is true | Is 29 prime?              | Yes/No         |
| Search       | Find an item                          | Search Roll No. 101       | Student record |
| Optimization | Find the best solution                | Shortest route            | Best route     |
| Counting     | Count all valid solutions             | Number of passed students | Integer count  |
| Function     | Compute a value                       | Factorial of 5            | 120            |
