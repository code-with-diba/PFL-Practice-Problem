### 1. Even or odd.

```c
#include <stdio.h>

int main() {
    int num;

    printf("Enter an integer: ");
    scanf("%d", &num);

    if (num % 2 == 0) {
        printf("%d is Even.\n", num);
    } else {
        printf("%d is Odd.\n", num);
    }

    return 0;
}
```

## 2. Negative, positive, or zero

```c
#include <stdio.h>
int main() {
    int n;
    scanf("%d", &n);
    if (n > 0)
        printf("Positive\n");
    else if (n < 0)
        printf("Negative\n");
    else
        printf("Zero\n");
    return 0;
}
```

## 3. Divisible by 5 and 11

```c
#include <stdio.h>
int main() {
    int n;
    scanf("%d", &n);
    if (n % 5 == 0 && n % 11 == 0)
        printf("Divisible by 5 and 11\n");
    else
        printf("Not divisible\n");
    return 0;
}
```

### 4. Maximum between three numbers

```c
#include <stdio.h>
int main() {
    int a, b, c;
    scanf("%d %d %d", &a, &b, &c);
    if (a >= b && a >= c)
        printf("Maximum = %d\n", a);
    else if (b >= a && b >= c)
        printf("Maximum = %d\n", b);
    else
        printf("Maximum = %d\n", c);
    return 0;
}
```

## 5. Leap year check

```c
#include <stdio.h>
int main() {
    int year;
    scanf("%d", &year);
    if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0))
        printf("Leap Year\n");
    else
        printf("Not a Leap Year\n");
    return 0;
}
```

## 6. Alphabet check

```c
#include <stdio.h>
int main() {
    char ch;
    scanf("%c", &ch);
    if ((ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z'))
        printf("Alphabet\n");
    else
        printf("Not an Alphabet\n");
    return 0;
}
```

### 7. Uppercase or lowercase

```c
#include <stdio.h>
int main() {
    char ch;
    scanf("%c", &ch);
    if (ch >= 'A' && ch <= 'Z')
        printf("Uppercase\n");
    else if (ch >= 'a' && ch <= 'z')
        printf("Lowercase\n");
    else
        printf("Not an alphabet\n");
    return 0;
}
```

### 8. Write a C program to input any alphabet and check whether it is a vowel.

```c
#include <stdio.h>

int main() {
    char ch;

    printf("Enter any alphabet: ");
    scanf("%c", &ch);

    if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u' ||
        ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U') {
        printf("%c is a Vowel.\n", ch);
    } else {
        printf("%c is not a Vowel.\n", ch);
    }
}
```

### 9. Write a C program to input any alphabet and check whether it is a vowel or a consonant. (nested if-else)

```c
#include <stdio.h>

int main() {
    char ch;

    printf("Enter any alphabet: ");
    scanf("%c", &ch);

    if ((ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z')) {
        if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u' ||
            ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U') {
            printf("%c is a Vowel.\n", ch);
        } else {
            printf("%c is a Consonant.\n", ch);
        }
    } else {
        printf("%c is not an alphabet.\n", ch);
    }
}
```

## 10. Alphabet, digit, or special character

```c
#include <stdio.h>
int main() {
    char ch;
    scanf("%c", &ch);
    if ((ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z'))
        printf("Alphabet\n");
    else if (ch >= '0' && ch <= '9')
        printf("Digit\n");
    else
        printf("Special Character\n");
    return 0;
}
```

## 11. Check whether a triangle's angles form a valid triangle

```c
#include <stdio.h>
int main() {
    double a1, a2, a3;
    scanf("%lf %lf %lf", &a1, &a2, &a3);
    if (a1 > 0 && a2 > 0 && a3 > 0 && (a1 + a2 + a3 == 180))
        printf("Valid Triangle\n");
    else
        printf("Invalid Triangle\n");
    return 0;
}
```

## 13. Grade from marks (if-else)

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

## 14. Percentage and grade from three subjects

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
