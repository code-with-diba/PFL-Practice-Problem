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
#include<stdio.h>
int main()
{
    double r;
    const double PI =3.1416;
    scanf("%lf",&r);
    printf("Diameter = %.2lf\n",2*r);
    printf("Circumference = %.2lf\n",2*PI*r);
    printf("Area = %.2lf",PI*r*r);
}

```

### 8. Centimeters to meters and kilometers

```c
#include <stdio.h>

int main() {
    double cm;
    scanf("%lf", &cm);
    printf("Meters = %.2lf\n", cm / 100);
    printf("Kilometers = %.5lf", cm / 100000);
}
```

### 9. Celsius to Fahrenheit

```c
#include<stdio.h>
int main()
{
  double c,f;
  scanf("%lf",&c);
  f=(c*9/5)+32;
  printf("Fahrenheit = %.2lf",f);
}

```

### 10. Fahrenheit to Celsius

```c
#include<stdio.h>
int main()
{
  double f,c;
  scanf("%lf",&f);
  c =(f-32)*5/9;
  printf("Celsius = %.2lf",c);
}

```

### 11. Days into years, weeks and days

```c
include <stdio.h>

int main() {
    int totalDays, years, weeks, days;
    scanf("%d", &totalDays);
    years = totalDays / 365;
    days = totalDays % 365;
    weeks = days / 7;
    days = days % 7;
    printf("%d years, %d weeks, %d days", years, weeks, days);
}

```

### 12. Power of a number x^y

```c
#include <stdio.h>
#include <math.h>

int main() {
    double x, y;
    scanf("%lf %lf", &x, &y);
    printf("Result = %.2lf", pow(x, y));
}
```

### 13. Square root of a number

```c
#include <stdio.h>
#include <math.h>

int main() {
    double n;
    scanf("%lf", &n);
    printf("Square root = %.2lf", sqrt(n));
}

```

### 14. Third angle of a triangle

```c
#include <stdio.h>

int main() {
    double angle1, angle2, angle3;
    scanf("%lf %lf", &angle1, &angle2);
    angle3 = 180 - angle1 - angle2;
    printf("Third angle = %.2lf", angle3);
}
```

### 15. Area of a triangle 

```c
#include <stdio.h>

int main() {
    double base, height;
    scanf("%lf %lf", &base, &height);
    printf("Area = %.2lf", 0.5 * base * height);
}
```

### 16. Area of an equilateral triangle

```c
#include <stdio.h>
#include <math.h>

int main() {
    double side;
    scanf("%lf", &side);
    printf("Area = %.2lf", (sqrt(3) / 4) * side * side);
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
    printf("Percentage = %.2lf", percentage);
}

```
