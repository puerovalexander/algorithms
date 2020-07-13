## Linked List Cycle II

https://leetcode.com/problems/linked-list-cycle-ii/

```python
def detectCycle(self, head):
    tmp = head
    a = []
    while(tmp):
        if tmp not in a:
            a.append(tmp)
        else:
            return tmp
        tmp = tmp.next
    return None
```
