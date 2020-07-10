## Linked List Cycle
https://leetcode.com/problems/linked-list-cycle/
```python
 def hasCycle(self, head):
     fast = head
     slow = head        
     while(fast and fast.next):
         if fast.next == slow:
             return True 
         fast = fast.next.next                
         slow = slow.next        
     return False
```
