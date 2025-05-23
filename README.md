# HILL CIPHER
HILL CIPHER
EX. NO: 3

## AIM:
IMPLEMENTATION OF HILL CIPHER

## To write a C program to implement the hill cipher substitution techniques.

## DESCRIPTION:

Each letter is represented by a number modulo 26. Often the simple scheme A = 0, B
= 1... Z = 25, is used, but this is not an essential feature of the cipher. To encrypt a message, each block of n letters is  multiplied by an invertible n × n matrix, against modulus 26. To
decrypt the message, each block is multiplied by the inverse of the m trix used for
 
encryption. The matrix used
 
for encryption is the cipher key, and it sho
 
ld be chosen
 
randomly from the set of invertible n × n matrices (modulo 26).


## ALGORITHM:

STEP-1: Read the plain text and key from the user. STEP-2: Split the plain text into groups of length three. STEP-3: Arrange the keyword in a 3*3 matrix.
STEP-4: Multiply the two matrices to obtain the cipher text of length three.
STEP-5: Combine all these groups to get the complete cipher text.

## PROGRAM 
```
#include <stdio.h>  
#include <string.h>  
  
int main()  
 {  
    int key;     
char s[1000];  
  
    printf("Enter a plaintext to encrypt:\n");     
fgets(s, sizeof(s), stdin);     printf("Enter 
key:\n");     scanf("%d", &key);  
  
    int n = strlen(s);  
  
    for (int i = 0; i < n; i++)   
    {  
        char c = s[i];         if 
(c >= 'a' && c <= 'z')   
        {  
            s[i] = 'a' + (c - 'a' + key) % 26;  
        }  
        else if (c >= 'A' && c <= 'Z')  
        {  
            s[i] = 'A' + (c - 'A' + key) % 26;  
        }  
    }  
    printf("Encrypted message: %s\n", s);  
  
    for (int i = 0; i < n; i++)  
    {  
        char c = s[i];         if 
(c >= 'a' && c <= 'z')   
        {  
            s[i] = 'a' + (c - 'a' - key + 26) % 26;   
        }  
        else if (c >= 'A' && c <= 'Z')  
        {  
            s[i] = 'A' + (c - 'A' - key + 26) % 26;   
        }  
    }  
    printf("Decrypted message: %s\n", s);  
  
    return 0;  
}
```

## OUTPUT

![image](https://github.com/user-attachments/assets/9f0d79f4-0524-4977-a2d3-a274f8904610)


## RESULT

Thus, a python program is implement for hill cipher substitution techniques.
