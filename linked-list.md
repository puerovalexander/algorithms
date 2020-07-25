#linked-list

+[Palindrome Linked List](#palindrome-linked-list)
+[Middle of the Linked List](#middle-of-the-linked-list)
+[Reverse Linked List](#reverse-linked-list)
+[Merge Two Sorted List](#merge-two-sorted-list)
+[Remove Nth Node From End of List](#remove-nth-node-from-end-of-list)
+[Linked List Cycle II](#linked-list-cycle-II)
+[Linked List Cycle](#linked-list-cycle)
+[Reorder List](#reorder-list)
+[Intersection of Two Linked Lists](#intersection-of-two-linked-list)
+[Sort List](#sort-list)

## Palindrome Linked List

https://leetcode.com/problems/palindrome-linked-list/

```python
def reverseList(self, head):
    prev = None
    current = head
    while current:
        temp = current.next
        current.next = prev
        prev = current
        current = temp
    return prev
    
def isEqual(self, first, second):
    while second:
        if second.val != first.val:
            return False
        second = second.next
        first = first.next
    return True
    
def isPalindrome(self, head):
    if not head or not head.next:
        return True
    prev = None
    slow = head
    fast = head
    while fast.next and fast.next.next:
        prev = slow
        slow = slow.next
        fast = fast.next.next
    secondHalf = slow.next
    if fast.next: 
        slow.next = None
        firstHalf = self.reverseList(head)
    else: 
        prev.next = None
        firstHalf = self.reverseList(head)
    return self.isEqual(firstHalf, secondHalf)
```
