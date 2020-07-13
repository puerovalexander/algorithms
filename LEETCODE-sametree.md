## Same Tree

https://leetcode.com/problems/same-tree/

```python
def isSameTree(self, p, q):        
    if p == None and q == None:
        return True
    if p == None or q == None:
        return False
    if p.val != q.val:
        return False
    if p.left == None and q.left == None and p.right == None and q.right == None:
        return True       
    return self.isSameTree(p.left,q.left) and self.isSameTree(p.right,q.right)
```    
