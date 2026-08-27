---
layout: base
title: "Loops - Basic Iteration Solutions"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/practical/loops-basic-iteration-solutions/"
---

# {{ page.title | escape }}

1. Write a program to display numbers from $1$ to $n$ using loop.

    ```c
    #include <stdio.h>

    int main() {
        int n, i;

        printf("Enter the value of n: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {
            printf("%d ", i);
        }

        return 0;
    }
    ```

2. Write a program to display numbers from $n$ to $1$ using loop.

    ```c
    #include <stdio.h>

    int main() {
        int n, i;

        printf("Enter the value of n: ");
        scanf("%d", &n);

        for (i = n; i >= 1; i--) {
            printf("%d ", i);
        }

        return 0;
    }
    ```

3. Write a program to display all even numbers from $1$ to $n$ using loop.

    ```c
    #include <stdio.h>

    int main() {
        int n, i;

        printf("Enter the value of n: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {
            if (i % 2 == 0)
                printf("%d ", i);
        }

        return 0;
    }
    ```

4. Write a program to display all odd numbers from $1$ to $n$ using loop.

    ```c
    #include <stdio.h>

    int main() {
        int n, i;

        printf("Enter the value of n: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {
            if (i % 2 != 0)
                printf("%d ", i);
        }

        return 0;
    }
    ```

5. Write a program to find the sum of numbers from $1$ to $n$ using while loop.

    ```c
    #include <stdio.h>

    int main() {
        int n, i = 1, sum = 0;

        printf("Enter the value of n: ");
        scanf("%d", &n);

        while (i <= n) {
            sum = sum + i;
            i++;
        }

        printf("Sum = %d", sum);

        return 0;
    }
    ```

6. Write a program to find the sum of all even numbers from $1$ to $n$ using do-while loop.

    ```c
    #include <stdio.h>

    int main() {
        int n, i = 1, sum = 0;

        printf("Enter the value of n: ");
        scanf("%d", &n);

        do {
            if (i % 2 == 0)
                sum = sum + i;

            i++;
        } while (i <= n);

        printf("Sum of even numbers = %d", sum);

        return 0;
    }
    ```

7. Write a program to find the sum of all odd numbers from $1$ to $n$ using loop.

    ```c
    #include <stdio.h>

    int main() {
        int n, i, sum = 0;

        printf("Enter the value of n: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {
            if (i % 2 != 0)
                sum = sum + i;
        }

        printf("Sum of odd numbers = %d", sum);

        return 0;
    }
    ```

8. Write a program to find the sum of squares from $1$ to $n$ using loop.

    ```c
    #include <stdio.h>

    int main() {
        int n, i;
        long sum = 0;

        printf("Enter the value of n: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {
            sum = sum + (i * i);
        }

        printf("Sum of squares = %ld", sum);

        return 0;
    }
    ```

9. Write a program to find the sum of cubes from $1$ to $n$ using loop.

    ```c
    #include <stdio.h>

    int main() {
        int n, i;
        long sum = 0;

        printf("Enter the value of n: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {
            sum = sum + (i * i * i);
        }

        printf("Sum of cubes = %ld", sum);

        return 0;
    }
    ```

10. Write a program to display the square and cube of numbers from $1$ to $n$ in tabular form  using loop.

    Example:

    ```
    Number    Square    Cube
    1         1         1
    2         4         8
    3         9         27
    ```

    ```c
    #include <stdio.h>

    int main() {
        int n, i;
        long long square, cube;

        printf("Enter the value of n: ");
        scanf("%d", &n);

        printf("Number\t\tSquare\t\tCube\n");

        for (i = 1; i <= n; i++) {
            square = (long long)i * i;
            cube = (long long)i * i * i;

            printf("%d\t\t%lld\t\t%lld\n", i, square, cube);
        }

        return 0;
    }
    ```