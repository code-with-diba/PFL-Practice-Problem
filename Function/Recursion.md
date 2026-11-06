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
