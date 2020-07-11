 ##Merge Two Sorted Lists
 https://leetcode.com/problems/merge-two-sorted-lists/
 ```python
 def mergeTwoLists(self, l1, l2):     
     result_list = ListNode()
     tmp = result_list
     while l1 and l2:
         if l1.val < l2.val:
             tmp.next = ListNode(l1.val)
             l1 = l1.next
         else:
             tmp.next = ListNode(l2.val)
             l2 = l2.next
         tmp = tmp.next
     if l1:
         tmp.next = l1
     if l2:
         tmp.next = l2
     return result_list.next
```
