### 1. Weekday name using switch case

```c
#include <stdio.h>
int main() {
    int day;
    scanf("%d", &day);
    switch (day)
    {
        case 1:
            printf("Sunday");
            break;
        case 2:
            printf("Monday");
            break;
        case 3:
            printf("Tuesday");
            break;
        case 4:
            printf("Wednesday");
            break;
        case 5:
            printf("Thursday");
            break;
        case 6:
            printf("Friday");
            break;
        case 7:
            printf("Saturday");
            break;
        default:
            printf("Invalid day");
    }
}

```

### 2. Simple calculator using switch case

```c
#include <stdio.h>
int main() {
    double a, b, result;
    char op;
    scanf("%lf %c %lf", &a, &b);
    switch (op) {
        case '+': result = a + b; break;
        case '-': result = a - b; break;
        case '*': result = a * b; break;
        case '/':
            if (b == 0) {
                printf("Division by zero error\n");
                return 0;
            }
            result = a / b;
            break;
        default:
            printf("Invalid operator\n");
            return 0;
    }
    printf("Result = %.2lf\n", result);
    return 0;
}
```

### 3. RED, GREEN, BLUE, BLACK message using switch case

```c
#include <stdio.h>
int main() {
    char ch;
    scanf("%c", &ch);
    switch (ch) {
        case 'r':
        case 'R':
            printf("RED\n");
            break;
        case 'g':
        case 'G':
            printf("GREEN\n");
            break;
        case 'b':
        case 'B':
            printf("BLUE\n");
            break;
        default:
            printf("BLACK\n");
    }
    return 0;
}
```

### 4. Grade using switch case

```c
#include <stdio.h>
int main() {
    double marks;
    scanf("%lf", &marks);
    switch ((int)(marks / 10)) {
        case 10:
        case 9:
            printf("Grade A\n");
            break;
        case 8:
            printf("Grade B\n");
            break;
        case 7:
            printf("Grade C\n");
            break;
        case 6:
            printf("Grade D\n");
            break;
        case 5:
        case 4:
            printf("Grade E\n");
            break;
        default:
            printf("Grade F\n");
    }
    return 0;
}
```
