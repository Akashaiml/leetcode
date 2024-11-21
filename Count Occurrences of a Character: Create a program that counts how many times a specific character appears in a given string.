#include <stdio.h>

// Function to count the occurrences of a specific character in a string
int countOccurrences(char str[], char target) {
    int count = 0;

    // Traverse through each character of the string
    for (int i = 0; str[i] != '\0'; i++) {
        // If the current character matches the target, increment the counter
        if (str[i] == target) {
            count++;
        }
    }

    return count;
}

int main() {
    char str[100], target;

    // Input the string
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    // Remove the newline character added by fgets (if any)
    str[strcspn(str, "\n")] = '\0';

    // Input the character to count
    printf("Enter the character to count: ");
    scanf("%c", &target);

    // Count the occurrences of the character
    int occurrences = countOccurrences(str, target);

    // Output the result
    printf("The character '%c' appears %d times in the string.\n", target, occurrences);

    return 0;
}
