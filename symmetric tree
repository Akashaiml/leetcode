/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     struct TreeNode *left;
 *     struct TreeNode *right;
 * };
 */
bool isSymmetricHelp(struct TreeNode* left, struct TreeNode* right) {
    if (left == NULL || right == NULL) {
        return left == right;
    }
    if (left->val != right->val) {
        return false;
    }

    return isSymmetricHelp(left->left, right->right) && isSymmetricHelp(left->right, right->left);
}

bool isSymmetric(struct TreeNode* root) {
    return root == NULL || isSymmetricHelp(root->left, root->right);
}
