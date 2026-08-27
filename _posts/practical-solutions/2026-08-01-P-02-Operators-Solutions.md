---
layout: base
title: "Operators Solutions"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/practical/operators-solutions/"
---

# {{ page.title | escape }}

1. Demonstrate all arithmetic operators in C.

    ```c
    #include <stdio.h>

    int main(){
        int num1, num2;
        printf("Enter Two Numbers:\n");
        scanf("%d %d", &num1, &num2);
        printf("\n");

        int add = num1 + num2;
        int sub = num1 - num2;
        int mul = num1 * num2;
        int div = num1 / num2;
        int mod = num1 % num2;

        printf("%d + %d = %d\n", num1, num2, add);
        printf("%d - %d = %d\n", num1, num2, sub);
        printf("%d * %d = %d\n", num1, num2, mul);
        printf("%d / %d = %d\n", num1, num2, div);
        printf("%d %% %d = %d\n", num1, num2, mod);

        return 0;
    }
    ```

2. Demonstrate relational operators using two numbers.

    ```c
    #include <stdio.h>

    int main(){
        int num1, num2;
        printf("Enter Two Numbers:\n");
        scanf("%d %d", &num1, &num2);
        printf("\n");

        int eq = num1 == num2;
        int neq = num1 != num2;
        int gt = num1 > num2;
        int lt = num1 < num2;
        int gte = num1 >= num2;
        int lte = num1 <= num2;

        printf("%d == %d : %d\n", num1, num2, eq);
        printf("%d != %d : %d\n", num1, num2, neq);
        printf("%d > %d  : %d\n", num1, num2, gt);
        printf("%d < %d  : %d\n", num1, num2, lt);
        printf("%d >= %d : %d\n", num1, num2, gte);
        printf("%d <= %d : %d\n", num1, num2, lte);

        return 0;
    }
    ```

3. Write a program to check whether a number lies within a specified range.

    ```c
    #include<stdio.h>

    int main(){
        int num, low, high;
        printf("Enter The Range: \n");

        printf("Enter lower range: ");
        scanf("%d", &low);

        printf("Enter higher range: ");
        scanf("%d", &high);

        printf("Enter the number: ");
        scanf("%d", &num);

        if(num >= low && num <= high){
            printf("%d lies within the specified range: %d to %d.\n", num, low, high);
        }
        else{
            printf("%d does not lie within the specified range: %d to %d.\n", num, low, high);
        }

        return 0;
    }
    ```

4. Write a program to swap two numbers using a temporary variable.

    ```c
    #include <stdio.h>

    int main(){
        int num1, num2;
        printf("Enter First Number: ");
        scanf("%d", &num1);
        printf("Enter Second Number: ");
        scanf("%d", &num2);
        printf("\n");
        int temp;

        printf("BEFORE SWAP:\n");
        printf("First Number: %d\n", num1);
        printf("Second Number: %d\n\n", num2);

        temp = num1;
        num1 = num2;
        num2 = temp;

        printf("AFTER SWAP:\n");
        printf("First Number: %d\n", num1);
        printf("Second Number: %d\n", num2);

        return 0;
    }
    ```

5. Write a program to swap two numbers without using a third variable.

    ```c
    #include <stdio.h>

    int main(){
        int num1, num2;
        printf("Enter First Number: ");
        scanf("%d", &num1);
        printf("Enter Second Number: ");
        scanf("%d", &num2);
        printf("\n");

        printf("BEFORE SWAP:\n");
        printf("First Number: %d\n", num1);
        printf("Second Number: %d\n\n", num2);

        num1 = num1 + num2;
        num2 = num1 - num2;
        num1 = num1 - num2;

        printf("AFTER SWAP:\n");
        printf("First Number: %d\n", num1);
        printf("Second Number: %d\n", num2);

        return 0;
    }
    ```