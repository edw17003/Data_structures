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

def is_balanced_parentheses(string):
    stack = Stack()

    for char in string:
        if char == "(":
            stack.push(char)
        elif char == ")":
            if stack.is_empty():
                return False
            stack.pop()

    return stack.is_empty()

# Test the function
def test_is_balanced_parentheses():
    assert is_balanced_parentheses("()()((()))") is True
    assert is_balanced_parentheses("((()(()))") is False
    assert is_balanced_parentheses("()((())") is False
    assert is_balanced_parentheses("") is True
    print("test passed")

test_is_balanced_parentheses()
```
[Back to Stacks Page](1-stacks.md)