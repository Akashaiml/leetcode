int firstUniqChar(char* s) {
    int ans = 0;
    int Letters[26] = {0};      //'a' -> Letters[0], 'b' -> Letters[1], ......, 'z' -> Letters[25]
    for(int i = 0; i < strlen(s); i++){
        Letters[s[i] - 'a']++;
        //Find the first non-repeating character if the original character turns out to be repeating
        if(Letters[s[ans] - 'a'] > 1){
            ans++;  //Move to the next index to see if it is the first non-repeating character
            while(ans <= i){
                if(Letters[s[ans] - 'a'] == 1)
                    break;
                else ans++;
            }
        }
    }
    if(ans == strlen(s))    //All characters appear more than once
        return -1;
    else
        return ans;
}
