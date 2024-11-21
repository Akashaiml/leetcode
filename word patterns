bool wordPattern(char* pattern, char* s) {
    int patIdx[256];
    int curSIdx = 0;
    int p = 0;

    memset(patIdx,-1,sizeof(patIdx));

    for (p = 0; pattern[p] != 0 && s[curSIdx] != 0; ++p) {
        if (patIdx[pattern[p]] == -1) {
            patIdx[pattern[p]] = curSIdx;

            for (char p1 = 0; p1 >= 0 && p1 < 256; ++p1) {
                if (patIdx[p1] == -1 || p1 == pattern[p]) continue;

                bool found = true;
                
                int p1Idx;
                int s1Idx;
                for (p1Idx = patIdx[p1], s1Idx = curSIdx; s[p1Idx] != ' ' && s[p1Idx] != 0 &&
                        s[s1Idx] != ' ' && s[s1Idx] != 0; ++p1Idx, ++s1Idx) {
                          
                    if (s[s1Idx] != s[p1Idx]) {
                        
                        found = false;
                        break;
                    }
                }

                bool isEnd1 = s[s1Idx] == ' ' || s[s1Idx] == 0;
                bool isEnd2 = s[p1Idx] == ' ' || s[p1Idx] == 0;
                if (isEnd1 != isEnd2) found = false;

                if (found) {
                    return false;
                }
            }

            for (; s[curSIdx] != ' ' && s[curSIdx] != 0; ++curSIdx);

            // move to begin of next word
            if (s[curSIdx] != 0) ++curSIdx;
        }
        else {
            // word cmp
            int i;
            for (i = patIdx[pattern[p]]; s[curSIdx] != ' ' && s[curSIdx] != 0 &&
                s[i] != ' ' && s[i] != 0; ++curSIdx, ++i) {

                if (s[i] != s[curSIdx]) return false;
            }

            // check blank or string end
            bool isEnd1 = s[i] == ' ' || s[i] == 0;
            bool isEnd2 = s[curSIdx] == ' ' || s[curSIdx] == 0;
            if (isEnd1 != isEnd2) return false;

            // move to begin of next word
            if (s[curSIdx] != 0) ++curSIdx;            
        }
    }

    if (pattern[p] != 0 || s[curSIdx] != 0) return false;

    return true;
}
