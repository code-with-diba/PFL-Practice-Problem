### 1. Write a C program to find the cube of any number using a function.
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

### 2.Write a C program using functions to find the area of a circle where the radius is given.
```c
#include <stdio.h>

double AreaC(double r)
{
    double a;
    a = 3.1416 * r * r;
    return a;
}

int main() {
    double a, b;
    scanf("%lf", &a);
    b = AreaC(a);
    printf("%.2lf", b);
}
```

### 3.Write a C program to find the minimum between two numbers using functions.
```c
#include <stdio.h>

int Min(int x, int y)
{
    if (x < y)
        return x;
    else
        return y;
}

int main() 
{
    int a, b, m;
    scanf("%d %d", &a, &b);
    m = Min(a, b);
    printf("%d", m);
}
```

### 4.Write a C program using functions to check whether a number is even or odd. 
```c
#include <stdio.h>

int OE(int x)
{
    if (x % 2 == 0)
        return 0;
    else
        return 1;
}

int main()
{
    int a, b;
    scanf("%d", &a);
    b = OE(a);
    if (b == 1)
        printf("Odd");
    else
        printf("Even");
}
```

### 5.Write a C program using functions to check whether a number is prime or not.
```c
#include <stdio.h>

int Isprime(int x)
{
    int i, f = 1;
    for (i = 2; i < x; i++) {
        if (x % i == 0) {
            f = 0;
            break;
        }
    }
    return f;
}

int main()
{
    int n;
    scanf("%d", &n);
    if (Isprime(n) == 1) {
        printf("Prime");
    }
    else {
        printf("Not prime");
    }
    return 0;
}
```

### 6.Write a C program using functions to find the factorial of an integer.
```c
#include<stdio.h>

int Factorial (int x)
{
    int i, fact=1;
    for(i=1; i<=x; i++) {
        fact = fact * i;
    }
    return fact;
}

int main()
{
    int n, result;
    scanf("%d", &n);
    result = Factorial(n);
    printf("%d", result);
   
}
```

### 7.Write a C program to find all prime numbers between the given intervals using functions. 
```c
#include<stdio.h>

int isprime(int x)
{
    int i, f=1;
    if(x<2) // 1 is not prime
        f=0;
    for(i=2; i<x; i++){
        if(x%i==0){
            f=0;
            break;
        }
    }
    return f;
}

int main()
{
    int a, b, i;
    scanf("%d %d", &a, &b);
    for(i=a; i<=b; i++){
        if(isprime(i)==1){
            printf("%d ", i);
        }
    }
}
```
