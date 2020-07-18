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
