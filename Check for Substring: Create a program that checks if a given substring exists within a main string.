#include <stdio.h>

// Function to check if substring 'sub' exists in string 'str'
int isSubstring(char str[], char sub[]) {
    int i, j;

    // Traverse the main string
    for (i = 0; str[i] != '\0'; i++) {
        // Check if the substring matches starting from this position
        for (j = 0; sub[j] != '\0'; j++) {
            // If characters don't match, break the inner loop
            if (str[i + j] != sub[j]) {
                break;
            }
        }

        // If we have checked all characters of the substring
        if (sub[j] == '\0') {
            return 1;  // Substring found
        }
    }

    return 0;  // Substring not found
}

int main() {
    char str[100], sub[100];

    // Input the main string
    printf("Enter the main string: ");
    fgets(str, sizeof(str), stdin);

    // Input the substring
    printf("Enter the substring to search for: ");
    fgets(sub, sizeof(sub), stdin);

    // Remove newline character that fgets might add
    str[strcspn(str, "\n")] = '\0';
    sub[strcspn(sub, "\n")] = '\0';

    // Check if substring exists in the main string
    if (isSubstring(str, sub)) {
        printf("The substring exists in the main string.\n");
    } else {
        printf("The substring does not exist in the main string.\n");
    }

    return 0;
}
