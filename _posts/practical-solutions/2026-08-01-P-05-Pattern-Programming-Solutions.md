---
layout: base
title: "Pattern Programming Solutions"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/practical/pattern-programming-solutions/"
---

# {{ page.title | escape }}

1. Write a program to print the following right-angled triangle star pattern using nested loops:

   ```
    *
    **
    ***
    ****
    *****
   ```

   ```c
   #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {
            for (j = 1; j <= i; j++) {
                printf("*");
            }
            printf("\n");
        }

        return 0;
    }
   ```

2. Write a program to print the following inverted right-angled triangle star pattern using nested loops:

   ```
    *****
    ****
    ***
    **
    *
   ```

   ```c
    #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = n; i >= 1; i--) {
            for (j = 1; j <= i; j++) {
                printf("*");
            }
            printf("\n");
        }

        return 0;
    }
   ```

3. Write a program to print the following right-angled number triangle pattern using nested loops:

   ```
    1
    12
    123
    1234
    12345
   ```

   ```c
   #include <stdio.h>

   int main() {
       int i, j, n;

       printf("Enter the number of rows: ");
       scanf("%d", &n);

       for (i = 1; i <= n; i++) {
           for (j = 1; j <= i; j++) {
               printf("%d", j);
           }
           printf("\n");
       }

       return 0;
   }
   ```

4. Write a program to print the following pattern using nested loops:

   ```
    1
    22
    333
    4444
    55555
   ```

   ```c
   #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {
            for (j = 1; j <= i; j++) {
                printf("%d", i);
            }
            printf("\n");
        }

        return 0;
    }
   ```

5. Write a program to print the following inverted right-angled number triangle pattern using nested loops:

   ```
    12345
    1234
    123
    12
    1
   ```

   ```c
   #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = n; i >= 1; i--) {
            for (j = 1; j <= i; j++) {
                printf("%d", j);
            }
            printf("\n");
        }

        return 0;
    }
   ```

6. Write a program to print the following right-aligned right-angled triangle star pattern using nested loops:

   ```
        *
       **
      ***
     ****
    *****
   ```

   ```c
   #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {
            for (j = 1; j <= n - i; j++) {
                printf(" ");
            }

            for (j = 1; j <= i; j++) {
                printf("*");
            }

            printf("\n");
        }

        return 0;
    }
   ```

7. Write a program to print the following palindromic number triangle pattern using nested loops:

   ```
    1
    121
    12321
    1234321
    123454321
   ```

   ```c
   #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {

            for (j = 1; j <= i; j++) {
                printf("%d", j);
            }

            for (j = i - 1; j >= 1; j--) {
                printf("%d", j);
            }

            printf("\n");
        }

        return 0;
    }
   ```

8. Write a program to print the following number triangle pattern using nested loops:

   ```
    5
    45
    345
    2345
    12345
   ```

   ```c
   #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {
            for (j = n - i + 1; j <= n; j++) {
                printf("%d", j);
            }
            printf("\n");
        }

        return 0;
    }
   ```

9. Write a program to print the following continuous number matrix using nested loops:

   ```
    1 2 3 4 5
    6 7 8 9 10
    11 12 13 14 15
    16 17 18 19 20
    21 22 23 24 25
   ```

   ```c
   #include <stdio.h>

    int main() {
        int i, j, n, num = 1;

        printf("Enter the size of matrix: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {
            for (j = 1; j <= n; j++) {
                printf("%d\t", num);
                num++;
            }
            printf("\n");
        }

        return 0;
    }
   ```

10. Write a program to print the following inverted odd-number triangle pattern using nested loops:

    ```
    1 3 5 7 9
    3 5 7 9
    5 7 9
    7 9
    9
    ```

    ```c
    #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {
            for (j = i; j <= n; j++) {
                printf("%d ", 2 * j - 1);
            }
            printf("\n");
        }

        return 0;
    }
    ```

11. Write a program to print the following right-shifted square star pattern using nested loops:

    ```
    *****
     *****
      *****
       *****
        *****
    ```

    ```c
    #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the size: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {

            for (j = 1; j < i; j++) {
                printf(" ");
            }

            for (j = 1; j <= n; j++) {
                printf("*");
            }

            printf("\n");
        }

        return 0;
    }
    ```

12. Write a program to print the following right-aligned square star pattern using nested loops:

    ```
        *****
       *****
      *****
     *****
    *****
    ```

    ```c
    #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the size: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {

            for (j = 1; j <= n - i; j++) {
                printf(" ");
            }

            for (j = 1; j <= n; j++) {
                printf("*");
            }

            printf("\n");
        }

        return 0;
    }
    ```

13. Write a program to print the following centered star pyramid pattern using nested loops:

    ```
        *
       ***
      *****
     *******
    *********
    ```

    ```c
    #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {

            for (j = 1; j <= n - i; j++) {
                printf(" ");
            }

            for (j = 1; j <= 2 * i - 1; j++) {
                printf("*");
            }

            printf("\n");
        }

        return 0;
    }
    ```

14. Write a program to print the following inverted centered star pyramid pattern using nested loops:

    ```
    *********
     *******
      *****
       ***
        *
    ```

    ```c
    #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = n; i >= 1; i--) {

            for (j = 1; j <= n - i; j++) {
                printf(" ");
            }

            for (j = 1; j <= 2 * i - 1; j++) {
                printf("*");
            }

            printf("\n");
        }

        return 0;
    }
    ```

15. Write a program to print the following hollow centered star pyramid pattern using nested loops:

    ```
        *
       * *
      *   *
     *     *
    *********
    ```

    ```c
    #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {

            for (j = 1; j <= n - i; j++) {
                printf(" ");
            }

            for (j = 1; j <= 2 * i - 1; j++) {
                if (j == 1 || j == 2 * i - 1 || i == n)
                    printf("*");
                else
                    printf(" ");
            }

            printf("\n");
        }

        return 0;
    }
    ```

16. Write a program to print the following inverted hollow centered star pyramid pattern using nested loops:

    ```
    *********
     *     *
      *   *
       * *
        *
    ```

    ```c
    #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = n; i >= 1; i--) {

            for (j = 1; j <= n - i; j++) {
                printf(" ");
            }

            for (j = 1; j <= 2 * i - 1; j++) {
                if (j == 1 || j == 2 * i - 1 || i == n)
                    printf("*");
                else
                    printf(" ");
            }

            printf("\n");
        }

        return 0;
    }
    ```

17. Write a program to print the following diamond-shaped star pattern using nested loops:

    ```
    *
    **
    ***
    ****
    *****
    ****
    ***
    **
    *
    ```

    ```c
    #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {
            for (j = 1; j <= i; j++) {
                printf("*");
            }
            printf("\n");
        }

        for (i = n - 1; i >= 1; i--) {
            for (j = 1; j <= i; j++) {
                printf("*");
            }
            printf("\n");
        }

        return 0;
    }
    ```

18. Write a program to print the following right-aligned diamond-shaped star pattern using nested loops:

    ```
        *
       **
      ***
     ****
    *****
     ****
      ***
       **
        *
    ```

    ```c
    #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {

            for (j = 1; j <= n - i; j++) {
                printf(" ");
            }

            for (j = 1; j <= i; j++) {
                printf("*");
            }

            printf("\n");
        }

        for (i = n - 1; i >= 1; i--) {

            for (j = 1; j <= n - i; j++) {
                printf(" ");
            }

            for (j = 1; j <= i; j++) {
                printf("*");
            }

            printf("\n");
        }

        return 0;
    }
    ```

19. Write a program to print the following centered diamond star pattern using nested loops:

    ```
        *
       ***
      *****
     *******
    *********
     *******
      *****
       ***
        *
    ```

    ```c
    #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {

            for (j = 1; j <= n - i; j++) {
                printf(" ");
            }

            for (j = 1; j <= 2 * i - 1; j++) {
                printf("*");
            }

            printf("\n");
        }

        for (i = n - 1; i >= 1; i--) {

            for (j = 1; j <= n - i; j++) {
                printf(" ");
            }

            for (j = 1; j <= 2 * i - 1; j++) {
                printf("*");
            }

            printf("\n");
        }

        return 0;
    }
    ```

20. Write a program to print the following star pattern using nested loops:

    ```
    *****
    ****
    ***
    **
    *
    **
    ***
    ****
    *****
    ```

    ```c
    #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = n; i >= 1; i--) {
            for (j = 1; j <= i; j++) {
                printf("*");
            }
            printf("\n");
        }

        for (i = 2; i <= n; i++) {
            for (j = 1; j <= i; j++) {
                printf("*");
            }
            printf("\n");
        }

        return 0;
    }
    ```

21. Write a program to print the following star pattern using nested loops:

    ```
    *****
     ****
      ***
       **
        *
       **
      ***
     ****
    *****
    ```

    ```c
    #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = n; i >= 1; i--) {

            for (j = 1; j <= n - i; j++) {
                printf(" ");
            }

            for (j = 1; j <= i; j++) {
                printf("*");
            }

            printf("\n");
        }

        for (i = 2; i <= n; i++) {

            for (j = 1; j <= n - i; j++) {
                printf(" ");
            }

            for (j = 1; j <= i; j++) {
                printf("*");
            }

            printf("\n");
        }

        return 0;
    }
    ```

22. Write a program to print the following star pattern using nested loops:

    ```
    *********
     *******
      *****
       ***
        *
       ***
      *****
     *******
    *********
    ```

    ```c
    #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the number of rows: ");
        scanf("%d", &n);

        for (i = n; i >= 1; i--) {

            for (j = 1; j <= n - i; j++) {
                printf(" ");
            }

            for (j = 1; j <= 2 * i - 1; j++) {
                printf("*");
            }

            printf("\n");
        }

        for (i = 2; i <= n; i++) {

            for (j = 1; j <= n - i; j++) {
                printf(" ");
            }

            for (j = 1; j <= 2 * i - 1; j++) {
                printf("*");
            }

            printf("\n");
        }

        return 0;
    }
    ```

23. Write a program to print the following hollow square star pattern using nested loops:

    ```
    *****
    *   *
    *   *
    *   *
    *****
    ```

    ```c
    #include <stdio.h>

    int main() {
        int i, j, n;

        printf("Enter the size of square: ");
        scanf("%d", &n);

        for (i = 1; i <= n; i++) {
            for (j = 1; j <= n; j++) {
                if (i == 1 || i == n || j == 1 || j == n)
                    printf("*");
                else
                    printf(" ");
            }
            printf("\n");
        }

        return 0;
    }
    ```

24. Write a program to print the following spiral number pattern using nested loops:

    ```
    1   2   3   4   5
    16  17  18  19  6
    15  24  25  20  7
    14  23  22  21  8
    13  12  11  10  9
    ```

    ```c
    #include <stdio.h>
    #include <stdlib.h>

    int main() {
        int n, i, j;
        int num = 1;
        int top, bottom, left, right;

        printf("Enter the size of matrix: ");
        scanf("%d", &n);

        int **a = malloc(n * sizeof(int *));

        for (i = 0; i < n; i++) {
            a[i] = malloc(n * sizeof(int));
        }

        top = 0;
        bottom = n - 1;
        left = 0;
        right = n - 1;

        while (top <= bottom && left <= right) {

            for (i = left; i <= right; i++)
                a[top][i] = num++;
            top++;

            for (i = top; i <= bottom; i++)
                a[i][right] = num++;
            right--;

            if (top <= bottom) {
                for (i = right; i >= left; i--)
                    a[bottom][i] = num++;
                bottom--;
            }

            if (left <= right) {
                for (i = bottom; i >= top; i--)
                    a[i][left] = num++;
                left++;
            }
        }

        for (i = 0; i < n; i++) {
            for (j = 0; j < n; j++) {
                printf("%-4d", a[i][j]);
            }
            printf("\n");
        }

        for (i = 0; i < n; i++) {
            free(a[i]);
        }
        free(a);

        return 0;
    }
    ```
