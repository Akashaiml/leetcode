/**
 * Note: The returned array must be malloced, assume caller calls free().
 */
char** summaryRanges(int* nums, int numsSize, int* returnSize) {
    char** ans = (char**)malloc(numsSize * sizeof(char*));
    *returnSize=0;
    int i=0;
    while (i<numsSize)
    {
       int start=nums[i];

       while (i<numsSize-1 && nums[i+1]==nums[i]+1) 
       {i++;} 

       ans[*returnSize] = (char*)malloc(25 * sizeof(char)); 

       if (start != nums[i]) // if not
       {
         sprintf(ans[*returnSize], "%d->%d", start,nums[i]);
       }
       else { sprintf(ans[*returnSize], "%d", nums[i]);}
       (*returnSize)++;
       i++;

    }

    return ans; 
}     
