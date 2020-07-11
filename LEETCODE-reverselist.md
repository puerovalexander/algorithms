## Reverse Linked List
https://leetcode.com/problems/reverse-linked-list/
```python
def reverseList(self, head):
    prev = None
    current = head
    while current:
        tmp = current.next
        current.next = prev
        prev = current
        current = tmp
    return prev
```    
