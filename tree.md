## Subtree of Another Tree

https://leetcode.com/problems/subtree-of-another-tree/

```python
def isEqual(self, s, t):
    if not s and not t:
        return True
    if not s or not t:
        return False
    return s.val == t.val and self.isEqual(s.left, t.left) and self.isEqual(s.right, t.right)
def isSubtree(self, s, t):
    return s and (self.isEqual(s, t) or self.isSubtree(s.left, t) or self.isSubtree(s.right, t))
```    
         
