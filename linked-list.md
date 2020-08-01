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

## Middle of the Linked List

https://leetcode.com/problems/middle-of-the-linked-list/

## Reverse Linked List

https://leetcode.com/problems/reverse-linked-list/

## Merge Two Sorted Lists
 
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
## Remove Nth Node From End of List

https://leetcode.com/problems/remove-nth-node-from-end-of-list/

## Linked List Cycle II

https://leetcode.com/problems/linked-list-cycle-ii/

## Linked List Cycle

https://leetcode.com/problems/linked-list-cycle/

## Reorder List

https://leetcode.com/problems/reorder-list/

## Intersection of Two Linked Lists

https://leetcode.com/problems/intersection-of-two-linked-lists/

## Sort List

https://leetcode.com/problems/sort-list/
