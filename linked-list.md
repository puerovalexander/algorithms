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
## Remove Nth Node From End of List

https://leetcode.com/problems/remove-nth-node-from-end-of-list/

## Linked List Cycle II

https://leetcode.com/problems/linked-list-cycle-ii/

## Linked List Cycle

https://leetcode.com/problems/linked-list-cycle/

## Intersection of Two Linked Lists

https://leetcode.com/problems/intersection-of-two-linked-lists/

## Sort List

https://leetcode.com/problems/sort-list/
