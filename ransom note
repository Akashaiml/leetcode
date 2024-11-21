bool canConstruct(char* ransomNote, char* magazine) {
    // Loop through each character in ransomNote
    for (int i = 0; ransomNote[i] != '\0'; i++) {
        // Find the character in the magazine
        char *ptr = strchr(magazine, ransomNote[i]);
        if (ptr == NULL) {
            return false;  // Character not found in magazine
        }
        // Mark this character as used by replacing it with a special character
        *ptr = '*';
    }
    return true;
}
