---
layout: base
title: "Geometric Progression Solutions"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/practical/blocked-solutions/geometric-progression-solutions/"
---

# {{ page.title | escape }}

1. Write a C program to display the first $n$ terms of an geometric progression when the first term and common ratio are given.

    ```c
    #include <stdio.h>

    int main() {
        int n, i;
        double a, r, term;

        printf("Enter first term (a): ");
        scanf("%lf", &a);

        printf("Enter common ratio (r): ");
        scanf("%lf", &r);

        printf("Enter number of terms (n): ");
        scanf("%d", &n);

        term = a;

        printf("Geometric Progression: ");

        for (i = 1; i <= n; i++) {
            printf("%.2lf ", term);
            term = term * r;
        }

        return 0;
    }
    ```

2. Write a C program to calculate the sum of the first $n$ terms of an geometric progression using loop.

    ```c
    #include <stdio.h>

    int main() {
        float a, r, current_term, sum = 0;
        int n;

        printf("Enter the first term (a): ");
        scanf("%f", &a);

        printf("Enter the common ratio (r): ");
        scanf("%f", &r);

        printf("Enter the number of terms (n): ");
        scanf("%d", &n);

        current_term = a;

        for (int i = 1; i <= n; i++) {
            sum += current_term;       
            current_term *= r;         
        }

        printf("\nThe sum of the first %d terms of the GP series is: %.2f\n", n, sum);

        return 0;
    }
    ```

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

    ```c
    #include <stdio.h>
    #include <math.h>

    int main() {
        double a, r, sum;
        int n;

        printf("Enter the first term (a): ");
        scanf("%lf", &a);

        printf("Enter the common ratio (r): ");
        scanf("%lf", &r);

        printf("Enter the number of terms (n): ");
        scanf("%d", &n);

        if (r == 1) {
            sum = n * a;
        } 
        else if (r > 0) {
            sum = (a * (pow(r, n) - 1)) / (r - 1);
        } 
        else {
            sum = (a * (1 - pow(r, n))) / (1 - r);
        }

        printf("The sum of the first %d terms is: %.4lf\n", n, sum);

        return 0;
    }
    ```

4. Write a C program to find the $n^{th}$ term of an geometric progression using loop.

    ```c
    #include <stdio.h>

    int main() {
        double first_term, ratio;
        int n;
        double nth_term;

        printf("Enter the first term (a): ");
        scanf("%lf", &first_term);

        printf("Enter the common ratio (r): ");
        scanf("%lf", &ratio);

        printf("Enter the term number to find (n): ");
        scanf("%d", &n);

        if (n <= 0) {
            printf("Error: Term position must be a positive integer.\n");
            return 1; 
        }

        nth_term = first_term;

        for (int i = 1; i < n; i++) {
            nth_term *= ratio;
        }

        printf("The %d-th term of the geometric progression is: %.2lf\n", n, nth_term);

        return 0;
    }
    ```

5. Write a C program to determine whether a given sequence forms an GP without using array.

    ```c
    #include <stdio.h>

    int main() {
        int n, i;
        double current, previous, ratio;

        printf("Enter number of terms: ");
        scanf("%d", &n);

        if (n <= 0) {
            printf("Invalid number of terms.\n");
            return 0;
        }

        printf("Enter the first term: ");
        scanf("%lf", &previous);

        if (n == 1) {
            printf("The sequence is a GP.\n");
            return 0;
        }

        printf("Enter the second term: ");
        scanf("%lf", &current);

        if (previous == 0) {
            if (current == 0)
                ratio = 0;
            else {
                printf("The sequence is NOT a GP.\n");
                return 0;
            }
        } else {
            ratio = current / previous;
        }

        previous = current;

        for (i = 3; i <= n; i++) {
            printf("Enter term %d: ", i);
            scanf("%lf", &current);

            if (previous == 0) {
                if (current != 0) {
                    printf("The sequence is NOT a GP.\n");
                    return 0;
                }
            } else {
                if (current / previous != ratio) {
                    printf("The sequence is NOT a GP.\n");
                    return 0;
                }
            }

            previous = current;
        }

        printf("The sequence is a GP.\n");

        return 0;
    }
    ```

6. Write a C program to determine whether a given sequence forms an GP.

    ```c
    #include <stdio.h>
    #include <stdlib.h>

    int main() {
        int n, i;
        double *a;

        printf("Enter number of terms: ");
        scanf("%d", &n);

        if (n <= 0) {
            printf("Invalid number of terms.\n");
            return 0;
        }

        a = (double *)malloc(n * sizeof(double));

        if (a == NULL) {
            printf("Memory allocation failed.\n");
            return 1;
        }

        printf("Enter the terms:\n");

        for (i = 0; i < n; i++) {
            scanf("%lf", &a[i]);
        }

        if (n <= 1) {
            printf("The sequence is a GP.\n");
            free(a);
            return 0;
        }

        for (i = 2; i < n; i++) {
            if (a[i] * a[i - 2] != a[i - 1] * a[i - 1]) {
                printf("The sequence is NOT a GP.\n");
                free(a);
                return 0;
            }
        }

        printf("The sequence is a GP.\n");

        free(a);

        return 0;
    }
    ```