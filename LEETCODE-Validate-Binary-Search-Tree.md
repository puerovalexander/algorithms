## Validate Binary Search Tree

https://leetcode.com/problems/validate-binary-search-tree/

``` python
def isValidBST(self, root):       
    if not root:
        return True
    stack = [(root, float('-inf'), float('inf'))]
    while stack:
        root, lower, upper = stack.pop()
        if not root:
            continue
        value = root.val
        if value <= lower or value >= upper:
            return False
        stack.append((root.right, value, upper))
        stack.append((root.left, lower, value))
    return True
```    
