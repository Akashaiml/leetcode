


typedef struct {
    int val;
} NumArray;


NumArray* numArrayCreate(int* nums, int numsSize) {
    NumArray *ptr = malloc(numsSize *sizeof(NumArray));
    for(int i = 0; i< numsSize; i++)
    {
        if(i != 0)
            ptr[i].val = nums[i] + ptr[i-1].val;
        else
            ptr[i].val = nums[i];
    }
    return ptr;
}

int numArraySumRange(NumArray* obj, int left, int right) {
    if (left == 0)
       return obj[right].val;
    else
        return obj[right].val - obj[left-1].val;
}

void numArrayFree(NumArray* obj) {
    free(obj);
}

/**
 * Your NumArray struct will be instantiated and called as such:
 * NumArray* obj = numArrayCreate(nums, numsSize);
 * int param_1 = numArraySumRange(obj, left, right);
 
 * numArrayFree(obj);
*/
