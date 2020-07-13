## Maximum Depth of Binary Tree

https://leetcode.com/problems/maximum-depth-of-binary-tree/

```python
def maxDepth(self, root):       
    if root == None:
        return 0
    return(1 + max(self.maxDepth(root.right),self.maxDepth(root.left)))
```    
