#include <stdio.h>
#include <ctype.h>  // For tolower() function

int main() {
    char str[100];
    int start = 0, end = 0;

    // Input the string
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    // Remove the newline character added by fgets (if any)
    str[strcspn(str, "\n")] = '\0';

    // First, calculate the length of the string
    while (str[end] != '\0') {
        end++;
    }
    end--;  // Set end to the last character (excluding the null terminator)

    // Compare characters from both ends of the string
    while (start < end) {
        // Skip spaces
        if (str[start] == ' ') {
            start++;
            continue;
        }
        if (str[end] == ' ') {
            end--;
            continue;
        }

        // Convert both characters to lowercase and compare
        if (tolower(str[start]) != tolower(str[end])) {
            printf("The string is not a palindrome.\n");
            return 0;  // Not a palindrome, exit
        }

        start++;
        end--;
    }

    // If the loop completes, it's a palindrome
    printf("The string is a palindrome.\n");

    return 0;
}
