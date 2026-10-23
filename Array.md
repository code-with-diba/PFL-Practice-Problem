# 1. Write a C program to find the sum of all elements of an array.

```c
#include<stdio.h>

int main(){

    int i,n,a[1000],sum=0;
    scanf("%d",&n);
    // input array
    for(i=0;i<n;i++){
        scanf("%d",&a[i]);
    }
    // calculating sum
    for(i=0;i<n;i++){
        sum+=a[i];
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
    // array input
    for(i=0;i<n;i++){
        scanf("%d",&a[i]);
    }
    // k value input
    scanf("%d",&k);
    // sum of all element value except k
    for(i=0;i<n;i++){
        if(i!=k)
            sum+=a[i];
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
    // array input
    for(i=0; i<n; i++){
        scanf("%d",&a[i]);
    }
    // max = index value 0 element
    max=a[0];
    // checking if other element are grater then max if so max = that element.
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
    // array input
    for(i=0; i<n; i++){
        scanf("%d",&a[i]);
    }
    // min = index value 0 element
    min=a[0];
    // checking if other element are less then min if so min = that element.
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
    int i,n,a[1000],c=0;
    scanf("%d",&n);
    // array input
    for(i=0;i<n;i++){
        scanf("%d",&a[i]);
    }
    // checking if the value is Negative or not if so c++ mean count + 1 
    for(i=0;i<n;i++){
        if(a[i]<0) // a[i] < 0 if true mean its negative
            c++;
    }
    printf("Total Negative = %d",c);

}
```

### 5. Write a C program to search for an element in an array.

```c
#include<stdio.h>

int main(){
    int i,n,a[1000],k,f=0;
    scanf("%d",&n);
    // array input
    for(i=0;i<n;i++){
        scanf("%d",&a[i]);
    }
    // input k value for seach
    scanf("%d",&k);
    // checking if k value is in the array if yes f = true and loop breaks.
    for(i=0;i<n;i++){
        if(a[i] == k){
            f = 1;
            break;
        }
    }
    // if f == 1 it means the value is in the element 
    if(f==1) {   //else No (if f == 0 it means its not in the array)
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
    // array input
    for(i=0;i<n;i++){
        scanf("%d",&a[i]);
    }
    // geting the position to delete 
    scanf("%d",&k);
    // deleting the positon from array
    for(i=k-1;i<n-1;i++){
        a[i]=a[i+1];
    }
    // since we removed a element the array size is n - 1
    n--;
    // printing updated array
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

