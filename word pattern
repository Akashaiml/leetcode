bool wordPattern(char* pattern, char* s) {
    char* hashmap[128] = {NULL}; // 存儲 pattern -> word 的映射
    char* reverseMap[128] = {NULL}; // 存儲 word -> pattern 的反向映射

    char* word = strtok(s, " "); // 分割字串
    int i = 0, j = 0;
    int exist = 0;
    while (word != NULL) {
        char c = pattern[i];
        exist = 0;
        // 如果 pattern 已經遍歷完，但還有多餘的單詞
        if (c == '\0') {
            printf("222");
            return false;
        }

        // 檢查 word -> pattern 映射
        j = 0;
        while(reverseMap[j] != NULL){
            if(strcmp(word, reverseMap[j]) == 0){
                exist = 1;
                if(hashmap[c] == NULL) return false;
                else if(strcmp(word, hashmap[c]) != 0){
                    return false;
                }
                else break;
            }
            j++;
        }
        if(exist == 0){ // 建立反映射
            reverseMap[j] = word;
        }
        // 檢查 pattern -> word 映射
        if (hashmap[c] == NULL) {
            hashmap[c] = word; // 建立映射
        } else if (strcmp(hashmap[c], word) != 0) {
            printf("1111");
            return false; // 不匹配
        }

        // 繼續處理下一個單詞
        word = strtok(NULL, " ");
        i++;
    }

    // 確保 pattern 也完全遍歷完
    return pattern[i] == '\0';
}
