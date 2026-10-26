### 1. Even or odd.

```c
#include <stdio.h>

int main() {
    int num;

    scanf("%d", &num);

    if (num % 2 == 0)
          printf("Even");
    else
          printf("Odd");
}

```

## 2. Negative, positive, or zero

```c
#include <stdio.h>
int main() {
    int n;
    scanf("%d", &n);
    if (n > 0)
        printf("Positive");
    else if (n < 0)
        printf("Negative");
    else
        printf("Zero");
}

```

## 3. Divisible by 5 and 11

```c
#include <stdio.h>
int main() {
    int n;
    scanf("%d", &n);
    if (n % 5 == 0 && n % 11 == 0)
        printf("Divisible");
    else
        printf("Not divisible");
}

```

### 4. Maximum between three numbers(Nested if-else)

```c
#include <stdio.h>
int main() {
    int a, b, c;
    scanf("%d %d %d", &a, &b, &c);

    if (a >= b) {
        if (a >= c)
            printf("Maximum = %d", a);
         else
            printf("Maximum = %d", c);
    }
    else {
        if (b >= c)
            printf("Maximum = %d", b);
         else
            printf("Maximum = %d", c);
    }
}

```

## 5. Leap year check

```c
#include <stdio.h>
int main() {
    int y;
    scanf("%d", &y);
    if ((y % 4 == 0 && y % 100 != 0) || (y % 400 == 0))
        printf("Leap Year");
    else
        printf("Not a Leap Year");
}

```

## 6. Alphabet check

```c
#include <stdio.h>
int main() {
    char ch;
    scanf("%c", &ch);
    if ((ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z'))
        printf("Alphabet");
    else
        printf("Not an Alphabet");
}
```

### 7. Uppercase or lowercase(Nested if-else)

```c
#include <stdio.h>

int main() {
    char ch;
    scanf("%c", &ch);

    if ((ch >= 'A' && ch <= 'Z') || (ch >= 'a' && ch <= 'z')){

        if (ch >= 'A' && ch <= 'Z')
            printf("Uppercase");
         else
            printf("Lowercase");
    }
        else
        printf("%c is not a valid alphabet letter.\n", ch);
}
```

### 8. Write a C program to input any alphabet and check whether it is a vowel.

```c
#include <stdio.h>

int main() {
    char ch;
    scanf("%c", &ch);

    if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u' ||
        ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U')
        printf("Vowel");
     else
        printf("Not a Vowel");
}

```

### 9. Write a C program to input any alphabet and check whether it is a vowel or a consonant. (nested if-else)

```c
#include <stdio.h>
int main() {
    char ch;
    scanf("%c", &ch);

    if ((ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z')) {
        if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u' ||
            ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U')
            printf("Vowel");
         else
            printf("Consonant");
    }
     else
        printf("Not an alphabet");
}

```

## 10. Alphabet, digit, or special character

```c
#include <stdio.h>
int main() {
    char ch;
    scanf("%c", &ch);
    if ((ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z'))
        printf("Alphabet");
    else if (ch >= '0' && ch <= '9')
        printf("Digit");
    else
        printf("Special Character");
}

```

## 11. Check whether a triangle's angles form a valid triangle

```c
#include <stdio.h>
int main() {
    double a1, a2, a3;
    scanf("%lf %lf %lf", &a1, &a2, &a3);
    if (a1 > 0 && a2 > 0 && a3 > 0 && (a1 + a2 + a3 == 180))
        printf("Valid Triangle");
    else
        printf("Invalid Triangle");
}
```

### 12. Write a C program to check whether the triangle is equilateral, isosceles, or scalene.

```c
#include <stdio.h>

int main() {
    double a, b, c;
    scanf("%lf %lf %lf", &a, &b, &c);

    if (a + b > c && a + c > b && b + c > a) {
        if (a == b && b == c) 
            printf("Equilateral");
         else if (a == b || a == c || b == c) 
            printf("Isosceles");
         else 
            printf("Scalene");
    } 
        else 
        printf("The triangle is not valid");
}
```

### 12. Write a C program to check whether the triangle is equilateral, isosceles, or scalene.

```c
#include <stdio.h>

int main() {
    float a, b, c;

    printf("Enter three sides of the triangle: ");
    scanf("%f %f %f", &a, &b, &c);

    if (a + b > c && a + c > b && b + c > a) {
        if (a == b && b == c) {
            printf("The triangle is an Equilateral triangle.\n");
        } else if (a == b || a == c || b == c) {
            printf("The triangle is an Isosceles triangle.\n");
        } else {
            printf("The triangle is a Scalene triangle.\n");
        }
    } else {
        printf("The triangle is not valid.\n");
    }

    return 0;
}
```

## 14. Grade from marks 

```c
#include <stdio.h>
int main() {
    double marks;
    scanf("%lf", &marks);
    if (marks >= 90)
        printf("Grade A\n");
    else if (marks >= 80)
        printf("Grade B\n");
    else if (marks >= 70)
        printf("Grade C\n");
    else if (marks >= 60)
        printf("Grade D\n");
    else if (marks >= 40)
        printf("Grade E\n");
    else
        printf("Grade F\n");
    return 0;
}
```

## 15. Percentage and grade from three subjects

```c
#include <stdio.h>
int main() {
    double physics, maths, chemistry;
    scanf("%lf %lf %lf", &physics, &maths, &chemistry);
    double percentage = ((physics + maths + chemistry) / 3.0);
    printf("Percentage = %.2lf\n", percentage);
    if (percentage >= 90)
        printf("Grade A\n");
    else if (percentage >= 80)
        printf("Grade B\n");
    else if (percentage >= 70)
        printf("Grade C\n");
    else if (percentage >= 60)
        printf("Grade D\n");
    else if (percentage >= 40)
        printf("Grade E\n");
    else
        printf("Grade F\n");
    return 0;
}
```

## 16. Count total number of notes in a given amount

```c
#include <stdio.h>
int main() {
    int amount;
    scanf("%d", &amount);
    int notes[] = {500, 100, 50, 20, 10, 5, 2, 1};
    int n = 8;
    for (int i = 0; i < n; i++) {
        int count = amount / notes[i];
        amount = amount % notes[i];
        if (count > 0)
            printf("Notes of %d = %d\n", notes[i], count);
    }
    return 0;
}
```
