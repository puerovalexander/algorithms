## Binary Tree Inorder Traversal

https://leetcode.com/problems/binary-tree-inorder-traversal/

```python
def inorderTraversal(self, root):        
    tree = []
    if not root:
        return tree
    tree.extend(self.inorderTraversal(root.left))
    tree.append(root.val)
    tree.extend(self.inorderTraversal(root.right))
    return tree 
```    
