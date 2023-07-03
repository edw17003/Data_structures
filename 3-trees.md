# Trees
## Introduction
A Tree is a data structure that is made up by nodes which are linked together by pointers. There are various kinds of Trees, but in this tutorial we will look at Binary Trees. Binary Trees have a special structure where each node must have exactly two child nodes: a left child and a right child. These node references can be set to None or Null (see node 3 below).

***We will be using the following data for each of the examples used in this tutorial.***

<picture>
  <img alt="Binary Tree." src="https://static.javatpoint.com/ds/images/binary-tree.png">
</picture>

_Source: static.javatpoint.com_

## Basic Setup
```python
class Node:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None
```

## Example: Sum Descendant Values
Suppose we need to find the sum of all descendent values in a binary tree given a root node as the input. Here's an example solution:

_Note: This example uses the same data as shown in the image in the introduction_
```python
def sum_values(root):
    if (root == None):
        return 0
    return root.data + sum_values(root.left) + sum_values(root.right)

# Create the nodes
node1 = Node(1)
node2 = Node(2)
node3 = Node(3)
node5 = Node(5)
node6 = Node(6)

# Structure the tree
node1.left = node2
node1.right = node3
node2.left = node5
node2.right = node6

print(sum_values(node1)) # 17
```
The sum_values function calls itself recursively in order to calculate the sum of the left and right children nodes. It starts with the current node's value, adds the sum of its left child's descendents values, then adds the sum of its right descendents values.

Because trees require traversal through an unknown number of nodes, recursion makes working with trees much simpler.

## Problem To Solve
Suppose we want to find the maximum value in a binary tree. Write a function that takes a root node as the input and returns the maximum value of the descendents of the given root node. [Link to Solution](find-max.md)

## Operations and Performance
- 

[Back to Welcome Page](0-welcome.md)