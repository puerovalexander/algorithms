 ## Kth Smallest Element in a BST
 
 https://leetcode.com/problems/kth-smallest-element-in-a-bst/
 
 ```python
 def kthSmallest(self, root, k):
     stack = []
     res = []
     while stack or root:
         while root:
             stack.append(root)
             root = root.left
         root = stack.pop()
         res.append(root)
         root = root.right
     return res[k-1].val
```
