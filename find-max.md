```python
class Node:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None

def find_max(root):
    if root is None:
        return None

    max_value = root.data
    left_max = find_max(root.left)
    right_max = find_max(root.right)

    if left_max is not None and left_max > max_value:
        max_value = left_max
    if right_max is not None and right_max > max_value:
        max_value = right_max

    return max_value

node1 = Node(1)
node2 = Node(2)
node3 = Node(3)
node5 = Node(5)
node6 = Node(6)

node1.left = node2
node1.right = node3
node2.left = node5
node2.right = node6

max_value = find_max(node1)
print(max_value)
```
[Back to Trees Page](3-trees.md)