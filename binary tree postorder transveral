#define maxN 200

void post(struct TreeNode* root, int* arr, int* idx) {
    if (root == NULL) {
        return;
    }
    post(root->left, arr, idx);
    post(root->right, arr, idx);
    arr[(*idx)++] = root->val;
}

int* postorderTraversal(struct TreeNode* root, int* returnSize) {
    int* arr = (int*)malloc(maxN * sizeof(int));
    int idx = 0;
    post(root, arr, &idx);
    *returnSize = idx;
    return arr;
}
