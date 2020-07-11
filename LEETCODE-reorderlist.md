##Reorder List
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
       lhead = head
       rhead = self.reverse(slow.next)
       slow.next = None           
       lcurrent = lhead
       rcurrent = rhead
       while lcurrent and rcurrent:
           tmp = rcurrent
           rcurrent = rcurrent.next
           tmp.next = lcurrent.next
           lcurrent.next = tmp
           lcurrent = lcurrent.next
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
