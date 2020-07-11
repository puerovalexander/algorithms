##Palindrome Linked List
https://leetcode.com/problems/palindrome-linked-list/
```python
def isPalindrome(self, head):      
    if not head or not head.next:
        return True                           
    slow = fast = head                                              
    while fast and fast.next:
        slow = slow.next
        fast = fast.next.next       
    rev = ListNode(slow.val);
    slow = slow.next
    while slow:
        prev = rev                                              
        current = ListNode(slow.val);
        current.next = prev
        rev = current
        slow = slow.next            
    while rev:
        if rev.val != head.val:
            return False
        rev = rev.next
        head = head.next
    return True 
```
