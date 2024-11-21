#include <stdio.h>
#include <string.h>

// Function to reverse a string
void reverseString(char str[]) {
    int start = 0;
    int end = strlen(str) - 1;
    
    // Swap characters from start to end until the middle of the string is reached
    while (start < end) {
        // Swap characters
        char temp = str[start];
        str[start] = str[end];
        str[end] = temp;
        
        // Move indices towards the center
        start++;
        end--;
    }
}

int main() {
    char str[100];
    
    // Input string
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    
    // Remove the newline character if it's there (added by fgets)
    str[strcspn(str, "\n")] = '\0';
    
    // Call the reverse function
    reverseString(str);
    
    // Output the reversed string
    printf("Reversed string: %s\n", str);

    return 0;
}
