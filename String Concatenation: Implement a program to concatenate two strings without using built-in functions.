#include <stdio.h>

// Function to concatenate two strings
void concatenateStrings(char str1[], char str2[]) {
    int i = 0, j = 0;

    // Find the null terminator of the first string
    while (str1[i] != '\0') {
        i++;
    }

    // Append characters of str2 to the end of str1
    while (str2[j] != '\0') {
        str1[i] = str2[j];  // Copy each character
        i++;                // Move to the next position in str1
        j++;                // Move to the next character in str2
    }

    // Null-terminate the concatenated string
    str1[i] = '\0';
}

int main() {
    char str1[200], str2[100];

    // Input the first string
    printf("Enter the first string: ");
    fgets(str1, sizeof(str1), stdin);
    // Remove the newline character added by fgets
    str1[strcspn(str1, "\n")] = '\0';

    // Input the second string
    printf("Enter the second string: ");
    fgets(str2, sizeof(str2), stdin);
    // Remove the newline character added by fgets
    str2[strcspn(str2, "\n")] = '\0';

    // Concatenate the two strings
    concatenateStrings(str1, str2);

    // Output the concatenated string
    printf("Concatenated string: %s\n", str1);

    return 0;
}
