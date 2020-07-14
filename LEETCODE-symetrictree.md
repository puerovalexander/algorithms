## Symmetric Tree

https://leetcode.com/problems/symmetric-tree/

```python
def isSymmetric(self, root):        
    if not root:
        return True
    return self.check_symmetry(root.left,root.right)        
def check_symmetry(self,left,right):
    if not left or not right:
        return not left and not right
    return left.val == right.val and self.check_symmetry(left.left,right.right) and self.check_symmetry(left.right,right.left)
```    
