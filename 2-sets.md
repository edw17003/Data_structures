# Sets
## Introduction
A set is a data structure that represents a collection of unique elements. It is commonly used when you need to store a group of items without any specific order and ensure that each item appears only once. In other words, **a set is a collection of distinct objects, in which duplicates are not allowed.**

## Basic Setup
Python has a built in 'set' class for working with sets. This makes creating sets as easy as calling the built-in 'set' method.
```python
my_set = set()
```
Adding and Removing Elements using python's built-in methods:
```python
# Adding elements to the set
my_set.add(4)       # {4}
my_set.update([5, 6, 7]) # {4, 5, 6, 7}

# Removing elements from the set
my_set.remove(5)    # {4, 6, 7}
my_set.discard(6)   # {4, 7}
my_set.pop()        # {7}
```
_Note: pop() removes a random element from the set. In the example above, it may remove 4 some times, and 7 at other times. Remember, data is in no particular order in sets._

## Use Cases
Because Sets ensure that each item of data is unique, they are commonly used to contrast data between multiple data sets. Two common examples are intersections and unions.

<picture>
  <img alt="Union and intersection diagram." src="https://www.shutterstock.com/image-vector/union-intersection-sets-260nw-1847364970.jpg">
</picture>

_Source: shutterstock.com_

## Example: Finding Common Elements
Suppose we have two sets, and we need to find the common elements that are in both sets. Here's how we would do it using python's built-in "intersection" method:
```python
set1 = {1, 2, 3, 4, 5}
set2 = {4, 5, 6, 7, 8}

common_elements = set1.intersection(set2)

print(common_elements) # {4, 5}
```

## Problem To Solve
Suppose we have two sets, 'set1' and 'set2'. Write some code that outputs whether or not set1 is a subset of set2. [Link to Solution](subset-check.md)

## Operations and Performance
- Adding Elements: The new element is added to the set. **O(1)**.
- Removing Elements: Search the set for the given value and remove it. In the worst case scenario, you will traverse the entire set to find the desired element. **O(n)**.
- Intersection: You need to check for the smaller set whether each of its elements is a member of the larger set. **O(min(n, m))**.
- Union: 

[Back to Welcome Page](0-welcome.md)