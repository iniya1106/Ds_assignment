struct ListNode* reverseList(struct ListNode* head) {
    struct ListNode* previous=NULL;
    struct ListNode* temp=head;
    while(temp){
        struct ListNode* next=temp->next;
        temp->next=previous;
        previous=temp;
        temp=next;
    }
    return previous;
}
