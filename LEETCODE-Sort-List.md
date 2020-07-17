## Sort List

https://leetcode.com/problems/sort-list/

```python
def merge(self, left, right):
    head = ListNode(0)
    current = head
    while left and right:
        if left.val <= right.val:
            current.next = left
            left = left.next
        else:
            current.next = right
            right = right.next
        current = current.next
    if not left:
        current.next = right
    elif not right:
        current.next = left
    return head.next   
def sortList(self, head):
    if not head or not head.next:
            return head
    mid = head
    tmp = head
    while mid.next and tmp.next and tmp.next.next:
        mid = mid.next
        tmp = tmp.next.next
    right = self.sortList(mid.next)
    mid.next = None
    left = self.sortList(head)
    return self.merge(left, right)
```
