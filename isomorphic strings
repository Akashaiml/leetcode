bool isIsomorphic(char* s, char* t) {
    int len1 = strlen(s);
    int len2 = strlen(t);
    if (len1 != len2) {
        return 0;
    }

    int map1[256] = {0};
    int map2[256] = {0};

    for (int i = 0; i < len1; i++) {
        int c1 = (int)s[i];
        int c2 = (int)t[i];

        if (map1[c1] == 0 && map2[c2] == 0) {
            map1[c1] = c2;
            map2[c2] = c1;
        } else if (map1[c1] != c2 || map2[c2] != c1) {
            return 0;
        }
    }
    return 1;

}
