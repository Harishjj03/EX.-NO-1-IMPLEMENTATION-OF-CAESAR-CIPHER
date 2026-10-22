# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER
## Reg NO : 212224223002
## Name : HARISHBALA J
## Date : 21-10-2026
## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main()
{
    char str[100];
    int key, i;

    printf("Enter text: ");
    scanf(" %99[^\n]", str);

    printf("Enter key: ");
    scanf("%d", &key);

    key = ((key % 26) + 26) % 26;

    for(i = 0; str[i] != '\0'; i++)
    {
        if(str[i] >= 'A' && str[i] <= 'Z')
            str[i] = (str[i] - 'A' + key) % 26 + 'A';
        else if(str[i] >= 'a' && str[i] <= 'z')
            str[i] = (str[i] - 'a' + key) % 26 + 'a';
    }

    printf("Encrypted text: %s\n", str);

    for(i = 0; str[i] != '\0'; i++)
    {
        if(str[i] >= 'A' && str[i] <= 'Z')
            str[i] = (str[i] - 'A' - key + 26) % 26 + 'A';
        else if(str[i] >= 'a' && str[i] <= 'z')
            str[i] = (str[i] - 'a' - key + 26) % 26 + 'a';
    }

    printf("Decrypted text: %s\n", str);

    return 0;
}
```
## OUTPUT:
<img width="1917" height="1025" alt="image" src="https://github.com/user-attachments/assets/f1a68f5c-3a07-4165-b79d-f513be0ba02e" />



## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
