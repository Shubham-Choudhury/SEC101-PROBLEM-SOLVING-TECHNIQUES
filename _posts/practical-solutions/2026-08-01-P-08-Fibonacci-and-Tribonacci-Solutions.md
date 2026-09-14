---
layout: base
title: "Fibonacci & Tribonacci Solutions"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/practical/fibonacci-and-tribonacci-solutions/"
---

# {{ page.title | escape }}

1. Write a C program to generate and display the first $n$ Fibonacci numbers.

    ```c
    #include <stdio.h>

    int main() {
        int n, i;
        long long a = 0, b = 1, c;

        printf("Enter n: ");
        scanf("%d", &n);

        if (n <= 0) {
            printf("Invalid input.\n");
            return 0;
        }

        printf("First %d Fibonacci numbers: ", n);

        for (i = 1; i <= n; i++) {
            printf("%lld ", a);

            c = a + b;
            a = b;
            b = c;
        }

        return 0;
    }
    ```

2. Write a C program to check whether a given non-negative integer is a Fibonacci number.

    ```c
    #include <stdio.h>

    int main() {
        long long n;
        long long a = 0, b = 1, c;

        printf("Enter a number: ");
        scanf("%lld", &n);

        if (n < 0) {
            printf("Negative numbers are not Fibonacci numbers.\n");
            return 0;
        }

        while (a < n) {
            c = a + b;
            a = b;
            b = c;
        }

        if (a == n)
            printf("%lld belongs to the Fibonacci sequence.\n", n);
        else
            printf("%lld does not belong to the Fibonacci sequence.\n", n);

        return 0;
    }
    ```

3. Write a C program to generate and display the first $n$ Tribonacci numbers.

    ```c
    #include <stdio.h>

    int main() {
        int n, i;
        long long a = 0, b = 0, c = 1, d;

        printf("Enter n: ");
        scanf("%d", &n);

        if (n <= 0) {
            printf("Invalid input.\n");
            return 0;
        }

        printf("First %d Tribonacci numbers: ", n);

        for (i = 1; i <= n; i++) {
            printf("%lld ", a);

            d = a + b + c;
            a = b;
            b = c;
            c = d;
        }

        return 0;
    }
    ```

4. Write a C program to check whether two given positive integers are consecutive Fibonacci numbers.

    ```c
    #include <stdio.h>

    int main() {
        long long x, y;
        long long a = 0, b = 1, c;
        int found = 0;

        printf("Enter two positive integers: ");
        scanf("%lld %lld", &x, &y);

        if (x <= 0 || y <= 0) {
            printf("Please enter positive integers.\n");
            return 0;
        }

        while (b <= y || a <= y) {
            if ((a == x && b == y) || (a == y && b == x)) {
                found = 1;
                break;
            }

            c = a + b;
            a = b;
            b = c;

            if (a > y && b > y)
                break;
        }

        if (found)
            printf("%lld and %lld are consecutive Fibonacci numbers.\n", x, y);
        else
            printf("%lld and %lld are not consecutive Fibonacci numbers.\n", x, y);

        return 0;
    }
    ```

5. Write a C program to find the largest Fibonacci number strictly smaller than a given positive integer $n$.

    ```c
    #include <stdio.h>

    int main() {
        long long n;
        long long a = 0, b = 1, c;
        long long largest = -1;

        printf("Enter a positive integer: ");
        scanf("%lld", &n);

        if (n <= 0) {
            printf("Invalid input.\n");
            return 0;
        }

        while (a < n) {
            largest = a;

            c = a + b;
            a = b;
            b = c;
        }

        if (largest >= 0)
            printf("Largest Fibonacci number smaller than %lld = %lld\n",
                n, largest);
        else
            printf("No Fibonacci number is smaller than %lld.\n", n);

        return 0;
    }
    ```

