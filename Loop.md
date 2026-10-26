### 1. Print the first n natural numbers

```c
#include <stdio.h>
int main() {
    int n,i;
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
        printf("%d ", i);
}
```

### 2. Print the first n odd/even natural numbers

```c
#include <stdio.h>
int main() {
    int n, choice,count = 0,num;
    scanf("%d %d", &n, &choice);
    num = (choice == 1) ? 1 : 2;
    while (count < n) {
        printf("%d ", num);
        num += 2;
        count++;
    }
}
```
### 3. Print all even numbers between 1 to n

```c
#include <stdio.h>
int main() {
    int n,i;
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
        if (i % 2 == 0)
            printf("%d ", i);
}
```

### 4. Print all odd numbers between 1 to n

```c
#include <stdio.h>
int main() {
    int n,i;
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
        if (i % 2 != 0)
            printf("%d ", i);
}
```

### 5. Sum of all natural numbers between 1 to n

```c
#include <stdio.h>
int main() {
    int n, sum = 0,i;
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
        sum += i;
    printf("Sum = %d", sum);
}
```

### 6. Sum of all even numbers between 1 to n

```c
#include <stdio.h>
int main() {
    int n, sum = 0,i;
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
        if (i % 2 == 0)
            sum += i;
    printf("Sum = %d", sum);
}
```

### 7. Sum of all odd numbers between 1 to n

```c
#include <stdio.h>
int main() {
    int n, sum = 0,i;
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
        if (i % 2 != 0)
            sum += i;
    printf("Sum = %d", sum);
}
```

### 8. Sum of every third integer (2 + 5 + 8 + 11 + ...) between 2 to n

```c
#include <stdio.h>
int main() {
    int n, sum = 0,i;
    scanf("%d", &n);
    for (i = 2; i <= n; i += 3)
        sum += i;
    printf("Sum = %d", sum);
}
```

### 9. Print all natural numbers in reverse (n to 1)

```c
#include <stdio.h>
int main() {
    int n,i;
    scanf("%d", &n);
    for (i = n; i >= 1; i--)
        printf("%d ", i);
}
```
### 10. Product of all natural numbers between 1 to n

```c
#include <stdio.h>
int main() {
    int n,i,product = 1;
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
        product *= i;
    printf("Product = %d", product);
}
```

### 11. Average of a list of n numbers

```c
#include <stdio.h>
int main() {
    int n,i;
    double sum = 0, num;
    scanf("%d", &n);
    for (i = 1; i <= n; i++) {
        scanf("%lf", &num);
        sum += num;
    }
    printf("Average = %.2lf", sum / n);
}
```

### 12. Maximum from a list of n numbers

```c
#include <stdio.h>
int main() {
    int n,i;
    double num, max;
    scanf("%d", &n);
    scanf("%lf", &max);// Considering the first number as max
    for (i = 2; i <= n; i++) {// Loop runs one time less
        scanf("%lf", &num);
        if (num > max)
            max = num;
    }
    printf("Maximum = %.2lf", max);
}
```

## 13. Count odd and even numbers from a list of n numbers

```c
#include <stdio.h>
int main() {
    int n,i, num, odd = 0, even=0;
    scanf("%d", &n);
    for (i = 1; i <= n; i++){
        scanf("%d", &num);
        if (num % 2 == 0)
            even++;
        else
            odd++;
    }
    printf("Even = %d, Odd = %d",even,odd);
}
```

## 14. Multiplication table of a number

```c
#include <stdio.h>

int main() {
    int n, i;
    scanf("%d", &n);
    for (i = 1; i <= 10; i++) {
        printf("%d x %d = %d\n", n, i, n * i);//New line is important
    }
}

```

### 15. Power of a number using a for loop
```c
#include <stdio.h>
int main() {
    int base, exp,i,result = 1;
    scanf("%d %d", &base, &exp);
    for (i = 1; i <= exp; ++i)
        result *= base;
    printf("Result = %d", result);
}
```

### 16. Factorial of a number
```c
#include <stdio.h>
int main() {
    int n,i,fact = 1;
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
        fact *= i;
    printf("Factorial = %d", fact);
}

```

### 17. Find all factors of a number
```c
#include <stdio.h>
int main() {
    int n,i;
    scanf("%d", &n);
    for (i = 1; i <= n; ++i) {
        if (n % i == 0)
            printf("%d ", i);
    }
}

```

### 18. Check whether a number is prime
```c
#include<stdio.h>
int main(){
    int num,count=0,i;
    printf("Enter any positive number : ");
    scanf("%d",&num);

    for(i=2; i<num; i++)
    {
        if(num%i==0)
        {
            count++;
            break;
        }
    }
     if(count==0)
            printf("Prime number");
        else
            printf("Not prime number");
}

```

### 19. Print Fibonacci series up to n terms
```c
#include <stdio.h>
int main() {
    int n,a = 0, b = 1, next;
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        printf("%d ", a);
        next = a + b;
        a = b;
        b = next;
    }
}

```

### 20. Check whether a number is an Armstrong number
```c
#include <stdio.h>
#include <math.h>
int main() {
    int n, original, digit, digits = 0;
    double sum = 0;
    scanf("%d", &n);
    original = n;
    int temp = n;
    while (temp != 0) {
        temp /= 10;
        digits++;
    }
    temp = n;
    while (temp != 0) {
        digit = temp % 10;
        sum += pow(digit, digits);
        temp /= 10;
    }
    printf("%s\n", (int)sum == original ? "Armstrong" : "Not Armstrong");
    return 0;
}
```

### 21. Count the number of digits in a number
```c
#include <stdio.h>
int main() {
    int n, count = 0;
    scanf("%d", &n);
    if (n == 0) count = 1;
    while (n != 0) {
        n /= 10;
        count++;
    }
    printf("Digits = %d\n", count);
    return 0;
}
```

### 22. Sum of digits of a number
```c
#include <stdio.h>
int main() {
    int n, sum = 0;
    scanf("%d", &n);
    while (n != 0) {
        sum += n % 10;
        n /= 10;
    }
    printf("Sum of digits = %d\n", sum);
    return 0;
}
```

### 23. Reverse of a number
```c
#include <stdio.h>
int main() {
    int n, reverse = 0;
    scanf("%d", &n);
    while (n != 0) {
        reverse = reverse * 10 + n % 10;
        n /= 10;
    }
    printf("Reverse = %d\n", reverse);
    return 0;
}
```

### 24. Print a number in words
```c
#include <stdio.h>
int main() {
    int n;
    char *digits[10] = {"Zero", "One", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine"};
    char *words[20];
    int count = 0;
    scanf("%d", &n);
    if (n == 0) {
        printf("Zero\n");
        return 0;
    }
    while (n != 0) {
        words[count++] = digits[n % 10];
        n /= 10;
    }
    for (int i = count - 1; i >= 0; i--) {
        printf("%s ", words[i]);
    }
    printf("\n");
    return 0;
}
```

### 25. Check whether a number is palindrome or not
```c
#include <stdio.h>
int main() {
    int n, original, reverse = 0;
    scanf("%d", &n);
    original = n;
    while (n != 0) {
        reverse = reverse * 10 + n % 10;
        n /= 10;
    }
    printf("%s\n", (original == reverse) ? "Palindrome" : "Not Palindrome");
    return 0;
}
```

### 26. HCF (GCD) of two numbers
```c
#include <stdio.h>
int main() {
    int a, b;
    scanf("%d %d", &a, &b);
    int x = a, y = b;
    while (y != 0) {
        int temp = y;
        y = x % y;
        x = temp;
    }
    printf("HCF = %d\n", x);
    return 0;
}
```

### 27. LCM of two numbers
```c
#include <stdio.h>
int main() {
    int a, b;
    scanf("%d %d", &a, &b);
    int x = a, y = b;
    while (y != 0) {
        int temp = y;
        y = x % y;
        x = temp;
    }
    int hcf = x;
    printf("LCM = %d\n", (a * b) / hcf);
    return 0;
}
```

### 28. One's complement of a binary number
```c
#include <stdio.h>
int main() {
    long long binary, complement = 0;
    int place = 1, remainder;
    scanf("%lld", &binary);
    while (binary != 0) {
        remainder = binary % 10;
        complement += (1 - remainder) * place;
        place *= 10;
        binary /= 10;
    }
    printf("One's complement = %lld\n", complement);
    return 0;
}
```

### 29. Convert Decimal to Binary
```c
#include <stdio.h>
int main() {
    int n, binary[32], count = 0;
    scanf("%d", &n);
    if (n == 0) {
        printf("0\n");
        return 0;
    }
    while (n > 0) {
        binary[count++] = n % 2;
        n /= 2;
    }
    for (int i = count - 1; i >= 0; i--) {
        printf("%d", binary[i]);
    }
    printf("\n");
    return 0;
}
```

### 30. Convert Decimal to Octal
```c
#include <stdio.h>
int main() {
    int n, octal[32], count = 0;
    scanf("%d", &n);
    if (n == 0) {
        printf("0\n");
        return 0;
    }
    while (n > 0) {
        octal[count++] = n % 8;
        n /= 8;
    }
    for (int i = count - 1; i >= 0; i--) {
        printf("%d", octal[i]);
    }
    printf("\n");
    return 0;
}
```

### 31. Convert Hexadecimal to Decimal
```c
#include <stdio.h>
#include <string.h>
#include <ctype.h>
int main() {
    char hex[20];
    scanf("%s", hex);
    int len = strlen(hex);
    long decimal = 0, base = 1;
    for (int i = len - 1; i >= 0; i--) {
        char c = toupper(hex[i]);
        int value = (c >= '0' && c <= '9') ? (c - '0') : (c - 'A' + 10);
        decimal += value * base;
        base *= 16;
    }
    printf("Decimal = %ld\n", decimal);
    return 0;
}
```

### 32. Convert Octal to Hexadecimal
```c
#include <stdio.h>
#include <string.h>
int main() {
    char octal[20];
    scanf("%s", octal);
    int len = strlen(octal);
    long decimal = 0, base = 1;
    for (int i = len - 1; i >= 0; i--) {
        decimal += (octal[i] - '0') * base;
        base *= 8;
    }
    char hexDigits[] = "0123456789ABCDEF";
    char hex[20];
    int index = 0;
    if (decimal == 0) {
        printf("0\n");
        return 0;
    }
    while (decimal > 0) {
        hex[index++] = hexDigits[decimal % 16];
        decimal /= 16;
    }
    for (int i = index - 1; i >= 0; i--) {
        printf("%c", hex[i]);
    }
    printf("\n");
    return 0;
}
```
