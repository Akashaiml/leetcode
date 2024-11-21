char* convertToTitle(int columnNumber) {
    static char ans [8];
    int i=6;
    ans[7] = '\0';
    while (columnNumber > 0){
        columnNumber--;
        ans[i--]=(columnNumber % 26)+'A';
        columnNumber = columnNumber/26;

    }
    return &ans[i+1];
}
