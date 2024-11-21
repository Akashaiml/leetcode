bool isSubsequence(char * s, char * t) {
    int lenS = strlen(s);
    int lenT = strlen(t);
    
    if (lenS > lenT)
        return false;
    
    int count = 0;
    for (int i = 0; i < lenT; i++) {
        if (*s == t[i]){
            count++;
            s++;
        }
    }

    return count == lenS;
}  
