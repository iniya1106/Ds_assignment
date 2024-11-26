struct ListNode* merge(struct ListNode* left,struct ListNode* right){
    struct ListNode temp;
    struct ListNode* current=&temp;
    temp.next=NULL;
    while(left&&right){
        if(left->val<right->val){
            current->next=left;
            left=left->next;
        }
        else{
            current->next=right;
            right=right->next;
        }
        current=current->next;
    }
    if(left)current->next=left;
    if(right)current->next=right;
    return temp.next;
 }
struct ListNode* sortList(struct ListNode* head) {
    if(!head||!head->next){
        return head;
    }
    struct ListNode* slow=head;
    struct ListNode* fast=head->next;
    while(fast && fast->next){
        slow=slow->next;
        fast=fast->next->next;
    }
    struct ListNode* mid=slow->next;
    slow->next=NULL;
    struct ListNode* left=sortList(head);
    struct ListNode* right=sortList(mid);
    return merge(left,right);
}
