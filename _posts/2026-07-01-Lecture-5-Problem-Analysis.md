---
layout: base
title: "Lecture 5: Problem Analysis"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/lecture-5-problem-analysis/"
---

# {{ page.title | escape }}

## 1. What is Problem Analysis?

**Definition:** Problem Analysis is the process of studying and understanding a problem before designing an algorithm or writing a program.

It involves identifying:

- Objectives
- Inputs
- Outputs
- Constraints
- Assumptions
- Requirements
- Possible solution approaches

### # Why is Problem Analysis Important?

Problem analysis helps us:

- Understand the actual problem.
- Avoid unnecessary work.
- Reduce programming errors.
- Choose the correct algorithm.
- Save development time and cost.
- Improve software quality.

#### **Example:**

Problem Statement: `"Write a program to calculate the average marks of five students."`

Before programming, ask:

- How many students? (5)
- How many subjects? (Not specified → clarification needed)
- What type of marks? (Integer or decimal?)
- What is the output format?

These questions are part of problem analysis.

## 2. Understanding the Problem Statement

The first step in problem analysis is to carefully read the problem statement.

Consider the following problem:

- "Write a program to calculate the simple interest."

What information is missing?

Possible questions:

- What inputs are required?
- What is the formula?
- Should decimal values be allowed?
- Should negative values be accepted?

Never assume missing information. Clarify the requirements whenever possible.

## 3. Identifying Inputs

Inputs are the data provided to the program. Without input, most programs cannot produce meaningful output.

#### **Example 1:** Addition Program

Inputs:

```
Number 1
Number 2
```

#### **Example 2:** Student Result Program

Inputs:

```
Roll Number
Marks
```

### Types of Inputs

| Input Type     | Example             | Value Example           |
| -------------- | ------------------- | ----------------------- |
| Integer        | Age, Marks          | 12, 52, 59              |
| Floating Point | Salary, Temperature | 12.56, 12.00, 85.9      |
| Character      | Grade               | 'A', 'B', 'e', 'R', '1' |
| String         | Name                | "Hello", "SXC"          |
| Boolean        | True/False          | 0, 1                    |

## 4. Identifying Outputs

Outputs are the results produced after processing the inputs.

#### **Example:** Addition Program

Output:

```
Sum
```

## 5. Identifying Constraints

Constraints are the conditions or limitations that the inputs or outputs must satisfy. Constraints ensure that the program works correctly within specified limits.

#### **Example 1:** Age

Constraint:

```
0 ≤ Age ≤ 120
```

#### **Example 2:** Marks

Constraint:

```
0 ≤ Marks ≤ 100
```

#### **Example 3:** Division

Constraint:

```
Denominator ≠ 0
```

### # Why Constraints Matter

Consider:

```
result = a / b;
```

If:

```
b = 0
```

The program will produce an error. Proper analysis helps identify such situations before implementation.

## 6. Assumptions

Sometimes a problem statement does not provide all the information. In such cases, reasonable assumptions may be made, but they should be clearly documented.

#### **Example:**

Problem:

```
Calculate employee salary.
```

Assumptions:

- Salary is monthly.
- Tax rate is fixed.
- All values are in Indian Rupees.

**Important Note:** Never make assumptions without documenting them, especially in software development.

## 7. Requirement Analysis

Requirement analysis is the process of determining exactly what the software must do.

It answers questions such as:

- What functions should the software perform?
- Who will use it?
- What data should be stored?
- What reports are required?

### # Functional Requirements

These describe what the system should do.

#### **Example:** Library System

- Add books
- Delete books
- Search books
- Issue books
- Return books

### # Non-functional Requirements

These describe how the system should perform.

#### **Examples:** Library System

- Fast response time
- Secure login
- User-friendly interface
- High reliability
- Low memory usage

## 8. Feasibility Analysis

Feasibility analysis determines whether the proposed solution is practical and achievable.

### # Types of Feasibility

- Technical Feasibility

  Can the required technology support the solution?

  **Example:** Can an old computer handle advanced AI software?

- Economic Feasibility

  Is the project affordable?

  **Example:** Should a small shop spend ₹50 lakh on software?

- Operational Feasibility

  Will users accept and use the system?

  **Example:** Can teachers easily use an online attendance system?

- Time Feasibility

  Can the project be completed within the available time?

  **Example:** Can a final-year project be completed in one semester?

## 9. Breaking Down Requirements

Large problems are easier to solve when divided into smaller tasks. This process is called **Problem Decomposition**.

#### **Example:** Student Management System

Instead of writing one large program, divide it into modules:

1. Add Student
2. Update Student
3. Delete Student
4. Search Student
5. Display Student List

Each module can be developed and tested independently.

### # Benefits

- Easier to understand.
- Easier to code.
- Easier to test.
- Easier to maintain.

## Problem Analysis Template

Whenever you receive a programming problem, analyze it using the following template:

| Component                   | Description                     |
| --------------------------- | ------------------------------- |
| Problem Statement           | What needs to be solved?        |
| Inputs                      | What data is required?          |
| Outputs                     | What results are expected?      |
| Constraints                 | What limitations exist?         |
| Assumptions                 | What assumptions are made?      |
| Functional Requirements     | What should the program do?     |
| Non-functional Requirements | How should the program perform? |
| Feasibility                 | Is the solution practical?      |
