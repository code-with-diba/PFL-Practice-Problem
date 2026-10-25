### 1. Sum of two numbers

```c
#include <stdio.h>

int main() {
    double a, b;
    scanf("%lf %lf", &a, &b);
    printf("Sum = %.2lf", a + b);
}
```

### 2. Two numbers, all arithmetic operations

```c
#include <stdio.h>

int main() {
    double a, b;
    scanf("%lf %lf", &a, &b);
    printf("Sum = %.2lf\n", a + b);
    printf("Difference = %.2lf\n", a - b);
    printf("Product = %.2lf\n", a * b);
    if (b != 0)
        printf("Quotient = %.2lf\n", a / b);
    else
        printf("Division by zero error\n");
}
```

### 3. Swap two variables using a temporary variable

```c
#include <stdio.h>

int main() {
    int a, b, temp;
    scanf("%d %d", &a, &b);
    temp = a;
    a = b;
    b = temp;
    printf("a = %d, b = %d", a, b);
}

```

### 4. Swap two variables without a temporary variable

```c
#include <stdio.h>

int main() {
    int a, b;
    scanf("%d %d", &a, &b);
    a = a + b;
    b = a - b;
    a = a - b;
    printf("a = %d, b = %d", a, b);
}
```

### 5. Perimeter of a rectangle

```c
include <stdio.h>

int main() {
    double length, breadth;
    scanf("%lf %lf", &length, &breadth);
    printf("Perimeter = %.2lf", 2 * (length + breadth));

}

```

### 6. Area of a rectangle

```c
#include <stdio.h>

int main() {
    double length, breadth;
    scanf("%lf %lf", &length, &breadth);
    printf("Area = %.2lf", length * breadth);
}
```

### 7. Diameter, circumference, area of a circle

```c
#include <stdio.h>
#define PI 3.14159265

int main() {
    double radius;
    scanf("%lf", &radius);
    printf("Diameter = %.2lf\n", 2 * radius);
    printf("Circumference = %.2lf\n", 2 * PI * radius);
    printf("Area = %.2lf\n", PI * radius * radius);
    return 0;
}
```

### 8. Centimeters to meters and kilometers

```c
#include <stdio.h>

int main() {
    double cm;
    scanf("%lf", &cm);
    printf("Meters = %.4lf\n", cm / 100.0);
    printf("Kilometers = %.6lf\n", cm / 100000.0);
    return 0;
}
```

### 9. Celsius to Fahrenheit

```c
#include <stdio.h>

int main() {
    double celsius;
    scanf("%lf", &celsius);
    printf("Fahrenheit = %.2lf\n", (celsius * 9 / 5) + 32);
    return 0;
}
```

### 10. Fahrenheit to Celsius

```c
#include <stdio.h>

int main() {
    double fahrenheit;
    scanf("%lf", &fahrenheit);
    printf("Celsius = %.2lf\n", (fahrenheit - 32) * 5 / 9);
    return 0;
}
```

### 11. Days into years, weeks and days

```c
#include <stdio.h>

int main() {
    int totalDays, years, weeks, days;
    scanf("%d", &totalDays);
    years = totalDays / 365;
    days = totalDays % 365;
    weeks = days / 7;
    days = days % 7;
    printf("%d years, %d weeks, %d days\n", years, weeks, days);
    return 0;
}
```

### 12. Power of a number x^y

```c
#include <stdio.h>
#include <math.h>

int main() {
    double x, y;
    scanf("%lf %lf", &x, &y);
    printf("Result = %.4lf\n", pow(x, y));
    return 0;
}
```

### 13. Square root of a number

```c
#include <stdio.h>
#include <math.h>

int main() {
    double n;
    scanf("%lf", &n);
    printf("Square root = %.4lf\n", sqrt(n));
    return 0;
}
```

### 14. Third angle of a triangle

```c
#include <stdio.h>

int main() {
    double angle1, angle2, angle3;
    scanf("%lf %lf", &angle1, &angle2);
    angle3 = 180 - angle1 - angle2;
    printf("Third angle = %.2lf\n", angle3);
    return 0;
}
```

### 15. Area of a triangle 

```c
#include <stdio.h>

int main() {
    double base, height;
    scanf("%lf %lf", &base, &height);
    printf("Area = %.2lf\n", 0.5 * base * height);
    return 0;
}
```

### 16. Area of an equilateral triangle

```c
#include <stdio.h>
#include <math.h>

int main() {
    double side;
    scanf("%lf", &side);
    printf("Area = %.4lf\n", (sqrt(3) / 4) * side * side);
    return 0;
}
```

### 17. Total, average and percentage of five subjects

```c
#include <stdio.h>

int main() {
    double marks[5], total = 0, average, percentage;
    for (int i = 0; i < 5; i++) {
        scanf("%lf", &marks[i]);
    }
    for (int i = 0; i < 5; i++) {
        total += marks[i];
    }
    average = total / 5;
    percentage = (total / 500) * 100;
    printf("Total = %.2lf\n", total);
    printf("Average = %.2lf\n", average);
    printf("Percentage = %.2lf%%\n", percentage);
    return 0;
}
```
