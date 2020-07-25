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
