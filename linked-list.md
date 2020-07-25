## Reorder List

https://leetcode.com/problems/reorder-list/

```python
def reorderList(self, head):       
   if not head:
       return None
   else:
       slow = fast = head
       while fast and fast.next:
           slow = slow.next
           fast = fast.next.next
       l_head = head
       r_head = self.reverse(slow.next)
       slow.next = None           
       l_current = l_head
       r_current = r_head
       while l_current and r_current:
           tmp = r_current
           r_current = r_current.next
           tmp.next = l_current.next
           l_current.next = tmp
           l_current = l_current.next
           
def reverse(self, head):
    if not head:
        return None
    else:
        prev = None
        current  = head
        while current:
            current.next = prev
            current = current.next
            prev = current
        return prev
```         
