---
layout: base
title: "Lecture 12: Structured Programming Constructs – Control Structure Stacking and Nesting"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/lecture-12-structured-programming-constructs-control-structure-stacking-and-nesting/"
---

# {{ page.title | escape }}

## 1. What is Control Structure Stacking?

Control Structure Stacking means placing one control structure after another, where each structure executes sequentially.

### # General Representation

![Control Structure Stacking General Representation]({{ '/assets/images/Control-Structure-Stacking-General-Representation.png' | relative_url }})

### # Characteristics of Stacking

- Structures execute one after another.
- Easy to understand.
- Suitable for most business applications.
- No structure exists inside another.

## 2. What is Nesting?

Nesting means placing one control structure inside another. A control structure becomes part of another control structure.

## Difference Between Stacking and Nesting

| Stacking                              | Nesting                                     |
| ------------------------------------- | ------------------------------------------- |
| Structures execute one after another. | One structure exists inside another.        |
| Easier to understand.                 | Slightly more complex.                      |
| Independent execution.                | Inner structure depends on outer structure. |
| Used in simple programs.              | Used in complex programs.                   |
