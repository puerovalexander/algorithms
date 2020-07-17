## Middle of the Linked List

https://leetcode.com/problems/middle-of-the-linked-list/

```python
def middleNode(self, head):      
    fast = head
    slow = head
    while fast.next != None:
        fast = fast.next.next
        slow = slow.next
    return slow
```    
