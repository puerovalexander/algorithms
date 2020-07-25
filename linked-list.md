## Linked List Cycle II

https://leetcode.com/problems/linked-list-cycle-ii/

```python
def detectCycle(self, head):
    fast = head
    slow = head        
    while fast and fast.next:
        if fast.next == slow:
            return fast 
        fast = fast.next.next                
        slow = slow.next        
    return None
```
