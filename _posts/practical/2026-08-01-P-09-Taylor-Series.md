---
layout: base
title: "Taylor Series"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/practical/taylor-series/"
---

# {{ page.title | escape }}

1. Write a C program to calculate $e^x$ using the Maclaurin series for a given value of $x$ and number of terms $n$.

    $$
    e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \frac{x^4}{4!} + \cdots 
    $$

2. Write a C program to calculate $\sin(x)$ using its Maclaurin series. The value of $x$ must be entered in radians.

    $$
    \sin(x) = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots
    $$

3. Write a C program to calculate $\cos(x)$ using its Maclaurin series. The value of $x$ must be entered in radians.

    $$
    \cos(x) = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \dots

    $$

4. Write a C program to approximate the value of $\pi$ using the Leibniz series:

    $$
    \pi = 4 \left( 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \dots \right)
    $$

6. Write a menu-driven C program to perform the following operations:

    I. Calculate $e^x$ 

    II. Calculate $\sin(x)$ 

    III. Calculate $\cos(x)$ 

    IV. Approximate $\pi$ 

    V. Exit

<a href="{{ '/practical/taylor-series-solutions/' | relative_url }}">Solutions</a>