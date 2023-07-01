```python        
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
```
[Back to Welcome Page](0-welcome.md)