# EX-4 VIGENERE CIPHER 
NAME: Haridharshini J 
REGISTER NUMBER: 212224040098 
# AIM: 
To implement the Vigenere Cipher substitution technique using the C program. 
# ALGORITHM: 
STEP-1: Arrange the alphabets in row and column of a 26*26 matrix. 
STEP-2: Circulate the alphabets in each row to position left such that the first letter is attached to 
the last. 
STEP-3: Repeat this process for all 26 rows and construct the final key matrix. 
STEP-4: The keyword and the plain text is read from the user. 
STEP-5: The characters in the keyword are repeated sequentially so as to match with that of the 
plain text. 
STEP-6: Pick the first letter of the plain text and that of the keyword as the row indices and 
column indices respectively. 
STEP-7: The junction character where these two meet forms the cipher character. 
STEP-8: Repeat the above steps to generate the entire cipher text. 
# PROGRAM: 
#include <stdio.h> 
#include <string.h> 
void vigenereCipher(char *text, char *key, int decrypt) { 
int len = strlen(text), keyLen = strlen(key); 
for (int i = 0; i < len; i++) { 
int shift = key[i % keyLen]- 'A'; 
text[i] = 'A' + (text[i]- 'A' + (decrypt ? 26- shift : shift)) % 26; 
} 
} 
int main() { 
char text[] = "HELLO", key[] = "KEY"; 
vigenereCipher(text, key, 0); 
printf("Encrypted Message: %s\n", text); 
vigenereCipher(text, key, 1); 
printf("Decrypted Message: %s\n", text); 
return 0; 
} 
# OUTPUT: 
<img width="964" height="328" alt="image" src="https://github.com/user-attachments/assets/de871c19-b235-4916-97ce-af2be3fdd4a7" />

# RESULT: 
Thus the implementation of the Vigenere Cipher is executed successfully. 
