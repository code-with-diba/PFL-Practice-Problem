### 1. Star pattern (Rectangle)
```c
input = n=4
* * * *
* * * *
* * * *
* * * *
```
```c
#include <stdio.h>
int main() {
    int n,i,j;
    scanf("%d", &n);
    for (i = 1; i <=n; i++) {
        for (j = 1; j <= n; j++) {
            printf("*");
        }
        printf("\n");
    }
}
```

### 2. Star pattern (triangle)
```c
input = n=5
*
* *
* * *
* * * *
* * * * *
```
```c
#include <stdio.h>
int main() {
    int n,i,j;
    scanf("%d", &n);
    for (i = 1; i <= n; i++) {
        for (j = 1; j <= i; j++) {
            printf("*");
        }
        printf("\n");
    }
}

```
```c
input = n=4
   *
  **
 ***
****
```
```c
#include <stdio.h>
int main() {
    int n,i,j,k;
    scanf("%d", &n);
    for (i = 1; i <= n; i++) {
        for (j = 1; j <=n- i; j++) {
            printf(" ");
        }
          for (k = 1; k <= i;k ++) {
            printf("*");
          }
        printf("\n");
    }
}
```
```c
n = 4
****
***
**
*
```
```c
#include <stdio.h>
int main() {
    int n,i,j;
    scanf("%d", &n);
    for (i = 1; i <= n; i++) {
        for (j = n; j >= i; j--) {
            printf("*");
        }
        printf("\n");
    }
}
```
```c
Enter n = 4
   *
  ***
 *****
*******
```
```c
for (i = 1; i <= n; i++) {
    for (j = 1; j <= n - i; j++) {
        printf(" ");
    }
    for (k = 1; k <= nst; k++) {
        printf("*");
    }
    nst = nst + 2;
    printf("\n");
}
```
```c
Enter n = 4
*
* *
* * *
* * * *
* * *
* *
*
```
```c
#include <stdio.h>
int main() {
    int n, i, j;
    scanf("%d", &n);
    for (i = 1; i <= n; i++) {
        for (j = 1; j <= i; j++) {
            printf("* ");
        }
        printf("\n");
    }
    for (i = 2; i <= n; i++) {
        for (j = i; j <= n; j++)
            printf("* ");
        printf("\n");
    }
}
```
### 8.Diamond Shape Pattern
```c
Enter N = 5
    *
   * *
  * * *
 * * * *
* * * * *
 * * * *
  * * *
   * *
    *
```
```c
#include <stdio.h>
int main() {
    int n, i, j, k, nst = 1;
    scanf("%d", &n);
      for (i = 1; i <= n; i++) {
        for (j = 1; j <= n - i; j++) 
            printf(" ");
        for (k = 1; k <= nst; k++) 
            printf("*");
        nst = nst + 2;
        printf("\n");
    }
    nst = 2 * n - 3;
    for (i = 1; i <= n - 1; i++) {
        for (j = 1; j <= i; j++) 
            printf(" ");
        for (k = 1; k <= nst; k++) 
            printf("*");
        nst = nst - 2;
        printf("\n");
    }
}


```

### 9.Holo Diamond
```c
Enter N = 5
*
**
* *
*  *
*****
```
```c
#include <stdio.h>
int main() {
    int i, j, n;
    scanf("%d", &n);
    for(i = 1; i <= n; i++){
        for(j = 1; j <= i; j++){
            if(j == 1 || i == n || j == i)
                printf("*");
            else
                printf(" ");
        }
        printf("\n");
    }
}
```
### 5.Pattern number
```c
Input - Enter N = 4
Output -
1
1 2
1 2 3
1 2 3 4
```
```c
#include <stdio.h>
int main() {
    int n,i,j;
    scanf("%d", &n);
    for (i = 1; i <= n; i++) {
        for (j = 1; j <= i; j++) {
            printf("%d ",j);
        }
        printf("\n");
    }
}

```
### 6.pattern number
```c
1
2 2
3 3 3
4 4 4 4
```
```c
#include <stdio.h>
int main() {
    int n,i,j;
    scanf("%d", &n);
    for (i = 1; i <= n; i++) {
        for (j = 1; j <= i; j++) {
            printf("%d ",i);
        }
        printf("\n");
    }
}
```
```c
input n = 4
4
3 3
2 2 2
1 1 1 1
```
```c
#include <stdio.h>
int main() {
    int n, i, j;
    scanf("%d", &n);
    for (i = 1; i <= n; i++) {
        for (j = 1; j <= i; j++) {
            printf("%d ", n - i + 1);
        }
        printf("\n");
    }
}
```

```c
input n = 4
4
4 3
4 3 2
4 3 2 1
```
```c
#include <stdio.h>
int main() {
    int n, i, j;
    scanf("%d", &n);
    for (i = 1; i <= n; i++) {
        for (j = 1; j <= i; j++) {
            printf("%d ", n - j + 1);
        }
        printf("\n");
    }
}
```
