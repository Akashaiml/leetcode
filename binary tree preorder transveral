/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     struct TreeNode *left;
 *     struct TreeNode *right;
 * };
 */

int* preorderTraversal(struct TreeNode* root, int* returnSize) {
    if (root == NULL) {
        *returnSize = 0;
        return NULL;
    }
    struct TreeNode** stack = (struct TreeNode**)malloc(sizeof(struct TreeNode*));
    int stackSize = 0;
    int capacity = 1;
    int* result = (int*)malloc(sizeof(int));
    int resultSize = 0;
    while (stackSize > 0 || root != NULL) {
        while (root != NULL) {
            result = (int*)realloc(result, (resultSize + 1) * sizeof(int));
            result[resultSize++] = root->val;
            if (root->right != NULL) {
                if (stackSize >= capacity) {
                    capacity *= 2;
                    stack = (struct TreeNode**)realloc(stack, capacity * sizeof(struct TreeNode*));
                }
                stack[stackSize++] = root->right;
            }
            root = root->left;
        }
        if (stackSize > 0) {
            root = stack[--stackSize];
        }
    }
    free(stack);
    *returnSize = resultSize;
    return result;
}
