---
layout: base
title: "Conditional Statements Solutions"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/practical/conditional-statements-solutions/"
---

# {{ page.title | escape }}

1. Write a program to check whether a number is positive, negative or zero.

    ```c
    #include <stdio.h>

    int main() {
        int num;

        printf("Enter a number: ");
        scanf("%d", &num);

        if (num > 0)
            printf("The number is positive.");
        else if (num < 0)
            printf("The number is negative.");
        else
            printf("The number is zero.");

        return 0;
    }
    ```

2. Write a program to check whether a number is even or odd.

    ```c
    #include <stdio.h>

    int main() {
        int num;

        printf("Enter a number: ");
        scanf("%d", &num);

        if (num % 2 == 0)
            printf("%d is an even number.", num);
        else
            printf("%d is an odd number.", num);

        return 0;
    }
    ```

3. Write a program to check whether a number is even or odd using bitwise operator.

    ```c
    #include <stdio.h>

    int main() {
        int num;

        printf("Enter a number: ");
        scanf("%d", &num);

        if (num & 1)
            printf("%d is an odd number.", num);
        else
            printf("%d is an even number.", num);

        return 0;
    }
    ```

4. Write a program to find the largest of two numbers.

    ```c
    #include <stdio.h>

    int main() {
        int a, b;

        printf("Enter two numbers: ");
        scanf("%d %d", &a, &b);

        if (a > b)
            printf("%d is the largest.", a);
        else if (b > a)
            printf("%d is the largest.", b);
        else
            printf("Both numbers are equal.");

        return 0;
    }
    ```

5. Write a program to find the largest of three numbers.

    ```c
    #include <stdio.h>

    int main() {
        int a, b, c;

        printf("Enter three numbers: ");
        scanf("%d %d %d", &a, &b, &c);

        if (a >= b && a >= c)
            printf("%d is the largest.", a);
        else if (b >= a && b >= c)
            printf("%d is the largest.", b);
        else
            printf("%d is the largest.", c);

        return 0;
    }
    ```

6. Write a program to find the smallest of three numbers.

    ```c
    #include <stdio.h>

    int main() {
        int a, b, c;

        printf("Enter three numbers: ");
        scanf("%d %d %d", &a, &b, &c);

        if (a <= b && a <= c)
            printf("%d is the smallest.", a);
        else if (b <= a && b <= c)
            printf("%d is the smallest.", b);
        else
            printf("%d is the smallest.", c);

        return 0;
    }
    ```

7. Write a program to check whether a year is a leap year.

    ```c
    #include <stdio.h>

    int main() {
        int year;

        printf("Enter a year: ");
        scanf("%d", &year);

        if ((year % 400 == 0) || (year % 4 == 0 && year % 100 != 0))
            printf("%d is a leap year.", year);
        else
            printf("%d is not a leap year.", year);

        return 0;
    }
    ```

8. Write a program to determine whether a character is a vowel or consonant.

    ```c
    #include <stdio.h>

    int main() {
        char ch;

        printf("Enter a character: ");
        scanf(" %c", &ch);

        if (ch == 'a' || ch == 'e' || ch == 'i' ||
            ch == 'o' || ch == 'u' ||
            ch == 'A' || ch == 'E' || ch == 'I' ||
            ch == 'O' || ch == 'U')
        {
            printf("%c is a vowel.", ch);
        }  
        else
        {
            printf("%c is a consonant.", ch);
        }

        return 0;
    }
    ```

9. Write a program to check whether a character is an uppercase letter, lowercase letter, digit or special character.

    ```c
    #include <stdio.h>

    int main() {
        char ch;

        printf("Enter a character: ");
        scanf("%c", &ch);

        if (ch >= 'A' && ch <= 'Z')
            printf("%c is a uppercase letter", ch);
        else if (ch >= 'a' && ch <= 'z')
            printf("%c is a lowercase letter", ch);
        else if (ch >= '0' && ch <= '9')
            printf("%c is a digit", ch);
        else
            printf("%c is a special character", ch);

        return 0;
    }
    ```

10. Write a program to calculate electricity bill based on slab-wise consumption.

    ```c
    #include <stdio.h>

    int main() {
        int units;
        float bill;

        const float SlAB1 = 1.50;
        const float SlAB2 = 2.50;
        const float SlAB3 = 4.00;
        const float SlAB4 = 6.00;

        printf("Enter electricity units consumed: ");
        scanf("%d", &units);

        if (units <= 100)
            bill = units * SlAB1;
        else if (units <= 200)
            bill = 100 * SlAB1 + (units - 100) * SlAB2;
        else if (units <= 500)
            bill = 100 * SlAB1 + 100 * SlAB2 + (units - 200) * SlAB3;
        else
            bill = 100 * SlAB1 + 100 * SlAB2 + 300 * SlAB3 + (units - 500) * SlAB4;

        printf("Electricity Bill = Rs. %.2f", bill);

        return 0;
    }
    ```