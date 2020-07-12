## Binary Tree Level Order Traversal

https://leetcode.com/problems/binary-tree-level-order-traversal/

```python
def levelOrder(self, root):
    if root == None:
        return []
     res = []
     q =deque([(root,0)])
     while q:
        n,l = q.popleft()
        if len(res) < l +1:
           res.append([])
        res[l].append(n.val)
        if n.left:
           q.append((n.left,l+1))
        if n.right:
           q.append((n.right,l+1))
     return res 
```
