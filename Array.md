# 1. Write a C program to find the sum of all elements of an array.

```c
#include<stdio.h>
int main(){
    int i,n,a[1000],sum=0;
    scanf("%d",&n);
    for(i=0;i<n;i++){
        scanf("%d",&a[i]);
    }
    for(i=0;i<n;i++){
        sum=sum+a[i];
    }
    printf("%d",sum);
}

```

### 2. Write a C program to find the sum of all array elements except the index value /element.

```c
#include<stdio.h>
int main(){
    int i,n,a[1000],sum=0,k;
    scanf("%d",&n);
    for(i=0;i<n;i++){
        scanf("%d",&a[i]);
    }
    scanf("%d",&k);
    for(i=0;i<n;i++){
        if(i!=k)
            sum=sum+a[i];
    }
    printf("%d",sum);
}
```

### 3. Write a C program to find the maximum/minimum element of an array.

MAX

```c
#include<stdio.h>
int main(){
    int i,n,a[1000],max;
    scanf("%d",&n);
    for(i=0; i<n; i++){
        scanf("%d",&a[i]);
    }
    max=a[0];
    for(i=1; i<n; i++){
        if(max<a[i])
            max=a[i];
    }
    printf("Maximum = %d",max);
}

```

### MINIMUM

```c
#include<stdio.h>
int main(){
    int i,n,a[1000],min;
    scanf("%d",&n);
    for(i=0; i<n; i++){
        scanf("%d",&a[i]);
    }
    min=a[0];
    for(i=1; i<n; i++){
        if(min>a[i])
            min=a[i];
    }
    printf("Minimum = %d",min);
}
```

### 4. Write a C program to count the total number of negative elements in an array.

```c
#include<stdio.h>
int main(){
    int i,n,a[1000],count=0;
    scanf("%d",&n);
    for(i=0;i<n;i++){
        scanf("%d",&a[i]);
    }
    for(i=0;i<n;i++){
        if(a[i]<0)
            count++;
    }
    printf("Total Negative = %d",count);
}

```

### 5. Write a C program to search for an element in an array.

```c
#include<stdio.h>
int main(){
    int i,n,a[1000],k,f=0;
    scanf("%d",&n);
    for(i=0;i<n;i++){
        scanf("%d",&a[i]);
    }
    scanf("%d",&k);
    for(i=0;i<n;i++){
        if(a[i] == k){
            f = 1;
            break;
        }
    }
    if(f==1) {
        printf("Yes");
    }
    else{
        printf("No");
    }
}

```

### 6. Write a C program to delete an element in an array at a specified position.

```c
#include<stdio.h>
int main(){
    int i,n,a[1000],k;
    scanf("%d",&n);
    for(i=0;i<n;i++){
        scanf("%d",&a[i]);
    }
    scanf("%d",&k);
    for(i=k-1;i<n-1;i++){
        a[i]=a[i+1];
    }
    n--;
    for(i=0;i<n;i++){
        printf("%d ",a[i]);
    }
}
```

### 7. Write a C program to insert an element from an array at a specified position.

```c
#include<stdio.h>

int main(){
    int i,n,a[1000],k,v;
    scanf("%d",&n);
    // array input
    for(i=0;i<n;i++){
        scanf("%d",&a[i]);
    }
    // input k and v (K is possiton & v is value of that possiton)
    scanf("%d %d", &k,&v);
    // will empty a possiton to incert value k in k - 1 index
    for(i=n-1;i>=k-1;i--){
       a[i+1] = a[i];
    }
    // in that k - 1 index will put the value v
    a[k-1] = v;
    // since we added 1 exta element to the array n + 1 
    n++;
    // printing updated array
    for(i=0;i<n;i++){
        printf("%d ",a[i]);
    }
}
```

### 8. Write a C program to left-rotate an array.

```c
#include <stdio.h>

int main() {
    int arr[100];
    int n, i, temp;

    printf("Enter the number of elements in the array: ");
    scanf("%d", &n);

    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    temp = arr[0];

    for (i = 0; i < n - 1; i++) {
        arr[i] = arr[i + 1];
    }

    arr[n - 1] = temp;

    printf("Resultant array after left rotation:\n");
    for (i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    return 0;
}
```

### Right Rotate

```c
#include <stdio.h>

int main() {
    int arr[100];
    int n, i, temp;

    printf("Enter the number of elements in the array: ");
    scanf("%d", &n);

    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    temp = arr[n-1];

    for (i = n-1; i > 0; i--) {
        arr[i] = arr[i-1];
    }

    arr[0] = temp;

    printf("Resultant array after left rotation:\n");
    for (i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    return 0;
}
```

### 9. Write a C program to put even and odd elements in two separate arrays.
```c
#include<stdio.h>

int main(){
   int n,i,a[1000],even[1000],odd[1000],ec=0,oc=0;
   scanf("%d",&n);

   for(i=0;i<n;i++){
        scanf("%d",&a[i]);
   }
   for(i=0;i<n;i++){
        if(a[i]%2==0){
            even[ec]=a[i];
            ec++;
         }
        else{
            odd[oc]=a[i];
            oc++;
        }
   }
   for(i=0; i<ec; i++){
        printf("%d ",even[i]);
   
    printf("\n");
    for(i=0; i<oc; i++){
        printf("%d ",odd[i]);
   }
}
```

### 10. Write a C program to print all unique elements in the array.
```c
#include<stdio.h>
/*
input:
7
2 3 4 2 3 3 5
output:
2 3 4 5
*/
int main(){
    
    int i,j,n,a[1000],f;
    scanf("%d",&n);
    // array input
    for(i=0; i<n; i++)
        scanf("%d",&a[i]);
    // filtering uniqe element 
    for(i=0; i<n; i++){
        // f = true
        f=1;
        // checking if the element is dup or not if so it will break and wont print.
        for(j=i-1;j>=0;j--){ // keep in mind it will print every element 1ce 
            if(a[i]==a[j]){
                f=0;
                break;
            }
        }
        if(f==1) printf("%d ",a[i]);
    }

}
```

OR
```c
#include<stdio.h>
/*
input:
5
1 2 3 3 9
output:
1 2 9
*/
int main(){
    
    int i,j,n,a[1000],f;
    scanf("%d",&n);
    // array input
    for(i=0; i<n; i++)
        scanf("%d",&a[i]);
    // filtering uniqe element 
    for(i=0; i<n; i++){
        // f = true
        f=1;
        // checking if the element is dup or not if so it will break and wont print.
        for(j=0;j<n;j++){ // keep in mind it will only print element that is not dup. 
            if(a[i]==a[j]&&i!=j){
                f=0;
                break;
            }
        }
        if(f==1) printf("%d ",a[i]);
    }
}
```

### 11.Write a C program to sort the elements of an array in ascending or descending order.
```c
#include<stdio.h>
// index pick -->> OL (i)
// checking -->> IL(j)
int main(){

   int n,i,j,a[1000],t;
   scanf("%d",&n);

   for(i=0;i<n;i++){
    scanf("%d",&a[i]);
   }
   for(i=0;i<n;i++){
        for(j=i+1;j<n;j++){
            if(a[i]>a[j]){
                t=a[i];
                a[i]=a[j];
                a[j]=t;
            }
        }
   }
   for(i=0;i<n;i++){
    printf("%d ",a[i]);
   }
}
```

### 2D Array
### 1.Write a C program to add two matrices.
```c
#include<stdio.h>

int main(){

    int i,j,r,c,a[100][100],b[100][100];
    scanf("%d %d",&r,&c);
    // loop for input array a
    for(i=0; i<r; i++)
        for(j=0; j<c; j++)
            scanf("%d",&a[i][j]);
    // loop for input array b
    for(i=0; i<r; i++)
        for(j=0; j<c; j++)
            scanf("%d",&b[i][j]);
    // adding 2 matrix in to a
    for(i=0; i<r; i++){
        for(j=0; j<c; j++){
            a[i][j] += b[i][j];
        }
    }
    // printing array a (updated after adding 2 matrix)
    for(i=0; i<r; i++){
        for(j=0; j<c; j++){
            printf("%d ",a[i][j]);
        }
        printf("\n");
    }

}
```
OR
```c
#include<stdio.h>

int main(){

    int i,j,r,c,a[100][100],b[100][100];
    scanf("%d %d",&r,&c);
    // loop for input array a
    for(i=0; i<r; i++)
        for(j=0; j<c; j++)
            scanf("%d",&a[i][j]);
    // loop for input array b
    for(i=0; i<r; i++)
        for(j=0; j<c; j++)
            scanf("%d",&b[i][j]);
    // adding 2 matrix in to a
    for(i=0; i<r; i++){
        for(j=0; j<c; j++){
            a[i][j] += b[i][j];
            printf("%d ",a[i][j]); // printing array a (updated after adding 2 matrix)
        }
        printf("\n");
    }

}
```

### 2.Write a C program to check whether two matrices are equal.
```c
#include<stdio.h>

int main(){

    int i,j,r,c,a[100][100],b[100][100],f=1;
    scanf("%d %d",&r,&c);
    for(i=0; i<r; i++){}
        for(j=0; j<c; j++){
            scanf("%d",&a[i][j]);
        } 
    for(i=0; i<r; i++){}
        for(j=0; j<c; j++){
            scanf("%d",&b[i][j]);
        }
    for(i=0; i<r; i++){
        for(j=0; j<c; j++){
            if(a[i][j]!=b[i][j]){
                f=0;
                break;
            }
        }
        if(f==0) break; //optional
    }
    if(f==1) printf("Equal");
    else printf("Not Equal");

}
```

### 3.Write a C program to perform Scalar matrix multiplication.
```c
#include <stdio.h>

int main() {
    int n, scalar;
    int i, j;

    printf("Enter the order of the matrix: ");
    scanf("%d", &n);

    printf("Enter the scalar value: ");
    scanf("%d", &scalar);

    printf("Scalar Matrix:\n");

    for (i = 0; i < n; i++) {
        for (j = 0; j < n; j++) {
            if (i == j)
                printf("%d ", scalar);
            else
                printf("0 ");
        }
        printf("\n");
    }

    return 0;
}
```

### 4.Write a C program to find the sum of a matrix's main/major diagonal elements.
```c
#include<stdio.h>

int main(){

    int i,j,n,a[100][100],sum=0;
    scanf("%d",&n);
    // loop for input array a
    for(i=0; i<n; i++){        
        for(j=0; j<n; j++){
            scanf("%d",&a[i][j]);
        }
    }
    for(i=0; i<n; i++){
            sum+= a [i][i]; //  -->> for a[i][n-1-i] RT (Minor)
    }
    printf("%d",sum);
}
```

### 5.Write a C program to find the sum of the minor diagonal elements of a matrix.
```c
#include<stdio.h>

int main(){

    int i,j,n,a[100][100],sum=0;
    scanf("%d",&n);
    // loop for input array a
    for(i=0; i<n; i++){        
        for(j=0; j<n; j++){
            scanf("%d",&a[i][j]);
        }
    }
    for(i=0; i<n; i++){
            sum+= a[i][n-1-i]; // a [i][i] -->> for LT (Major)
    }
    printf("%d",sum);
}
```

### 6.Write a C program to find the transpose of a matrix. 
```c
#include<stdio.h>

int main(){

    int i,j,r,c,a[100][100],tr[100][100];

    scanf("%d %d",&r,&c);
    for(i=0; i<r; i++){
        for(j=0; j<c; j++){
            scanf("%d",&a[i][j]);
        }
            
    } 
    for(i=0; i<r; i++){
        for(j=0; j<c; j++){
            tr[j][i]=a[i][j];
        }
    }
    for(i=0; i<c; i++){
        for(j=0; j<r; j++){
            printf("%d ",tr[i][j]);
        }
        printf("\n");
    }

}
```

### 7.Write a C program to check whether a matrix is an identity matrix.
```c
#include<stdio.h>

int main(){

    int i,j,n,a[100][100],c1=0,c0=0;

    scanf("%d",&n);
    // input for array a
    for(i=0; i<n; i++){
        for(j=0; j<n; j++){
            scanf("%d",&a[i][j]);
        }
    }
    // checking wheather its a Identity Matrix or not. 
    for(i=0; i<n; i++){
        for(j=0; j<n; j++){
            if(i == j && a[i][j] == 1){ // i == j && a[i][j] == 1 c1 = should be n like if n = 5 c1 should be 5
                c1++;
            }
            else if(i != j && a[i][j] == 0){ // i != j && a[i][j] == 0 c0 = should be n*n-n like if n = 5 c0 should be 5*5-5 = 20 
                c0++;                        // coz in a square matrix there is total n*n element and since we have 1 on the diagonal axis 
            }                                // thats why we -n after the multiplication 
        }
    }

    if(c1==n && c0==n*n-n) printf("Identity");
    else printf("Not Identity");

}
```

### 8.Write a C program to check whether a matrix is sparse.
```c
#include<stdio.h>

int main(){

    int i,j,r,c,a[100][100],count=0;

    scanf("%d %d",&r,&c);
    // array input
    for(i=0; i<r; i++){
        for(j=0; j<c; j++){
            scanf("%d",&a[i][j]);
        }
    }
    // checking if the eliment is 0 or not. if == 0 count else dont.
    for(i=0; i<r; i++){
        for(j=0; j<c; j++){
            if(a[i][j]==0)
                count++;
        }
    }
            
    if(count > (r*c)/2){
        printf("Sparse Matrix");
    }
    else{
        printf("Not a Sparse Matrix");
    }

}
```

### 9.Write a C program to check whether a matrix is symmetric.
```c
#include <stdio.h>

int main() {
    int matrix[10][10];
    int n, i, j;
    int symmetric = 1;

    scanf("%d", &n);

    for (i = 0; i < n; i++) {
        for (j = 0; j < n; j++) {
            scanf("%d", &matrix[i][j]);
        }
    }

    for (i = 0; i < n; i++) {
        for (j = 0; j < n; j++) {
            if (matrix[i][j] != matrix[j][i]) {
                symmetric = 0;
                break;
            }
        }
    }

    if (symmetric == 1){
        printf("The matrix is symmetric.\n");
    }
    else{
        printf("The matrix is not symmetric.\n");
    }
        
}
```

### 10.Write a C program to print Pascal's triangle up to n rows.
```c
#include<stdio.h>

int main(){

    int i,j,n,a;

    scanf("%d",&n);

    for(i=0; i<n; i++){
        a=1;

        for(j=0; j<n-i-1; j++){
            printf(" ");
        }

        for(j=0; j<=i; j++){
            printf("%d ",a);
            a=a*(i-j)/(j+1);
        }
        printf("\n");
    }

}
```
