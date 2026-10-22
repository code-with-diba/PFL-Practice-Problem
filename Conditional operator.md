## 1. Maximum between two numbers using conditional operator

```c
#include <stdio.h>
int main() {
    int a, b, max;
    scanf("%d %d", &a, &b);
    max = (a > b) ? a : b;
    printf("Maximum = %d\n", max);
    return 0;
}
```

## 2. Maximum between three numbers using conditional operator

```c
#include <stdio.h>
int main() {
    int a, b, c, max;
    scanf("%d %d %d", &a, &b, &c);
    max = (a > b) ? ((a > c) ? a : c) : ((b > c) ? b : c);
    printf("Maximum = %d\n", max);
    return 0;
}
```

## 3. Even or odd using conditional operator

```c
#include <stdio.h>
int main() {
    int n;
    scanf("%d", &n);
    printf("%s\n", (n % 2 == 0) ? "Even" : "Odd");
    return 0;
}
```

## 4. Leap year using conditional operator

```c
#include <stdio.h>
int main() {
    int year;
    scanf("%d", &year);
    int isLeap = ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0));
    printf("%s\n", isLeap ? "Leap year" : "Not leap year");
    return 0;
}
```

## 5. Alphabet check using conditional operator

```c
#include <stdio.h>
int main() {
    char ch;
    scanf("%c", &ch);
    int isAlpha = ((ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z'));
    printf("%s\n", isAlpha ? "Alphabet" : "Not alphabet");
    return 0;
}
```
