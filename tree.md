# tree

+[Binary Tree Inorder Traversal](#binary-tree-inorder-traversal)
+[Symmetric Tree](#symmetric-tree)
+[Maximum Depth of Binary Tree](#maximum-depth-of-binary-tree)
+[Same Tree](#same-tree)
+[Invert Binary Tree](#invert-binary-tree)
+[Path Sum](#path-sum)
+[Binary Tree Level Order Traversal](#binary-tree-level-order-traversal)
+[Subtree of Another Tree](#subtree-of-another-tree)
+[Kth Smallest Element in a BST](#kth-smallest-element-in-a-bst)
+[Validate Binary Search Tree](#validate-binary-search-tree)
+[Binary Search Tree Iterator](#binary-search-tree-iterator)

## Maximum Depth of Binary Tree

https://leetcode.com/problems/maximum-depth-of-binary-tree/

```python
def maxDepth(self, root):       
    if root == None:
        return 0
    return(1 + max(self.maxDepth(root.right), self.maxDepth(root.left)))
```    
