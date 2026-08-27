---
layout: base
title: "Basic Input/Output Solutions"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/practical/basic-input-output-solutions/"
---

# {{ page.title | escape }}

1. Write a C program to read an integer and display it.

    ```c
    #include <stdio.h>

    int main() {
        int num;

        printf("Enter an integer: ");
        scanf("%d", &num);

        printf("The entered integer is: %d\n", num);

        return 0;
    }
    ```

2. Read two integers and display their sum, difference, product and quotient.

    ```c
    #include <stdio.h>

    int main() {
        int a, b;

        printf("Enter two integers: ");
        scanf("%d %d", &a, &b);

        printf("Sum = %d\n", a + b);
        printf("Difference = %d\n", a - b);
        printf("Product = %d\n", a * b);
        printf("Quotient = %d\n", a / b);

        return 0;
    }
    ```

3. Read the radius of a circle and calculate its area and circumference.

    ```c
    #include <stdio.h>

    int main() {
        float radius, area, circumference;
        const float PI = 3.14159;

        printf("Enter the radius of the circle: ");
        scanf("%f", &radius);

        area = PI * radius * radius;
        circumference = 2 * PI * radius;

        printf("Area = %.2f\n", area);
        printf("Circumference = %.2f\n", circumference);

        return 0;
    }
    ```

4. Read the length and breadth of a rectangle and calculate its area and perimeter.

    ```c
    #include <stdio.h>

    int main() {
        float length, breadth, area, perimeter;

        printf("Enter the length of the rectangle: ");
        scanf("%f", &length);

        printf("Enter the breadth of the rectangle: ");
        scanf("%f", &breadth);

        area = length * breadth;
        perimeter = 2 * (length + breadth);

        printf("Area = %.2f\n", area);
        printf("Perimeter = %.2f\n", perimeter);

        return 0;
    }
    ```

5. Convert Celsius to Fahrenheit.

    ```c
    #include <stdio.h>

    int main() {
        float celsius, fahrenheit;

        printf("Enter temperature in Celsius: ");
        scanf("%f", &celsius);

        fahrenheit = (celsius * 9 / 5) + 32;

        printf("Temperature in Fahrenheit = %.2f\n", fahrenheit);

        return 0;
    }
    ```

6. Convert Fahrenheit to Celsius.

    ```c
    #include <stdio.h>

    int main() {
        float fahrenheit, celsius;

        printf("Enter temperature in Fahrenheit: ");
        scanf("%f", &fahrenheit);

        celsius = (fahrenheit - 32) * 5 / 9;

        printf("Temperature in Celsius = %.2f\n", celsius);

        return 0;
    }
    ```

7. Convert kilometres into metres, centimetres and millimetres.

    ```c
    #include <stdio.h>

    int main() {
        float km, metres, centimetres, millimetres;

        printf("Enter distance in kilometres: ");
        scanf("%f", &km);

        metres = km * 1000;
        centimetres = km * 100000;
        millimetres = km * 1000000;

        printf("Metres = %.2f\n", metres);
        printf("Centimetres = %.2f\n", centimetres);
        printf("Millimetres = %.2f\n", millimetres);

        return 0;
    }
    ```

8. Convert a given number of seconds into hours, minutes and seconds.

    ```c
    #include <stdio.h>

    int main() {
        int totalSeconds, hours, minutes, seconds;

        printf("Enter the number of seconds: ");
        scanf("%d", &totalSeconds);

        hours = totalSeconds / 3600;
        totalSeconds = totalSeconds % 3600;
        minutes = totalSeconds / 60;
        seconds = totalSeconds % 60;

        printf("Hours = %d\n", hours);
        printf("Minutes = %d\n", minutes);
        printf("Seconds = %d\n", seconds);

        return 0;
    }
    ```

9. Calculate simple interest.

    ```c
    #include <stdio.h>

    int main() {
        float principal, rate, time, simpleInterest;

        printf("Enter principal amount: ");
        scanf("%f", &principal);

        printf("Enter rate of interest: ");
        scanf("%f", &rate);

        printf("Enter time in years: ");
        scanf("%f", &time);

        simpleInterest = (principal * rate * time) / 100;

        printf("Simple Interest = %.2f\n", simpleInterest);

        return 0;
    }
    ```

10. Calculate compound interest.

    ```c
    #include <stdio.h>
    #include <math.h>

    int main() {
        float principal, rate, time, amount, compoundInterest;

        printf("Enter principal amount: ");
        scanf("%f", &principal);

        printf("Enter rate of interest: ");
        scanf("%f", &rate);

        printf("Enter time in years: ");
        scanf("%f", &time);

        amount = principal * pow((1 + rate / 100), time);
        compoundInterest = amount - principal;

        printf("Compound Interest = %.2f\n", compoundInterest);
        printf("Total Amount = %.2f\n", amount);

        return 0;
    }
    ```