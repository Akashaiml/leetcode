bool isAnagram(char* s, char* t) {
    int m=strlen(s);
    int n=strlen(t);
    if(m!=n)
    return false;
    int count[256] = {0};

    for (int i = 0; i < m; i++) {
        count[s[i]]++;
        count[t[i]]--;
    }

    for (int i = 0; i < 256; i++) {
        if (count[i] != 0)
            return false;
    }

    return true;

    
}
