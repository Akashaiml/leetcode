/**
 * Note: The returned array must be malloced, assume caller calls free().
 */
int* countBits(int n, int* returnSize){
    *returnSize = n + 1;
    int* ret = (int*) malloc(*returnSize * sizeof(int));
    ret[0] = 0;
    for (int i = 1; i < *returnSize; i++) {
        ret[i] = (i & 1) + ret[i >> 1];
    }
    return ret;
}
