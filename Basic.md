### 1. Sum of two numbers

```c
#include <stdio.h>

int main() {
    double a, b;
    scanf("%lf %lf", &a, &b);
    printf("Sum = %.2lf\n", a + b);
    return 0;
}
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
    return 0;
}
