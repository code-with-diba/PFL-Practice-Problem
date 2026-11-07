### 1. Length of a string

```c
#include <stdio.h>
int main() {
    char str[100];
    scanf("%[^\n]", str);
    int length = 0;
    while (str[length] != '\0')
        length++;
    printf("Length = %d\n", length);
    return 0;
}
```

### 2. Copy one string to another

```c
#include <stdio.h>
int main() {
    char str[100], copy[100];
    scanf("%[^\n]", str);
    int i = 0;
    while (str[i] != '\0') {
        copy[i] = str[i];
        i++;
    }
    copy[i] = '\0';
    printf("Copied string = %s\n", copy);
    return 0;
}
```

### 3. Concatenate two strings

```c
#include <stdio.h>
int main() {
    char str1[100], str2[100];
    scanf("%s %s", str1, str2);
    int i = 0, j = 0;
    while (str1[i] != '\0')
        i++;
    while (str2[j] != '\0') {
        str1[i] = str2[j];
        i++;
        j++;
    }
    str1[i] = '\0';
    printf("Concatenated string = %s\n", str1);
    return 0;
}
```

### 4. Compare two strings

```c
#include <stdio.h>
int main() {
    char str1[100], str2[100];
    scanf("%s %s", str1, str2);
    int i = 0, equal = 1;
    while (str1[i] != '\0' || str2[i] != '\0') {
        if (str1[i] != str2[i]) { equal = 0; break; }
        i++;
    }
    printf("%s\n", equal ? "Equal" : "Not Equal");
    return 0;
}
```

### 5. Toggle case of each character of a string

```c
#include <stdio.h>
int main() {
    char str[100];
    scanf("%[^\n]", str);
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] >= 'a' && str[i] <= 'z')
            str[i] = str[i] - 32;
        else if (str[i] >= 'A' && str[i] <= 'Z')
            str[i] = str[i] + 32;
    }
    printf("%s\n", str);
    return 0;
}
```

### 6. Count total number of vowels and consonants in a string

```c
#include <stdio.h>
int main() {
    char str[100];
    scanf("%[^\n]", str);
    int vowels = 0, consonants = 0;
    for (int i = 0; str[i] != '\0'; i++) {
        char ch = str[i];
        if ((ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z')) {
            if (ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u'||ch=='A'||ch=='E'||ch=='I'||ch=='O'||ch=='U')
                vowels++;
            else
                consonants++;
        }
    }
    printf("Vowels = %d, Consonants = %d\n", vowels, consonants);
    return 0;
}
```
### 7. First occurrence of a character in a string

```c
#include <stdio.h>
int main() {
    char str[100], ch;
    scanf("%s %c", str, &ch);
    int pos = -1;
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] == ch) { pos = i; break; }
    }
    if (pos != -1)
        printf("First occurrence at index %d\n", pos);
    else
        printf("Character not found\n");
    return 0;
}
```

### 8. Last occurrence of a character in a string

```c
#include <stdio.h>
int main() {
    char str[100], ch;
    scanf("%s %c", str, &ch);
    int pos = -1;
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] == ch)
            pos = i;
    }
    if (pos != -1)
        printf("Last occurrence at index %d\n", pos);
    else
        printf("Character not found\n");
    return 0;
}
```

### 9. Search all occurrences of a character in a string

```c
#include <stdio.h>
int main() {
    char str[100], ch;
    scanf("%s %c", str, &ch);
    int found = 0;
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] == ch) {
            printf("Found at index %d\n", i);
            found = 1;
        }
    }
    if (!found)
        printf("Character not found\n");
    return 0;
}
```

### 10. Count occurrences of a character in a string

```c
#include <stdio.h>
int main() {
    char str[100], ch;
    scanf("%s %c", str, &ch);
    int count = 0;
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] == ch)
            count++;
    }
    printf("Occurrences = %d\n", count);
    return 0;
}
```

### 11. Reverse of a string

```c
#include <stdio.h>
int main() {
    char str[100];
    scanf("%[^\n]", str);
    int length = 0;
    while (str[length] != '\0')
        length++;
    for (int i = length - 1; i >= 0; i--)
        printf("%c", str[i]);
    printf("\n");
    return 0;
}
```

### 12. Check whether a string is a palindrome

```c
#include <stdio.h>
int main() {
    char str[100];
    int l = 0,i;
    scanf("%s", str);
    while (str[l] != '\0')
        l++;
    int isPalindrome = 1;
    for (i = 0; i < l / 2; i++) {
        if (str[i] != str[l - 1 - i]) {
                isPalindrome = 0;
                 break;
         }
    }
    if(isPalindrome == 1)
        printf("Palindrome");
    else
        printf("Not Palindrome");
}

```

