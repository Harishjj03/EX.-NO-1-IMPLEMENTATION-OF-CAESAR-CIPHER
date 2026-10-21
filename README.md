# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER
## Reg NO : 212224223002
## Name : HARISHBALA J
## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
# ENCRYPTION:
```
#include <stdio.h>

int main()
{
    char str[100];
    int key, i;

    printf("Enter text: ");
    scanf("%s", str);

    printf("Enter key: ");
    scanf("%d", &key);

    for(i = 0; str[i] != '\0'; i++)
    {
        if(str[i] >= 'A' && str[i] <= 'Z')
            str[i] = (str[i] - 'A' + key + 26) % 26 + 'A';
        else if(str[i] >= 'a' && str[i] <= 'z')
            str[i] = (str[i] - 'a' + key + 26) % 26 + 'a';
    }

    printf("Encrypted text: %s", str);

    return 0;
}
```
# DECRYPTION:
```
#include <stdio.h>

int main()
{
    char str[100];
    int key, i;

    printf("Enter text: ");
    scanf("%99s", str);

    printf("Enter key: ");
    scanf("%d", &key);

    for(i = 0; str[i] != '\0'; i++)
    {
        if(str[i] >= 'A' && str[i] <= 'Z')
            str[i] = (str[i] - 'A' - key % 26 + 26) % 26 + 'A';
        else if(str[i] >= 'a' && str[i] <= 'z')
            str[i] = (str[i] - 'a' - key % 26 + 26) % 26 + 'a';
    }

    printf("Decrypted value: %s", str);

    return 0;
}
```
## OUTPUT:
## ENCRYPTION:

<img width="1916" height="1035" alt="image" src="https://github.com/user-attachments/assets/b9e32101-c068-478c-aa1d-f2a832930479" />

## DECRYPTION:

<img width="1912" height="1027" alt="image" src="https://github.com/user-attachments/assets/bce4b75c-19d2-454b-b060-6ed353e7a70d" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
