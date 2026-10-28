### 1. Pascal's triangle

```
Input -- n=5
Output --
    1
   1 1
  1 2 1
 1 3 3 1
1 4 6 4 1
```

```c
#include <stdio.h>
int main() {
    int rows, i, j, space, coef = 1;
    printf("Enter the number of rows: ");
    scanf("%d", &rows);
    for (i = 0; i < rows; i++) {
        for (space = 1; space <= rows - i; space++)
            printf(" ");
        for (j = 0; j <= i; j++) {
            if (j == 0 || i == 0)
                coef = 1;
            else
                coef = coef * (i - j + 1) / j;
            printf("%d ", coef);
        }
        printf("\n");
    }
    return 0;
}
```

### 2. Pyramid Pattern
```c
Input - Enter n: 5
Output --
    *
   * *
  * * *
 * * * *
* * * * *
```
```c
#include<stdio.h>
int main()
{
    int n,nst=1,i,j,k;
    scanf("%d",&n);

    for(i=1;i<=n;i++){
        for(j=1;j<=n-i;j++){
            printf(" ");
        }
        for(k=1;k<=nst;k++){
            printf("*");
        }

        nst=nst+2;
        printf("\n");
    }
}
```

### 3. Inverted Pyramid
```c
Enter n: 5
* * * * *
 * * * *
  * * *
   * *
    *
```
```c
#include <stdio.h>
int main() {
    int n,i,j,k,nst;
    scanf("%d", &n);
    nst = n;
    for (i = 1; i <= n; i++) {
        for (j = 1; j <= i - 1; j++) {
            printf(" ");
        }
        for (k= 1; k <= nst; k++) {
            printf("* ");
        }
        nst--;
        printf("\n");
    }
}
```

### 3. Pyramid

```c
#include <stdio.h>

int main() {
    int r, c, n;
    scanf("%d", &n);
    for(r = 1; r < n; r++){
        for(c = 1; c < n; c++){
            printf(" ");
        }
        for(c = 1; c < r; c++){
            printf("* ");
        }
        printf("\n");
    }

    return 0;
}
```

### Pattern number
```c
Input - Enter N = 5
Output -
1
1 2
1 2 3
1 2 3 4
```
```c
#include <stdio.h>
int main() {
    int r,c,n;
    printf("Enter N = ");
    scanf("%d",&n);
    for(r = 1;r <= n; r++){
        for(c = 1;c < r; c++)
            printf("%d ",c);
        }
        printf("\n ");
    }
    return 0;
}
```

### Pattern A AB...
```c
Input - Enter N = 5
Output -
A
AB
ABC
ABCD
````
```c
#include <stdio.h>
int main() {
    int r,c,n;
    printf("Enter N = ");
    scanf("%d",&n);
    for(r = 1;r <= n; r++){
        for(c = 1;c < r; c++)
            printf("%c",c+64);
        }
        printf("\n ");
    }
    return 0;
}
```

### Pira
```c
Enter N = 5
    *
   * *
  * * *
 * * * *
* * * * *
 * * * *
  * * *
```
```c
#include <stdio.h>

int main() {
    int r,c,n;
    printf("Enter N = ");
    scanf("%d",&n);
    for(r = 1;r <= n; r++){
        for(c = 1;c <= n-r; c++){
            printf(" ");
        }
        for(c = 1;c <= r; c++){
            printf("* ");
        }
        printf("\n");
    }

    return 0;
}
```

### Diamond Shape Pattern
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
    int r,c,n;
    printf("Enter N = ");
    scanf("%d",&n);
    for(r = 1;r < n; r++){
        for(c = 1; c <=n-r; c++){
            printf(" ");
        }
        for(c = 1; c <=r; c++){
            printf("* ");
        }
        printf("\n");
    }
    for(r = n;r >=1; r--){
        for(c = 1; c <=n-r; c++){
            printf(" ");
        }
        for(c = 1; c <=r; c++){
            printf("* ");
        }
        printf("\n");
    }

    return 0;
}
```

### Holo Diamond
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
    int r,c,n;
    printf("Enter N = ");
    scanf("%d",&n);
    for(r = 1;r <=n; r++){
        for(c = 1;c <=r; c++){
            if(c==1 || r==n || c==r){
                printf("*");
            }
            else{
                printf(" ");
            }
        }
        printf("\n");
    }

    return 0;
}
```

### Holo Pyramid

Input - Enter N = 5
Output -
    *
   * *
  *   *
 *     *
*********

```c
#include <stdio.h>

int main() {
    int r,c,n = 5;
    printf("Enter N = %d \n",

    for(r = 1;r <=n; r++){
        for(c=1;c<=n-r;c++){
            printf(" ");
        }
        for(c = 1; c<=2*r; c+
            if(c==1 || r==n |
                printf("*");
            }
            else{
                printf(" ");
            }
        }
        for(c=1;c<=2*n-r;c++)
            printf(" ");
        }
        printf("\n");
    }
}
```
