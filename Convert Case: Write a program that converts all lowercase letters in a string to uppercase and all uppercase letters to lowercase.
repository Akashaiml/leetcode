#include <stdio.h>

// Function to convert all lowercase to uppercase and vice versa
void convertCase(char str[]) {
    int i = 0;

    // Traverse the string character by character
    while (str[i] != '\0') {
        // If the character is lowercase, convert to uppercase
        if (str[i] >= 'a' && str[i] <= 'z') {
            str[i] = str[i] - 'a' + 'A';
        }
        // If the character is uppercase, convert to lowercase
        else if (str[i] >= 'A' && str[i] <= 'Z') {
            str[i] = str[i] - 'A' + 'a';
        }
        i++;
    }
}

int main() {
    char str[100];

    // Input the string
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    // Remove the newline character added by fgets (if any)
    str[strcspn(str, "\n")] = '\0';

    // Convert the case of all letters
    convertCase(str);

    // Output the modified string
    printf("Modified string: %s\n", str);

    return 0;
}
