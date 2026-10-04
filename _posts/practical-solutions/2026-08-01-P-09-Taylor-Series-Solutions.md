---
layout: base
title: "Taylor Series Solutions"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/practical/blocked-solutions/taylor-series-solutions/"
---

# {{ page.title | escape }}

1. Write a C program to calculate $e^x$ using the Maclaurin series for a given value of $x$ and number of terms $n$.

    $$
    e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \frac{x^4}{4!} + \cdots 
    $$

    ```c
    #include <stdio.h>

    int main() {
        int n, i;
        double x, term, sum;

        printf("Enter x: ");
        scanf("%lf", &x);

        printf("Enter number of terms: ");
        scanf("%d", &n);

        if (n <= 0) {
            printf("Number of terms must be positive.\n");
            return 0;
        }

        sum = 1.0;
        term = 1.0;

        for (i = 1; i < n; i++) {
            term = term * x / i;
            sum = sum + term;
        }

        printf("e^%.2lf = %.10lf\n", x, sum);

        return 0;
    }
    ```

2. Write a C program to calculate $\sin(x)$ using its Maclaurin series. The value of $x$ must be entered in radians.

    $$
    \sin(x) = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots
    $$

    ```c
    #include <stdio.h>

    int main() {
        int n, i;
        double x, term, sum;

        printf("Enter x in radians: ");
        scanf("%lf", &x);

        printf("Enter number of terms: ");
        scanf("%d", &n);

        if (n <= 0) {
            printf("Number of terms must be positive.\n");
            return 0;
        }

        term = x;
        sum = term;

        for (i = 1; i < n; i++) {
            term = -term * x * x / ((2 * i) * (2 * i + 1));
            sum = sum + term;
        }

        printf("sin(%.4lf) = %.10lf\n", x, sum);

        return 0;
    }
    ```

3. Write a C program to calculate $\cos(x)$ using its Maclaurin series. The value of $x$ must be entered in radians.

    $$
    \cos(x) = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \dots
    $$

    ```c
    #include <stdio.h>

    int main() {
        int n, i;
        double x, term, sum;

        printf("Enter x in radians: ");
        scanf("%lf", &x);

        printf("Enter number of terms: ");
        scanf("%d", &n);

        if (n <= 0) {
            printf("Number of terms must be positive.\n");
            return 0;
        }

        term = 1.0;
        sum = term;

        for (i = 1; i < n; i++) {
            term = -term * x * x / ((2 * i - 1) * (2 * i));
            sum = sum + term;
        }

        printf("cos(%.4lf) = %.10lf\n", x, sum);

        return 0;
    }
    ```

4. Write a C program to approximate the value of $\pi$ using the Leibniz series:

    $$
    \pi = 4 \left( 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \dots \right)
    $$

    ```c
    #include <stdio.h>

    int main() {
        int n, i;
        double pi = 0.0;
        double term;

        printf("Enter number of terms: ");
        scanf("%d", &n);

        if (n <= 0) {
            printf("Number of terms must be positive.\n");
            return 0;
        }

        for (i = 0; i < n; i++) {
            term = 1.0 / (2 * i + 1);

            if (i % 2 == 0)
                pi = pi + term;
            else
                pi = pi - term;
        }

        pi = 4 * pi;

        printf("Approximate value of pi = %.10lf\n", pi);

        return 0;
    }
    ```

5. Write a menu-driven C program to perform the following operations:

    I. Calculate $e^x$ 

    II. Calculate $\sin(x)$ 

    III. Calculate $\cos(x)$ 

    IV. Approximate $\pi$ 

    V. Exit

    ```c
    #include <stdio.h>

    int main() {
        int choice, n, i;
        double x, term, result;

        do {
            printf("\n========== TAYLOR SERIES MENU ==========\n");
            printf("1. Calculate e^x\n");
            printf("2. Calculate sin(x)\n");
            printf("3. Calculate cos(x)\n");
            printf("4. Approximate pi\n");
            printf("5. Exit\n");
            printf("========================================\n");

            printf("Enter your choice: ");
            scanf("%d", &choice);

            switch (choice) {

                case 1:
                    /* Calculate e^x */
                    printf("\nEnter x: ");
                    scanf("%lf", &x);

                    printf("Enter number of terms: ");
                    scanf("%d", &n);

                    if (n <= 0) {
                        printf("Number of terms must be positive.\n");
                        break;
                    }

                    term = 1.0;
                    result = 1.0;

                    for (i = 1; i < n; i++) {
                        term = term * x / i;
                        result = result + term;
                    }

                    printf("e^%.4lf = %.10lf\n", x, result);
                    break;


                case 2:
                    /* Calculate sin(x) */
                    printf("\nEnter x in radians: ");
                    scanf("%lf", &x);

                    printf("Enter number of terms: ");
                    scanf("%d", &n);

                    if (n <= 0) {
                        printf("Number of terms must be positive.\n");
                        break;
                    }

                    term = x;
                    result = term;

                    for (i = 1; i < n; i++) {
                        term = -term * x * x /
                            ((2 * i) * (2 * i + 1));

                        result = result + term;
                    }

                    printf("sin(%.4lf) = %.10lf\n", x, result);
                    break;


                case 3:
                    /* Calculate cos(x) */
                    printf("\nEnter x in radians: ");
                    scanf("%lf", &x);

                    printf("Enter number of terms: ");
                    scanf("%d", &n);

                    if (n <= 0) {
                        printf("Number of terms must be positive.\n");
                        break;
                    }

                    term = 1.0;
                    result = term;

                    for (i = 1; i < n; i++) {
                        term = -term * x * x /
                            ((2 * i - 1) * (2 * i));

                        result = result + term;
                    }

                    printf("cos(%.4lf) = %.10lf\n", x, result);
                    break;


                case 4:
                    /* Approximate pi using Leibniz series */
                    printf("\nEnter number of terms: ");
                    scanf("%d", &n);

                    if (n <= 0) {
                        printf("Number of terms must be positive.\n");
                        break;
                    }

                    result = 0.0;

                    for (i = 0; i < n; i++) {
                        term = 1.0 / (2 * i + 1);

                        if (i % 2 == 0)
                            result = result + term;
                        else
                            result = result - term;
                    }

                    result = 4 * result;

                    printf("Approximate value of pi = %.10lf\n",
                        result);
                    break;


                case 5:
                    printf("\nProgram terminated.\n");
                    break;


                default:
                    printf("\nInvalid choice. Please try again.\n");
            }

        } while (choice != 5);

        return 0;
    }
    ```