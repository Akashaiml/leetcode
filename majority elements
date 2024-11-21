int majorityElement(int* nums, int numsSize) {
    int majorityElement = nums[0];
    int count = 1;
    for (int i = 1; i < numsSize; i++) {
        if (nums[i] == majorityElement) {
            count++;
        } else {
            count--;
            if (count == 0) {
                majorityElement = nums[i];
                count = 1;
            }
        }
    }
    return majorityElement;
}
