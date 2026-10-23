### 1. Pascal's triangle

```Input -- Enter the number of rows
Output --
    1
   1 1
  1 2 1
 1 3 3 1
1 4 6 4 1

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

Input - Enter n: 5
Output --
    *
   * *
  * * *
 * * * *
* * * * *

```c
#include <stdio.h>

int main(){
    int i, j, n;

    printf("Enter n: ");
    scanf("%d", &n);

    for(i = 1; i <= n; i++){
        for(j = 1; j <= n - i; j++){
            printf(" ");
        }

        for(j = 1; j <= i; j++){
            printf("* ");
        }

        printf("\n");
    }

    return 0;
}
```

### 3. Inverted Pyramid

Enter n: 5
* * * * *
 * * * *
  * * *
   * *
    *

```c
#include <stdio.h>

int main(){
    int i, j, n;

    printf("Enter n: ");
    scanf("%d", &n);

    for(i = n; i >= 1; i--){
        for(j = 1; j <= n - i; j++){
            printf(" ");
        }

        for(j = 1; j <= i; j++){
            printf("* ");
        }

        printf("\n");
    }

    return 0;
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

Input - Enter N = 5
Output -
1
1 2
1 2 3
1 2 3 4

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

Input - Enter N = 5
Output -
A
AB
ABC
ABCD

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

Enter N = 5
    *
   * *
  * * *
 * * * *
* * * * *
 * * * *
  * * *

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

Enter N = 5
*
**
* *
*  *
*****

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
