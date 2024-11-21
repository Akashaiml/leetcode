/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     struct TreeNode *left;
 *     struct TreeNode *right;
 * };
 */
/**
 * Note: The returned array must be malloced, assume caller calls free().
 */
void traversal(struct TreeNode * root, char ** ret_arr, int * ret_arr_index, int running_arr[], int * running_arr_index)
{
    if(root)
    {
        if(!root->left && !root->right) //Leaf Node
        {
            ret_arr[*ret_arr_index] = (char *)malloc(sizeof(char) * 300);
            int cur_index = 0;

            //Copy the running array into ret_arr
            int i=0;
            for(i=0; i<*running_arr_index; i++)
            {
                char tmp_str[10];
                sprintf(tmp_str, "%d", running_arr[i]);

                int len_str = strlen(tmp_str);
                memcpy(&ret_arr[*ret_arr_index][cur_index], tmp_str, len_str);
                cur_index += len_str;
                
                //Insertion of "->"
                memcpy(&ret_arr[*ret_arr_index][cur_index], "->", sizeof("->"));
                cur_index += strlen("->");   
            }

            char tmp[10];
            sprintf(tmp, "%d", root->val);
            int len_str = strlen(tmp);
            memcpy(&ret_arr[*ret_arr_index][cur_index], tmp, len_str);
            cur_index += len_str;
            ret_arr[*ret_arr_index][cur_index] = '\0';
            *ret_arr_index += 1;
            return;
        }

        running_arr[*running_arr_index] = root->val;
        *running_arr_index += 1;

        traversal(root->left, ret_arr, ret_arr_index, running_arr, running_arr_index);
        traversal(root->right, ret_arr, ret_arr_index, running_arr, running_arr_index);

        *running_arr_index -= 1;
        return;
    }
    return;
}

char** binaryTreePaths(struct TreeNode* root, int* returnSize) 
{
    char ** ret_arr = (char **)malloc(sizeof(char *) * 100);
    int ret_arr_index = 0;

    int running_arr[100] = {INT_MIN};
    int running_arr_index = 0;

    traversal(root, ret_arr, &ret_arr_index, running_arr, &running_arr_index); 
    *returnSize = ret_arr_index;
    return ret_arr;   
}
