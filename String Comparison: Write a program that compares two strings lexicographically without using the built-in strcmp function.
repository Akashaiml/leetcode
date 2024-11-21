#include <stdio.h>

// Function to compare two strings lexicographically
int compareStrings(char str1[], char str2[]) {
    int i = 0;

    // Compare characters of both strings
    while (str1[i] != '\0' && str2[i] != '\0') {
        if (str1[i] < str2[i]) {
            return -1;  // str1 is lexicographically less than str2
        } else if (str1[i] > str2[i]) {
            return 1;   // str1 is lexicographically greater than str2
        }
        i++;
    }

    // If the strings are of different lengths, compare their null terminators
    if (str1[i] == '\0' && str2[i] != '\0') {
        return -1;  // str1 is shorter than str2
    } else if (str1[i] != '\0' && str2[i] == '\0') {
        return 1;   // str1 is longer than str2
    }

    return 0;  // Both strings are equal
}

int main() {
    char str1[100], str2[100];

    // Input two strings
    printf("Enter the first string: ");
    fgets(str1, sizeof(str1), stdin);
    // Remove the newline character added by fgets
    str1[strcspn(str1, "\n")] = '\0';

    printf("Enter the second string: ");
    fgets(str2, sizeof(str2), stdin);
    // Remove the newline character added by fgets
    str2[strcspn(str2, "\n")] = '\0';

    // Compare the strings
    int result = compareStrings(str1, str2);

    // Output the result of comparison
    if (result == 0) {
        printf("The strings are equal.\n");
    } else if (result < 0) {
        printf("The first string is lexicographically smaller.\n");
    } else {
        printf("The first string is lexicographically greater.\n");
    }

    return 0;
}
