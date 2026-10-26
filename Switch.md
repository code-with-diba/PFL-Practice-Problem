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
#include<stdio.h>
int main()
{
    double a,b;
    char op;
    scanf("%lf %c %lf",&a,&op,&b);

    switch(op)
    {
        case '+':
        printf("%.2lf",a+b);
        break;

        case '-':
        printf("%.2lf",a-b);
        break;

        case '*':
        printf("%.2lf",a*b);
        break;

        case '/':
         if(b!=0)
            printf("%.2lf",a/b);
         else
            printf("Cannot divide by zero");
            break;
        default:
            printf("Invalid operator");
        }
}

```

### 3.Write a C program to take an input character variable and print one of the following messages, (a) RED, if either r or R is assigned to the variable  (b) GREEN, if either g or G is assigned to the variable  (c) BLUE, if either b or B is assigned to the variable  (d) BLACK, if the variable is assigned any other character

```c
#include <stdio.h>
int main() {
    char ch;
    scanf("%c", &ch);
    switch (ch) {
        case 'r':
        case 'R':
            printf("RED");
            break;
        case 'g':
        case 'G':
            printf("GREEN");
            break;
        case 'b':
        case 'B':
            printf("BLUE");
            break;
        default:
            printf("BLACK");
    }
}
```

### 4. Write a C program using a switch-case statement to input the marks of a subject and calculate the grade according to the following:  
marks >= 90 : Grade A  
marks >= 80 : Grade B  
marks >= 70 : Grade C  
marks >= 60 : Grade D  
marks >= 40 : Grade E  
marks < 40 : Grade F

```c
#include <stdio.h>
int main() {
    double marks;
    scanf("%lf", &marks);
    switch ((int)(marks / 10)) {
        case 10:
        case 9:
            printf("Grade A");
            break;
        case 8:
            printf("Grade B");
            break;
        case 7:
            printf("Grade C");
            break;
        case 6:
            printf("Grade D");
            break;
        case 5:
        case 4:
            printf("Grade E");
            break;
        default:
            printf("Grade F");
    }
}

```
