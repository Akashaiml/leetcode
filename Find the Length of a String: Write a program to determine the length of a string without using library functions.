#include <stdio.h>

int stringLength(char str[]) {
    int length = 0;
    
    // Iterate through each character of the string until the null-terminator is found
    while (str[length] != '\0') {
        length++;  // Increment the length for each character
    }
    
    return length;
}

int main() {
    char str[100];

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);  // Input string using fgets (safer than gets)

    // Call the stringLength function to calculate and print the length
    int len = stringLength(str);
    printf("The length of the string is: %d\n", len);

    return 0;
}
