## Remove Nth Node From End of List

https://leetcode.com/problems/remove-nth-node-from-end-of-list/

```python
def removeNthFromEnd(self, head, n):       
    tmp = head
    node = head
    if (head == None or head.next == None):
        return None
    for i in range(n+1):
        if tmp:
            tmp = tmp.next
        else:
            return head.next
    while tmp:
        tmp = tmp.next
        node = node.next
    node.next = node.next.next
    return head
```        
