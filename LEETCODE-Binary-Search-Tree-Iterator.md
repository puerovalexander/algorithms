##  Binary Search Tree Iterator

https://leetcode.com/problems/binary-search-tree-iterator/

```python
class BSTIterator(object):
    def __init__(self, root):
        self.stack = list()
        self.addLeft(root)
    def addLeft(self, root):
        while root:
            self.stack.append(root)
            root = root.left   
    def next(self):
        top = self.stack.pop()
        if top.right:
            self.addLeft(top.right)
        return top.val
    def hasNext(self):
        return len(self.stack) > 0
```
