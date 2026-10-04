---
layout: base
title: "Arithmetic Progression Solutions"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/practical/blocked-solutions/arithmetic-progression-solutions/"
---

# {{ page.title | escape }}

1. Write a C program to display the first $n$ terms of an AP when the first term and common difference are given.

    ```c
    #include <stdio.h>

    int main() {
        int a, d, n, i, term;

        printf("Enter the first term: ");
        scanf("%d", &a);

        printf("Enter the common difference: ");
        scanf("%d", &d);

        printf("Enter the number of terms: ");
        scanf("%d", &n);

        printf("Arithmetic Progression: ");

        for (i = 0; i < n; i++) {
            term = a + i * d;
            printf("%d ", term);
        }

        return 0;
    }
    ```

2. Write a C program to calculate the sum of the first $n$ terms of an arithmetic progression using loop.

    ```c
    #include <stdio.h>

    int main() {
        int a, d, n, i;
        int sum = 0;

        printf("Enter first term: ");
        scanf("%d", &a);

        printf("Enter common difference: ");
        scanf("%d", &d);

        printf("Enter number of terms: ");
        scanf("%d", &n);

        for (i = 0; i < n; i++) {
            sum = sum + (a + i * d);
        }

        printf("Sum of AP = %d\n", sum);

        return 0;
    }
    ```

3. Write a C program to calculate the sum of the first $n$ terms of an arithmetic progression.<br>FORMULA: $S_n = \frac{n}{2} [2a + (n - 1)d]$

    ```c
    #include <stdio.h>

    int main() {
        int a, d, n;
        int sum;

        printf("Enter first term (a): ");
        scanf("%d", &a);

        printf("Enter common difference (d): ");
        scanf("%d", &d);

        printf("Enter number of terms (n): ");
        scanf("%d", &n);

        sum = n * (2 * a + (n - 1) * d) / 2;

        printf("Sum of AP = %d\n", sum);

        return 0;
    }
    ```

4. Write a C program to find the $n^{th}$ term of an arithmetic progression using loop.

    ```c
    #include <stdio.h>

    int main() {
        int a, d, n;
        int nth_term;

        printf("Enter first term (a): ");
        scanf("%d", &a);

        printf("Enter common difference (d): ");
        scanf("%d", &d);

        printf("Enter number of terms (n): ");
        scanf("%d", &n);

        if (n <= 0) {
            printf("Error: Position 'n' must be a positive integer greater than 0.\n");
            return 1;
        }

        nth_term = a;

        for (int i = 1; i < n; i++) {
            nth_term += d;
        }

        printf("The %d-th term of the arithmetic progression is: %d\n", n, nth_term);

        return 0;
    }
    ```

5. Write a C program to find the $n^{th}$ term of an arithmetic progression.<br>FORMULA: $a_n = a + (n - 1)d$

    ```c
    #include <stdio.h>

    int main() {
        int a, d, n;
        int nthTerm;

        printf("Enter first term (a): ");
        scanf("%d", &a);

        printf("Enter common difference (d): ");
        scanf("%d", &d);

        printf("Enter term number (n): ");
        scanf("%d", &n);

        nthTerm = a + (n - 1) * d;

        printf("The %dth term = %d\n", n, nthTerm);

        return 0;
    }
    ```

6. Write a C program to generate all AP terms within a given range.

    ```c
    #include <stdio.h>

    int main() {
        int a, d, lower, upper;
        int term;

        printf("Enter first term (a): ");
        scanf("%d", &a);

        printf("Enter common difference (d): ");
        scanf("%d", &d);

        printf("Enter lower limit: ");
        scanf("%d", &lower);

        printf("Enter upper limit: ");
        scanf("%d", &upper);

        printf("AP terms within the range: ");

        if (d == 0) {
            if (a >= lower && a <= upper) {
                printf("%d", a);
            } else {
                printf("No terms");
            }
        }
        else if (d > 0) {
            term = a;

            while (term <= upper) {
                if (term >= lower) {
                    printf("%d ", term);
                }

                term = term + d;
            }
        }
        else {
            term = a;

            while (term >= lower) {
                if (term <= upper) {
                    printf("%d ", term);
                }

                term = term + d;
            }
        }

        return 0;
    }
    ```

7. Write a C program to determine whether a given sequence forms an AP without using array.

    ```c
    #include <stdio.h>

    int main() {
        int n, i;
        int current, previous;
        int difference;
        int isAP = 1;

        printf("Enter number of terms: ");
        scanf("%d", &n);

        if (n <= 0) {
            printf("Invalid number of terms.\n");
            return 0;
        }

        printf("Enter term 1: ");
        scanf("%d", &previous);

        if (n == 1) {
            printf("The sequence is an AP.\n");
            return 0;
        }

        printf("Enter term 2: ");
        scanf("%d", &current);

        difference = current - previous;
        previous = current;

        for (i = 3; i <= n; i++) {
            printf("Enter term %d: ", i);
            scanf("%d", &current);

            if (current - previous != difference) {
                isAP = 0;
            }

            previous = current;
        }

        if (isAP == 1) {
            printf("The sequence is an AP.\n");
            printf("Common Difference = %d\n", difference);
        } else {
            printf("The sequence is NOT an AP.\n");
        }

        return 0;
    }
    ```

8. Write a C program to determine whether a given sequence forms an AP.

    ```c
    #include <stdio.h>
    #include <stdlib.h>

    int main() {
        int n, i;
        int *a;
        int difference;
        int isAP = 1;

        printf("Enter number of terms: ");
        scanf("%d", &n);

        if (n <= 0) {
            printf("Invalid number of terms.\n");
            return 0;
        }

        a = (int *)malloc(n * sizeof(int));

        if (a == NULL) {
            printf("Memory allocation failed.\n");
            return 1;
        }

        printf("Enter the terms:\n");

        for (i = 0; i < n; i++) {
            scanf("%d", &a[i]);
        }

        if (n <= 2) {
            printf("The sequence is an AP.\n");
            free(a);
            return 0;
        }

        difference = a[1] - a[0];

        for (i = 2; i < n; i++) {
            if (a[i] - a[i - 1] != difference) {
                isAP = 0;
                break;
            }
        }

        if (isAP == 1) {
            printf("The sequence is an AP.\n");
            printf("Common difference = %d\n", difference);
        } else {
            printf("The sequence is NOT an AP.\n");
        }

        free(a);

        return 0;
    }
    ```
