---
layout: base
title: "Lecture 4: Classification of Computational Problems"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/lecture-4-classification-of-computational-problems/"
---

# {{ page.title | escape }}

## 1. Classification of Computational Problems

Computational problems can be classified in many ways.

The most common classifications are:

<ol type="i">
    <li>Well-defined and Ill-defined Problems</li>
    <li>Structured and Unstructured Problems</li>
    <li>Simple and Complex Problems</li>
    <li>Deterministic and Non-deterministic Problems</li>
    <li>Static and Dynamic Problems</li>
</ol>

## **i-a. Well-defined Problems:**

A well-defined problem clearly specifies:

- Inputs
- Outputs
- Constraints
- Rules
- Goal

There is little or no ambiguity.

### Characteristics:

- Clear objective
- Clearly defined input
- Clearly defined output
- Fixed constraints
- Usually one correct answer

#### **Example 1: Addition**

Problem: `Add two integers.`

Input:

```
A = 10
B = 25
```

Output:

```
35
```

Everything is clearly defined.

#### **Example 2: Area of Rectangle**

Input:

```
Length
Width
```

Output:

```
Area = Length × Width
```

There is no ambiguity.

### Advantages of Well-defined Problems

- Easy to understand
- Easy to design algorithms
- Easy to test
- Easy to verify correctness

## **i-b. Ill-defined Problems**

An ill-defined problem lacks one or more of the following:

- Clear input
- Clear output
- Clear rules
- Clear constraints

Different people may produce different solutions.

#### **Example**

Problem: `Write a beautiful poem.`

Questions arise:

- What makes a poem beautiful?
- How should beauty be measured?

There is no unique answer.

| Well-defined               | Ill-defined                 |
| -------------------------- | --------------------------- |
| Clear input                | Input may be unclear        |
| Clear output               | Output may be subjective    |
| Fixed rules                | Rules may change            |
| Objective                  | Subjective                  |
| Usually one correct answer | Multiple acceptable answers |

### Real-Life Examples

| Problem               | Type                |
| --------------------- | ------------------- |
| Calculate tax         | Well-defined        |
| Play chess optimally  | Mostly well-defined |
| Design a company logo | Ill-defined         |
| Compose music         | Ill-defined         |
| Calculate GPA         | Well-defined        |

---

## **ii-a. Structured Problems**

A structured problem can be solved by following a sequence of well-defined steps. The solution procedure is organized and predictable.

### Characteristics:

- Sequential steps
- Standard methods exist
- Easily converted into algorithms
- Often used in programming

#### **Example 1**

Problem: `Find factorial.`

Steps:

- Read number.
- Multiply numbers from 1 to n.
- Display result.

#### **Example 2**

Problem: `Calculate salary.`

Steps:

- Read basic salary.
- Calculate allowances.
- Calculate deductions.
- Display net salary.

## **ii-b. Unstructured Problems**

An unstructured problem has no fixed sequence of steps.

It often requires:

- Creativity
- Human judgment
- Experience
- Trial and error

#### **Example 1**

Develop a new social media platform.

There is no single correct design.

**Example 2**

Design a game.

Many possible approaches exist.

| Structured         | Unstructured                |
| ------------------ | --------------------------- |
| Fixed steps        | Flexible approach           |
| Algorithm possible | Often difficult to automate |
| Predictable        | Creative                    |
| Objective          | Subjective                  |

---

## **iii-a Simple Problems**

A simple problem requires a small number of inputs and straightforward processing.

Characteristics

- Few variables
- Easy algorithm
- Short execution time
- Easy to understand

#### **Examples**

- Calculate: `2 + 3`

- Find maximum of two numbers.

- Calculate: `Area = Length × Width`

- Check if a number is even.

## **iii-b. Complex Problems**

A complex problem involves:

- Large input
- Multiple constraints
- Multiple subproblems
- Complex algorithms

#### **Example 1**

Google Maps route planning.

Needs to consider:

- Distance
- Traffic
- Road closures
- Fuel efficiency

#### **Example 2**

Weather forecasting.

Uses enormous amounts of data.

| Simple           | Complex           |
| ---------------- | ----------------- |
| Small input      | Large input       |
| Easy algorithm   | Complex algorithm |
| Few steps        | Many steps        |
| Less computation | Heavy computation |

---

## **iv-a. Deterministic Problems**

A deterministic problem always produces the same output for the same input.

#### **Example 1**

Input: `5 + 3`

Output: `8`

Always.

#### **Example 2**

Square of 6

Output: `36`

Always.

Characteristics

- Predictable
- Repeatable
- Reliable

## **iv-b. Non-deterministic Problems**

A non-deterministic problem may have multiple valid solutions or uncertain outcomes.

#### **Example 1**

Chess.

Several good moves may exist.

#### **Example 2**

Robot navigation.

Depending on sensor data, different paths may be chosen.

| Deterministic            | Non-deterministic                      |
| ------------------------ | -------------------------------------- |
| Same input → Same output | Same input → Multiple possible outputs |
| Predictable              | Less predictable                       |
| Fixed rules              | May involve choices or uncertainty     |

---

## **v-a. Static Problems**

A static problem has inputs that remain unchanged during execution.

#### **Example 1**

Sort an array.

Input:

```
[5, 2, 9, 1]
```

The array does not change while sorting.

#### **Example 2**

Calculate GPA.

Marks remain fixed during computation.

Characteristics

- Stable data
- Easier algorithms
- Easier testing

## **v-b. Dynamic Problems**

A dynamic problem has inputs or conditions that may change while the computation is in progress.

#### **Example 1**

Navigation system.

Traffic conditions change continuously.

#### **Example 2**

Stock market analysis.

Prices change every second.

| Static             | Dynamic                      |
| ------------------ | ---------------------------- |
| Data fixed         | Data changes                 |
| Easier computation | More challenging computation |
| Predictable        | Requires continuous updates  |
