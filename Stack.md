# Stack in Python

## Introduction
A **stack** is a linear data structure that follows the **Last In, First Out (LIFO)** principle, meaning the last element added is the first one to be removed. Stacks are widely used in applications such as expression evaluation, function calls, and backtracking algorithms.

## Stack Operations
The fundamental operations of a stack include:
- **Push**: Adds an element to the top of the stack.
- **Pop**: Removes and returns the top element of the stack.
- **Peek (Top)**: Returns the top element without removing it.
- **isEmpty**: Checks if the stack is empty.
- **Size**: Returns the number of elements in the stack.

## Implementing Stack in Python
Python provides multiple ways to implement a stack:
1. Using a **list**
2. Using **collections.deque** (preferred for efficiency)
3. Using **queue.LifoQueue** (thread-safe implementation)

### 1. Stack Implementation Using List
```python
class Stack:
    def __init__(self):
        self.stack = []
    
    def push(self, item):
        self.stack.append(item)
    
    def pop(self):
        if not self.is_empty():
            return self.stack.pop()
        return "Stack is empty"
    
    def peek(self):
        if not self.is_empty():
            return self.stack[-1]
        return "Stack is empty"
    
    def is_empty(self):
        return len(self.stack) == 0
    
    def size(self):
        return len(self.stack)

# Example usage
s = Stack()
s.push(10)
s.push(20)
s.push(30)
print(s.pop())  # Output: 30
print(s.peek())  # Output: 20
print(s.is_empty())  # Output: False
```

### 2. Stack Implementation Using collections.deque
```python
from collections import deque

class Stack:
    def __init__(self):
        self.stack = deque()
    
    def push(self, item):
        self.stack.append(item)
    
    def pop(self):
        if not self.is_empty():
            return self.stack.pop()
        return "Stack is empty"
    
    def peek(self):
        if not self.is_empty():
            return self.stack[-1]
        return "Stack is empty"
    
    def is_empty(self):
        return len(self.stack) == 0
    
    def size(self):
        return len(self.stack)

# Example usage
s = Stack()
s.push(5)
s.push(15)
s.push(25)
print(s.pop())  # Output: 25
```

### 3. Stack Implementation Using queue.LifoQueue
```python
from queue import LifoQueue

stack = LifoQueue()
stack.put(1)
stack.put(2)
stack.put(3)

print(stack.get())  # Output: 3
print(stack.get())  # Output: 2
```

## Time Complexity Analysis
| Operation | Complexity |
|-----------|------------|
| Push | O(1) |
| Pop | O(1) |
| Peek | O(1) |
| isEmpty | O(1) |
| Size | O(1) |

## Applications of Stack
- Function calls (Call Stack)
- Undo/Redo operations in editors
- Parenthesis matching in expressions
- Depth-First Search (DFS) in graphs

## Conclusion
Stacks are an essential data structure with various real-world applications. Understanding different implementations in Python helps in choosing the right approach based on efficiency and use case.

---

Next up: **Queue in Python** 🚀

