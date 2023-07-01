# Stacks
## Introduction
A stack is a data structure where the last item added is the first one to be removed. A phrase commonly associated with this is "Last In, First Out" (LIFO). I think of python stacks like a stack of plates: you can only access or remove the top-most plate. You wouldn't naturally add **or** remove from the middle or the bottom.

<picture>
  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://www.tutorialspoint.com/data_structures_algorithms/images/stack_representation.jpg">
</picture>

_Source: www.tutorialspoint.com_

## Basic Setup
```python
class Stack:
    def __init__(self):
        self.stack = []

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
```

## Problem To Solve
Suppose we have a string containing parentheses, and we need to check if the parentheses are balanced. Assuming that the "basic setup" portion is already in place, write a function that checks if the parentheses are balanced in a given string. [Link to Solution](balance-parens.md)

[Back to Welcome Page](0-welcome.md)