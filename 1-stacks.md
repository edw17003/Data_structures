# Stacks
## Introduction
A stack is a data structure where the last item added is the first one to be removed. A phrase commonly associated with this is "Last In, First Out" (LIFO). I think of python stacks like a stack of plates: you can only access or remove the top-most plate. You wouldn't naturally **add or remove** from the middle or the bottom.

<picture>
  <img alt="LIFO diagram." src="https://www.tutorialspoint.com/data_structures_algorithms/images/stack_representation.jpg">
</picture>

_Source: tutorialspoint.com_

## Basic Setup
```python
class Stack:
    def __init__(self, items=None):
        if items is None:
            self.stack = []
        else:
            self.stack = list(items)

    def push(self, item):
        self.stack.append(item)

    def pop(self):
        if self.is_empty():
            return None
        return self.stack.pop()

    def is_empty(self):
        return len(self.stack) == 0

    def size(self):
        return len(self.stack)
```
## Example: Finding the Maximum in a Stack
Suppose we have a stack of integers, and we need to find the maximum element in the stack. Here's an example solution:
```python
def find_maximum(stack):
    if stack.is_empty():
        return None

    max_element = stack.pop()
    while not stack.is_empty():
        element = stack.pop()
        if element > max_element:
            max_element = element

    return max_element

# Test the function
def test_find_maximum():
    assert find_maximum(Stack([5, 2, 9, 1, 7])) == 9
    assert find_maximum(Stack([])) is None
    print("test passed")

test_find_maximum()
```

## Problem To Solve
Suppose we have a string containing parentheses, and we need to check if the parentheses are balanced. Write a function that checks if the parentheses are balanced in a given string. [Link to Solution](is-balanced.md)

## Operations and Performance
- Push Operation: The new element is added to the top of the stack. **O(1)**.
- Pop Operation: The topmost element is removed from the stack. **O(1)**.
- Peek Operation: Allows you to access the top element without modifying the stack. **O(1)**.
- Search Operation: Search the stack for a given value. Linear time complexity. In the worst case, you will traverse the entire stack to find the desired element. Therefore, time complexity is equal to the number of elements in the stack (n). **O(n)**.

[Back to Welcome Page](0-welcome.md)