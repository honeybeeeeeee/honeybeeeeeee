# honeybeeeeeee
class Solution {
public:
    ListNode* ReverseList(ListNode* pHead) {
		ListNode* pReversedHead = NULL;
    ListNode* pNode = pHead;
    ListNode* pPrev = NULL;
    while(pNode != NULL)
    {
        ListNode* pNext = pNode->next;

        if(pNext == NULL)
            pReversedHead = pNode;

        pNode->next = pPrev;

        pPrev = pNode;
        pNode = pNext;
    }

    return pReversedHead;
}
    
};
