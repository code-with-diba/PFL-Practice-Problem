### 1. Print all Prime numbers between 1 to n
```c
#include <stdio.h>
int main() {
    int n;
    scanf("%d", &n);
    for (int i = 2; i <= n; i++) {
        int isPrime = 1;
        for (int j = 2; j * j <= i; j++) {
            if (i % j == 0) {
                isPrime = 0;
                break;
            }
        }
        if (isPrime) {
            printf("%d ", i);
        }
    }
    printf("\n");
    return 0;
}
```

### 2. Print all Perfect numbers between 1 to n
```c
#include <stdio.h>
int main() {
    int n;
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        int sum = 0;
        for (int j = 1; j < i; j++) {
            if (i % j == 0) {
                sum += j;
            }
        }
        if (sum == i) {
            printf("%d ", i);
        }
    }
    printf("\n");
    return 0;
}
```

### 3. Star pattern (right triangle)
```c
#include <stdio.h>
int main() {
    int n;
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        for (int j = 1; j <= i; j++) {
            printf("* ");
        }
        printf("\n");
    }
    return 0;
}
```

### 4. Pascal's triangle up to n rows
```c
#include <stdio.h>
int main() {
    int n;
    scanf("%d", &n);
    for (int i = 0; i < n; i++) {
        long long value = 1;
        for (int j = 0; j <= i; j++) {
            printf("%lld ", value);
            value = value * (i - j) / (j + 1);
        }
        printf("\n");
    }
    return 0;
}
```
