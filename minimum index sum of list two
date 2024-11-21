/**
 * Note: The returned array must be malloced, assume caller calls free().
 */
char** findRestaurant(char** list1, int list1Size, char** list2, int list2Size, int* returnSize) {
    int n = list1Size;
 char** words = (char**)malloc(2000 * sizeof(char *));
 int index = 0,min = 2000;
 for(int i=0;i<list1Size;i++){
    for(int j=0;j<list2Size;j++){
        if(strcmp(list1[i],list2[j]) == 0 ){
            if(i + j < min) {
                min = i + j;
                for(int z=0;z<index;z++){
                    strcpy(words[z],"");
                    free(words[z]);
                }
                index = 0;
                words[index] = (char*)malloc(31 * sizeof(char));
                strcpy(words[index],list1[i]);
                
                index++;
                

            }else if(i + j  == min){
                words[index] = (char*)malloc(31 * sizeof(char));
                strcpy(words[index],list1[i]);
                index++;
            }
        }
    }
 }
 *returnSize = index;
 return words;
}
