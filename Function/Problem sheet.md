### 1. Write a C program to find the cube of any number using a function
```c
#include <stdio.h>

int cube(int x) {
    int y;
    y = x * x * x;
    return y;
}

int main() {
    int a, b;
    scanf("%d", &a);
    b = cube(a);
    printf("%d", b);
}
```
