## Path Sum

https://leetcode.com/problems/path-sum/

```python
def hasPathSum(self, root, sum):
    if not root:
        return False
        
    if not (root.left or root.right) and root.val == sum:
        return True
        
    sum -= root.val
        
    return self.hasPathSum(root.left, sum) or self.hasPathSum(root.right, sum)
```
