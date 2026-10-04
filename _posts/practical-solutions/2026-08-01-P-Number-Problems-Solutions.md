---
layout: base
title: "Number Problems Solutions"
date: 2026-06-29 09:00:00 +0530
categories: jekyll update
permalink: "/practical/number-problems-solutions/"
---

# {{ page.title | escape }}

## Digit Extraction

1. Extract the digits of an integer from right to left.

    Example:
    ```
    Input: 12345
    Output: 5 4 3 2 1
    ```

    ```c
    #include <stdio.h>

    int main() {
        int n, digit;

        printf("Enter an integer: ");
        scanf("%d", &n);

        while (n > 0) {
            digit = n % 10;
            printf("%d ", digit);
            n = n / 10;
        }

        return 0;
    }
    ```

2. Extract the digits of an integer from left to right.

    Example:
    ```c
    Input: 12345
    Output: 1 2 3 4 5
    ```

    ```c
    #include <stdio.h>

    int main() {
        int n, divisor = 1, digit;

        printf("Enter an integer: ");
        scanf("%d", &n);

        while (n / divisor >= 10) {
            divisor = divisor * 10;
        }

        while (divisor > 0) {
            digit = n / divisor;
            printf("%d ", digit);

            n = n % divisor;
            divisor = divisor / 10;
        }

        return 0;
    }
    ```

3. Count the number of digits in an integer.

    ```c
    #include <stdio.h>

    int main() {
        int n, count = 0;

        printf("Enter an integer: ");
        scanf("%d", &n);

        while (n != 0) {
            n = n / 10;
            count++;
        }

        printf("Number of digits = %d", count);

        return 0;
    }
    ```

4. Find the largest and smallest digit

    ```c
    #include <stdio.h>

    int main() {
        int n, digit;
        int largest = 0;
        int smallest = 9;

        printf("Enter an integer: ");
        scanf("%d", &n);

        if (n < 0)
            n = -n;

        if (n == 0) {
            largest = 0;
            smallest = 0;
        } else {
            while (n > 0) {
                digit = n % 10;

                if (digit > largest)
                    largest = digit;

                if (digit < smallest)
                    smallest = digit;

                n = n / 10;
            }
        }

        printf("Largest digit = %d\n", largest);
        printf("Smallest digit = %d\n", smallest);

        return 0;
    }
    ```

5. Count the number of even and odd digits.

    ```c
    #include <stdio.h>

    int main() {
        int n, digit;
        int even = 0, odd = 0;

        printf("Enter an integer: ");
        scanf("%d", &n);

        if (n < 0)
            n = -n;

        if (n == 0) {
            even = 1;
        } else {
            while (n > 0) {
                digit = n % 10;

                if (digit % 2 == 0)
                    even++;
                else
                    odd++;

                n = n / 10;
            }
        }

        printf("Even digits = %d\n", even);
        printf("Odd digits = %d\n", odd);

        return 0;
    }
    ```

## Number Reversal & Palindrome

1. Reverse an integer.

    ```c
    #include <stdio.h>

    int main() {
        int n, digit, reverse = 0;

        printf("Enter an integer: ");
        scanf("%d", &n);

        while (n != 0) {
            digit = n % 10;
            reverse = reverse * 10 + digit;
            n = n / 10;
        }

        printf("Reversed integer = %d\n", reverse);

        return 0;
    }
    ```
2. Check whether an integer is a palindrome.

    ```c
    #include <stdio.h>

    int main() {
        int n, original, digit, reverse = 0;

        printf("Enter an integer: ");
        scanf("%d", &n);

        original = n;

        if (n < 0)
            n = -n;

        while (n != 0) {
            digit = n % 10;
            reverse = reverse * 10 + digit;
            n = n / 10;
        }

        if (original < 0)
            reverse = -reverse;

        if (original == reverse)
            printf("Palindrome\n");
        else
            printf("Not Palindrome\n");

        return 0;
    }
    ```

## Prime Numbers

1. Check whether a number is prime or not.

    ```c
    #include <stdio.h>

    int main() {
        int n, i, isPrime = 1;

        printf("Enter an integer: ");
        scanf("%d", &n);

        if (n <= 1) {
            isPrime = 0;
        } else {
            for (i = 2; i < n; i++) {
                if (n % i == 0) {
                    isPrime = 0;
                    break;
                }
            }
        }

        if (isPrime)
            printf("Prime\n");
        else
            printf("Not Prime\n");

        return 0;
    }
    ```

2. Display all prime numbers within a given range.

    ```c
    #include <stdio.h>

    int main() {
        int start, end, i, j, isPrime;

        printf("Enter starting number: ");
        scanf("%d", &start);

        printf("Enter ending number: ");
        scanf("%d", &end);

        for (i = start; i <= end; i++) {
            if (i < 2)
                continue;

            isPrime = 1;

            for (j = 2; j * j <= i; j++) {
                if (i % j == 0) {
                    isPrime = 0;
                    break;
                }
            }

            if (isPrime)
                printf("%d ", i);
        }

        return 0;
    }
    ```

## Prime Factors

1. Find the prime factors of a number.

    ```c
    #include <stdio.h>

    int main() {
        int n, i;

        printf("Enter an integer: ");
        scanf("%d", &n);

        printf("Prime factors: ");

        for (i = 2; i <= n; i++) {
            while (n % i == 0) {
                printf("%d ", i);
                n = n / i;
            }
        }

        return 0;
    }
    ```

2. Find the number of distinct prime factors.

    ```c
    #include <stdio.h>

    int main() {
        int n, i, count = 0;

        printf("Enter an integer: ");
        scanf("%d", &n);

        for (i = 2; i <= n; i++) {
            if (n % i == 0) {
                count++;

                while (n % i == 0) {
                    n = n / i;
                }
            }
        }

        printf("Number of distinct prime factors = %d\n", count);

        return 0;
    }
    ```

## Perfect Numbers

1. Check whether a number is a perfect number.

    ```c
    #include <stdio.h>

    int main() {
        int n, i, sum = 0;

        printf("Enter an integer: ");
        scanf("%d", &n);

        for (i = 1; i < n; i++) {
            if (n % i == 0) {
                sum = sum + i;
            }
        }

        if (sum == n)
            printf("Perfect Number\n");
        else
            printf("Not a Perfect Number\n");

        return 0;
    }
    ```

2. Display all perfect numbers up to $n$.

    ```c
    #include <stdio.h>

    int main() {
        int n, num, i, sum;

        printf("Enter the value of n: ");
        scanf("%d", &n);

        printf("Perfect numbers up to %d are: ", n);

        for (num = 1; num <= n; num++) {
            sum = 0;

            for (i = 1; i < num; i++) {
                if (num % i == 0) {
                    sum = sum + i;
                }
            }

            if (sum == num) {
                printf("%d ", num);
            }
        }

        return 0;
    }
    ```

## Armstrong Numbers

1. Check whether a number is an Armstrong number.

    ```c
    #include <stdio.h>

    int main() {
        int n, original, digit;
        int digits = 0, sum = 0, power, i;

        printf("Enter an integer: ");
        scanf("%d", &n);

        original = n;

        if (n < 0)
            n = -n;

        if (n == 0) {
            digits = 1;
        } else {
            int temp = n;

            while (temp > 0) {
                digits++;
                temp = temp / 10;
            }
        }

        int temp = n;

        while (temp > 0) {
            digit = temp % 10;

            power = 1;

            for (i = 1; i <= digits; i++) {
                power = power * digit;
            }

            sum = sum + power;
            temp = temp / 10;
        }

        if (sum == n)
            printf("Armstrong Number\n");
        else
            printf("Not an Armstrong Number\n");

        return 0;
    }
    ```

2. Display all Armstrong numbers between 1 and $n$.

    ```c
    #include <stdio.h>

    int main() {
        int n, num, temp, digit;
        int digits, sum, power, i;

        printf("Enter the value of n: ");
        scanf("%d", &n);

        printf("Armstrong numbers between 1 and %d are:\n", n);

        for (num = 1; num <= n; num++) {

            temp = num;
            digits = 0;

            while (temp > 0) {
                digits++;
                temp = temp / 10;
            }

            temp = num;
            sum = 0;

            while (temp > 0) {
                digit = temp % 10;

                power = 1;

                for (i = 1; i <= digits; i++) {
                    power = power * digit;
                }

                sum = sum + power;
                temp = temp / 10;
            }

            if (sum == num) {
                printf("%d ", num);
            }
        }

        return 0;
    }
    ```

## Amicable Numbers

1. Check whether two numbers are amicable.

    ```c
    #include <stdio.h>

    int main() {
        int a, b, i;
        int sumA = 0, sumB = 0;

        printf("Enter two integers: ");
        scanf("%d %d", &a, &b);

        for (i = 1; i < a; i++) {
            if (a % i == 0) {
                sumA = sumA + i;
            }
        }

        for (i = 1; i < b; i++) {
            if (b % i == 0) {
                sumB = sumB + i;
            }
        }

        if (sumA == b && sumB == a)
            printf("Amicable Numbers\n");
        else
            printf("Not Amicable Numbers\n");

        return 0;
    }
    ```

2. Display all amicable pairs within a given range.

    ```c
    #include <stdio.h>

    int main() {
        int start, end;
        int a, b, i;
        int sumA, sumB;

        printf("Enter the range: ");
        scanf("%d %d", &start, &end);

        printf("Amicable pairs:\n");

        for (a = start; a <= end; a++) {

            sumA = 0;

            for (i = 1; i < a; i++) {
                if (a % i == 0) {
                    sumA = sumA + i;
                }
            }

            b = sumA;

            if (b > a && b <= end) {

                sumB = 0;

                for (i = 1; i < b; i++) {
                    if (b % i == 0) {
                        sumB = sumB + i;
                    }
                }

                if (sumB == a) {
                    printf("%d %d\n", a, b);
                }
            }
        }

        return 0;
    }
    ```

## Factorial

1. Calculate factorial using do-while.

    ```c
    #include <stdio.h>

    int main() {
        int n, i = 1;
        long long factorial = 1;

        printf("Enter a number: ");
        scanf("%d", &n);

        if (n < 0) {
            printf("Factorial is not possible for negative numbers.");
        }
        else {
            do {
                factorial = factorial * i;
                i++;
            } while (i <= n);

            printf("Factorial = %lld", factorial);
        }

        return 0;
    }
    ```

2. Calculate $^{n}C_{r}$ using factorials.

    ```c
    #include <stdio.h>

    int main() {
        int n, r, i;
        long long nFact = 1, rFact = 1, nrFact = 1;
        long long combination;

        printf("Enter n and r: ");
        scanf("%d %d", &n, &r);

        if (r < 0 || r > n) {
            printf("Invalid input");
        }
        else {
            for (i = 1; i <= n; i++) {
                nFact = nFact * i;
            }

            for (i = 1; i <= r; i++) {
                rFact = rFact * i;
            }

            for (i = 1; i <= n - r; i++) {
                nrFact = nrFact * i;
            }

            combination = nFact / (rFact * nrFact);

            printf("nCr = %lld", combination);
        }

        return 0;
    }
    ```

3. Calculate $^{n}P_{r}$ using factorials.

    ```c
    #include <stdio.h>

    int main() {
        int n, r, i;
        long long nFact = 1, nrFact = 1;
        long long permutation;

        printf("Enter n and r: ");
        scanf("%d %d", &n, &r);

        if (r < 0 || r > n) {
            printf("Invalid input");
        }
        else {
            for (i = 1; i <= n; i++) {
                nFact = nFact * i;
            }

            for (i = 1; i <= n - r; i++) {
                nrFact = nrFact * i;
            }

            permutation = nFact / nrFact;

            printf("nPr = %lld", permutation);
        }

        return 0;
    }
    ```

## Number Base Conversion

1. Convert decimal to binary.

    ```c
    #include <stdio.h>

    int main() {
        int n, remainder;
        long long binary = 0, place = 1;

        printf("Enter a decimal number: ");
        scanf("%d", &n);

        if (n == 0) {
            printf("Binary = 0");
        } else {
            while (n > 0) {
                remainder = n % 2;
                binary = binary + remainder * place;
                place = place * 10;
                n = n / 2;
            }

            printf("Binary = %lld", binary);
        }

        return 0;
    }
    ```

2. Convert decimal to octal.

    ```c
    #include <stdio.h>

    int main() {
        int n, remainder;
        int octal = 0, place = 1;

        printf("Enter a decimal number: ");
        scanf("%d", &n);

        if (n == 0) {
            printf("Octal = 0");
        } else {
            while (n > 0) {
                remainder = n % 8;
                octal = octal + remainder * place;
                place = place * 10;
                n = n / 8;
            }

            printf("Octal = %d", octal);
        }

        return 0;
    }
    ```

3. Convert decimal to hexadecimal.

    ```c
    #include <stdio.h>

    int main() {
        int n, remainder;
        char hex[20];
        int i = 0, j;

        printf("Enter a decimal number: ");
        scanf("%d", &n);

        if (n == 0) {
            printf("Hexadecimal = 0");
        } else {
            while (n > 0) {
                remainder = n % 16;

                if (remainder < 10)
                    hex[i] = remainder + '0';
                else
                    hex[i] = remainder - 10 + 'A';

                i++;
                n = n / 16;
            }

            printf("Hexadecimal = ");

            for (j = i - 1; j >= 0; j--) {
                printf("%c", hex[j]);
            }
        }

        return 0;
    }
    ```

4. Convert binary to hexadecimal.

    ```c
    #include <stdio.h>

    int main() {
        long long binary;
        int digit, decimal = 0, base = 1, remainder;
        char hex[20];
        int i = 0, j;

        printf("Enter binary number: ");
        scanf("%lld", &binary);

        while (binary > 0) {
            digit = binary % 10;
            decimal = decimal + digit * base;
            base = base * 2;
            binary = binary / 10;
        }

        if (decimal == 0) {
            printf("Hexadecimal = 0");
        } else {
            while (decimal > 0) {
                remainder = decimal % 16;

                if (remainder < 10)
                    hex[i] = remainder + '0';
                else
                    hex[i] = remainder - 10 + 'A';

                i++;
                decimal = decimal / 16;
            }

            printf("Hexadecimal = ");

            for (j = i - 1; j >= 0; j--)
                printf("%c", hex[j]);
        }

        return 0;
    }
    ```