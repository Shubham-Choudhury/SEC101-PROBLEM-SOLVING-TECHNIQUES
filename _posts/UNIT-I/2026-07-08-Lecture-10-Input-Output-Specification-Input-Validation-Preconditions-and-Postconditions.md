---
layout: base
title: "Lecture 10: Input/Output Specification, Input Validation, Preconditions, and Postconditions"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/lecture-10-input-output-specification-input-validation-preconditions-and-postconditions/"
---

# {{ page.title | escape }}

## 1. Input Specification

Input Specification describes the data that a program expects from the user or another system. A clear input specification reduces ambiguity and helps prevent errors.

It clearly defines:

- Input name
- Data type
- Valid range
- Format
- Constraints

### # Components of Input Specification

| Component   | Description                             |
| ----------- | --------------------------------------- |
| Input Name  | Name of the input variable              |
| Data Type   | Integer, Float, Character, String, etc. |
| Valid Range | Minimum and maximum allowed values      |
| Format      | Expected input format                   |
| Constraints | Additional conditions                   |

#### **Example:** Student Marks

Problem: `Calculate student grade.`

Input Specification:

| Input        | Data Type | Valid Range           |
| ------------ | --------- | --------------------- |
| Student Name | String    | Maximum 50 characters |
| Roll Number  | Integer   | Positive integer      |
| Marks        | Integer   | 0–100                 |

## 2. Output Specification

Output Specification describes the information that the program should produce after processing the input.

It defines:

- Output name
- Format
- Data type
- Units (if applicable)

#### **Example:**

Problem: `Calculate Simple Interest.`

Output Specification:

| Output          | Data Type |
| --------------- | --------- |
| Simple Interest | Float     |

## 3. Input Validation

Input Validation is the process of checking whether the entered input satisfies the required conditions before processing. If the input is invalid, the program should reject it and ask the user to enter valid data.

### # Why Input Validation is Important

Without validation:

- Programs may crash.
- Incorrect results may be produced.
- Security risks may arise.
- Invalid data may be stored.

### # Types of Input Validation

1. Range Validation:

   Checks whether the input lies within a specified range.

   Example:

   Age

   ```
   0 ≤ Age ≤ 120
   ```

   Input:

   ```
   150
   ```

   Output:

   ```
   Invalid Age
   ```

2. Type Validation

   Checks whether the data type is correct.

   Example:

   Age should be an integer.

   User enters:

   ```
   Twenty
   ```

   Output:

   ```
   Invalid Data Type
   ```

3. Format Validation

   Checks whether the input follows a specified format.

   Example:

   Email

   Correct:

   ```
   student@example.com
   ```

   Incorrect:

   ```
   studentexample.com
   ```

4. Length Validation

   Checks the number of characters.

   Example:

   Password

   Minimum:

   ```
   8 characters
   ```

   Input:

   ```
   abc
   ```

   Output:

   ```
   Password Too Short
   ```

5. Presence Validation

   Checks whether a required field has been left blank.

   Example:

   Student Name

   Blank input:

   ```
   ""
   ```

   Output:

   ```
   Name Cannot Be Empty
   ```

## 4. Error Handling

When invalid input is detected, the program should:

<ol type="I">
<li>Display a meaningful error message.</li>
<li>Ask the user to enter the data again.</li>
<li>Prevent incorrect processing.</li>
</ol>

## 5. Preconditions

A Precondition is a condition that must be true before an algorithm or program begins execution. If the precondition is not satisfied, the algorithm should not continue.

#### **Example:** Division

Problem: `Divide A by B.`

Precondition:

```
B ≠ 0
```

If:

```
B = 0
```

Division cannot be performed.

### # Importance of Preconditions

They help to:

- Prevent runtime errors.
- Improve algorithm correctness.
- Clearly define valid inputs.

## 6. Postconditions

A Postcondition is a condition that must be true after the successful execution of an algorithm or program. It describes the expected state after completion.

#### **Example:** Addition

Problem: `Add two numbers.`

Postcondition:

```
Sum = A + B
```

## Preconditions vs Postconditions

| Preconditions                    | Postconditions               |
| -------------------------------- | ---------------------------- |
| Must be true before execution    | Must be true after execution |
| Define valid starting conditions | Define expected final state  |
| Prevent invalid execution        | Verify correct execution     |
