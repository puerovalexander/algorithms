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

```python
def getIntersectionNode(self, headA, headB):
    tmp1 = headA
    tmp2 = headB
    d = {}
    while tmp1:
        d[tmp1] = tmp1
        tmp1 = tmp1.next
    while tmp2:
        if tmp2 in d:
            return tmp2
        tmp2 = tmp2.next
    return None
```
## Sort List

https://leetcode.com/problems/sort-list/
