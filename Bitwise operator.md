### 1. Swap two numbers using bitwise operator

```c
#include <stdio.h>

int main() {
    int a, b;
    scanf("%d %d", &a, &b);
    a = a ^ b;
    b = a ^ b;
    a = a ^ b;
    printf("a = %d, b = %d\n", a, b);
    return 0;
}
```

### 2. Check if LSB is set

```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);
    if (n & 1)
        printf("LSB is set\n");
    else
        printf("LSB is not set\n");
    return 0;
}
```

### 3. Check if MSB is set

```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);
    int bits = sizeof(int) * 8;
    if (n & (1 << (bits - 1)))
        printf("MSB is set\n");
    else
        printf("MSB is not set\n");
    return 0;
}
```

### 4. Get nth bit of a number

```c
#include <stdio.h>

int main() {
    int n, pos;
    scanf("%d %d", &n, &pos);
    int bit = (n >> pos) & 1;
    printf("Bit at position %d is %d\n", pos, bit);
    return 0;
}
```

### 5. Set nth bit of a number

```c
#include <stdio.h>

int main() {
    int n, pos;
    scanf("%d %d", &n, &pos);
    n = n | (1 << pos);
    printf("Number after setting %d bit: %d\n", pos, n);
    return 0;
}
```

### 6. Clear nth bit of a number

```c
#include <stdio.h>

int main() {
    int n, pos;
    scanf("%d %d", &n, &pos);
    n = n & ~(1 << pos);
    printf("Number after clearing %d bit: %d\n", pos, n);
    return 0;
}
```

### 7. Toggle nth bit of a number

```c
#include <stdio.h>

int main() {
    int n, pos;
    scanf("%d %d", &n, &pos);
    n = n ^ (1 << pos);
    printf("Number after toggling %d bit: %d\n", pos, n);
    return 0;
}
```

### 8. Get highest set bit of a number

```c
#include <stdio.h>

int main() {
    unsigned int n;
    scanf("%u", &n);
    int pos = -1;
    while (n) {
        pos++;
        n = n >> 1;
    }
    printf("Highest set bit position: %d\n", pos);
    return 0;
}
```

### 9. Get lowest set bit of a number

```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);
    int lowest = n & (-n);
    printf("Lowest set bit = %d\n", lowest);
    return 0;
}
```

### 10. Count trailing zeros in a binary number

```c
#include <stdio.h>

int main() {
    unsigned int n;
    scanf("%u", &n);
    int count = 0;
    if (n == 0) {
        printf("Trailing zeros = 32\n");
        return 0;
    }
    while ((n & 1) == 0) {
        count++;
        n = n >> 1;
    }
    printf("Trailing zeros = %d\n", count);
    return 0;
}
```

### 11. Count leading zeros in a binary number

```c
#include <stdio.h>

int main() {
    unsigned int n;
    scanf("%u", &n);
    int bits = sizeof(int) * 8;
    int count = 0;
    for (int i = bits - 1; i >= 0; i--) {
        if ((n >> i) & 1)
            break;
        count++;
    }
    printf("Leading zeros = %d\n", count);
    return 0;
}
```

### 12. Flip bits of a binary number using bitwise operator

```c
#include <stdio.h>

int main() {
    unsigned int n;
    scanf("%u", &n);
    unsigned int flipped = ~n;
    printf("Flipped = %u\n", flipped);
    return 0;
}
```

### 13. Count total zeros and ones in a binary number

```c
#include <stdio.h>

int main() {
    unsigned int n;
    scanf("%u", &n);
    int ones = 0, zeros = 0;
    int bits = sizeof(int) * 8;
    for (int i = 0; i < bits; i++) {
        if ((n >> i) & 1)
            ones++;
        else
            zeros++;
    }
    printf("Ones = %d, Zeros = %d\n", ones, zeros);
    return 0;
}
```

### 14. Rotate bits of a given number

```c
#include <stdio.h>

int main() {
    unsigned int n, d;
    int bits = sizeof(int) * 8;
    scanf("%u %u", &n, &d);
    d = d % bits;
    unsigned int leftRotate = (n << d) | (n >> (bits - d));
    unsigned int rightRotate = (n >> d) | (n << (bits - d));
    printf("Left rotate = %u\n", leftRotate);
    printf("Right rotate = %u\n", rightRotate);
    return 0;
}
```

### 15. Convert decimal to binary using bitwise operators

```c
#include <stdio.h>

int main() {
    unsigned int n;
    scanf("%u", &n);
    char binary[33];
    int index = 0;
    int started = 0;
    for (int i = 31; i >= 0; i--) {
        int bit = (n >> i) & 1;
        if (bit)
            started = 1;
        if (started)
            binary[index++] = bit + '0';
    }
    if (index == 0)
        binary[index++] = '0';
    binary[index] = '\0';
    printf("Binary = %s\n", binary);
    return 0;
}
```

## 16. Swap two numbers using bitwise operator (alternate demo)

```c
#include <stdio.h>
void swapBitwise(int *a, int *b) {
    *a = *a ^ *b;
    *b = *a ^ *b;
    *a = *a ^ *b;
}
int main() {
    int a, b;
    scanf("%d %d", &a, &b);
    swapBitwise(&a, &b);
    printf("a = %d, b = %d\n", a, b);
    return 0;
}
```

## 17. Check even or odd using bitwise operator

```c
#include <stdio.h>
int main() {
    int n;
    scanf("%d", &n);
    if (n & 1) {
        printf("Odd\n");
    }
    else {
        printf("Even\n");
    }
    return 0;
}
```
