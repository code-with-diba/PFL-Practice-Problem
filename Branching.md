## 1. Maximum between three numbers

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

## 4. Even or odd

```c
#include <stdio.h>
int main() {
    int n;
    scanf("%d", &n);
    if (n % 2 == 0)
        printf("Even\n");
    else
        printf("Odd\n");
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

## 7. Vowel or consonant

```c
#include <stdio.h>
int main() {
    char ch;
    scanf("%c", &ch);
    if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u' || 
        ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U')
        printf("Vowel\n");
    else
        printf("Consonant\n");
    return 0;
}
```

## 8. Alphabet, digit, or special character

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

## 9. Uppercase or lowercase

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

## 10. Week number to weekday name

```c
#include <stdio.h>
int main() {
    int week;
    scanf("%d", &week);
    if (week == 1)
        printf("Sunday\n");
    else if (week == 2)
        printf("Monday\n");
    else if (week == 3)
        printf("Tuesday\n");
    else if (week == 4)
        printf("Wednesday\n");
    else if (week == 5)
        printf("Thursday\n");
    else if (week == 6)
        printf("Friday\n");
    else if (week == 7)
        printf("Saturday\n");
    else
        printf("Invalid Input\n");
    return 0;
}
```

## 11. Count total number of notes in a given amount

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
}
```

## 12. Check whether a triangle's angles form a valid triangle

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
