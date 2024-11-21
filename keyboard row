/**
 * Note: The returned array must be malloced, assume caller calls free().
 */
char** findWords(char** words, int wordsSize, int* returnSize) {
    const int letter[26] = {2, 3, 3, 2, 1, 2, 2, 2, 1, 2, 2, 2, 3,
                      3, 1, 1, 1, 1, 2, 1, 1, 3, 1, 3, 1, 3};
    char** ans =
        malloc(wordsSize * sizeof(char*)); // Create pointer for solution
    int k = 0;
    for (int i = 0; i < wordsSize; i++) {
        int j = 0;
        int row = letter[(words[i][j] | 0x20) - 'a'];
        while (words[i][j] != '\0') {
            if (letter[(words[i][j] | 0x20) - 'a'] != row) {
                row = 0;
                break;
            }
            j++;
        }

        if (row != 0) {
            ans[k] = strdup(words[i]);
            k++;
        }
    }
    *returnSize = k;

    return ans;
}
