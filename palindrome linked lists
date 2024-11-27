long    nodelen(struct ListNode *arg)
{
    long    i;

    i = 0;
    while (arg)
    {
        arg = arg->next;
        i++;
    }
    return (i);
}


bool isPalindrome(struct ListNode* head) {

    struct ListNode *n = head;
    int             *arr;
    int             j;
    int             i;

    arr = malloc(sizeof(int) * (nodelen(head) + 1));
    if (arr == NULL)
        return (NULL);
    for(i = 0; n != NULL; i++, n = n->next)
        arr[i] = n->val;
    arr[i] = 0;
    for (j = i - 1; (j >= 0 && head); head = head->next)
    {
      if (head->val != arr[j--])
            return (false);
    }
    return (true);
}
