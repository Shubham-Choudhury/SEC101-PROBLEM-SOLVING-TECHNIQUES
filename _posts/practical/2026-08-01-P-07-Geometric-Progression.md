---
layout: base
title: "Geometric Progression"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/practical/geometric-progression/"
---

# {{ page.title | escape }}

1. Write a C program to display the first $n$ terms of an geometric progression when the first term and common ratio are given.

2. Write a C program to calculate the sum of the first $n$ terms of an geometric progression using loop.

3. Write a C program to calculate the sum of the first $n$ terms of an geometric progression.

    $$
    \begin{align*}
    \textbf{Case 1: } & r = 1 \\
    & S_n = na \\[1em]
    \textbf{Case 2: } &  r > 0, \, r \neq 1 \\
    & S_n = \frac{a(r^n - 1)}{r - 1} \\[1em]
    \textbf{Case 3: } &  r < 0 \\
    & S_n = \frac{a(1 - r^n)}{1 - r}
    \end{align*}
    $$

4. Write a C program to find the $n^{th}$ term of an geometric progression using loop.

5. Write a C program to determine whether a given sequence forms an GP without using array.

6. Write a C program to determine whether a given sequence forms an GP.

<a href="{{ '/practical/geometric-progression-solutions/' | relative_url }}">Solutions</a>
