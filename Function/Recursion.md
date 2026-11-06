### 1.Sum of first n natural number:

```c
#include<stdio.h>

int sum( int n){
    if( n == 1)
        return 1;
    else
        return n + sum(n-1);
}
```

### 2.Factorial of n
```c
include<stdio.h>

int fact( int n){
    if(n == 1)
        return 1;
    else
        return n * fact(n-1);
}
```
### 3.Nth fibonacci: 0, 1, 1, 2, 3, 5, 8, 13, 21, . . .
```c
#include<stdio.h>

int fib(int n){
    if(n == 1)
        return 0;
    else if(n == 2)
        return 1;
    else
        return fib(n-1) + fib(n-2);
}
```
