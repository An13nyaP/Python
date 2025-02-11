# Queue in Python

## Introduction
A **queue** is a linear data structure that follows the **First In, First Out (FIFO)** principle. This means that the first element added to the queue is the first one to be removed. Queues are widely used in scheduling tasks, managing requests, and buffering data.

## Queue Operations
The fundamental operations of a queue include:
- **Enqueue**: Adds an element to the end of the queue.
- **Dequeue**: Removes and returns the front element of the queue.
- **Front (Peek)**: Returns the front element without removing it.
- **isEmpty**: Checks if the queue is empty.
- **Size**: Returns the number of elements in the queue.

## Implementing Queue in Python
Python provides multiple ways to implement a queue:
1. Using a **list** (not efficient)
2. Using **collections.deque** (preferred for efficiency)
3. Using **queue.Queue** (thread-safe implementation)

### 1. Queue Implementation Using List (Not Recommended)
```python
class Queue:
    def __init__(self):
        self.queue = []
    
    def enqueue(self, item):
        self.queue.append(item)
    
    def dequeue(self):
        if not self.is_empty():
            return self.queue.pop(0)
        return "Queue is empty"
    
    def front(self):
        if not self.is_empty():
            return self.queue[0]
        return "Queue is empty"
    
    def is_empty(self):
        return len(self.queue) == 0
    
    def size(self):
        return len(self.queue)

# Example usage
q = Queue()
q.enqueue(10)
q.enqueue(20)
q.enqueue(30)
print(q.dequeue())  # Output: 10
print(q.front())  # Output: 20
print(q.is_empty())  # Output: False
```

### 2. Queue Implementation Using collections.deque (Efficient)
```python
from collections import deque

class Queue:
    def __init__(self):
        self.queue = deque()
    
    def enqueue(self, item):
        self.queue.append(item)
    
    def dequeue(self):
        if not self.is_empty():
            return self.queue.popleft()
        return "Queue is empty"
    
    def front(self):
        if not self.is_empty():
            return self.queue[0]
        return "Queue is empty"
    
    def is_empty(self):
        return len(self.queue) == 0
    
    def size(self):
        return len(self.queue)

# Example usage
q = Queue()
q.enqueue(5)
q.enqueue(15)
q.enqueue(25)
print(q.dequeue())  # Output: 5
```

### 3. Queue Implementation Using queue.Queue (Thread-Safe)
```python
from queue import Queue

q = Queue()
q.put(1)
q.put(2)
q.put(3)

print(q.get())  # Output: 1
print(q.get())  # Output: 2
```

## Time Complexity Analysis
| Operation | Complexity |
|-----------|------------|
| Enqueue | O(1) |
| Dequeue | O(1) |
| Front | O(1) |
| isEmpty | O(1) |
| Size | O(1) |

## Applications of Queue
- Process scheduling in operating systems
- Print spooling
- Breadth-First Search (BFS) in graphs
- Handling requests in web servers
- Data buffering in streaming applications

## Conclusion
Queues are fundamental data structures with multiple real-world applications. Using **collections.deque** is the best approach for efficient queue operations in Python.

---

# Deque in Python

## Introduction
A **deque** (double-ended queue) is a linear data structure that allows insertion and deletion from both ends. Unlike a regular queue (FIFO), a deque provides efficient operations from both ends, making it a versatile data structure.

Python provides a built-in **collections.deque** module that allows fast appends and pops from both ends with O(1) time complexity.

## Deque Operations
The fundamental operations of a deque include:
- **append(x)**: Adds element `x` to the right end.
- **appendleft(x)**: Adds element `x` to the left end.
- **pop()**: Removes and returns the rightmost element.
- **popleft()**: Removes and returns the leftmost element.
- **extend(iterable)**: Extends deque by appending elements from the iterable (right side).
- **extendleft(iterable)**: Extends deque by appending elements from the iterable (left side, reversed order).
- **rotate(n)**: Rotates the deque `n` steps to the right (negative `n` for left rotation).
- **reverse()**: Reverses the order of elements in the deque.
- **clear()**: Removes all elements from the deque.

## Implementing Deque in Python
### 1. Creating a Deque and Basic Operations
```python
from collections import deque

# Initializing a deque
d = deque()

# Appending elements
d.append(10)
d.append(20)
d.appendleft(5)
print(d)  # Output: deque([5, 10, 20])

# Removing elements
d.pop()  # Removes 20
d.popleft()  # Removes 5
print(d)  # Output: deque([10])
```

### 2. Extending and Rotating Deque
```python
from collections import deque

# Initializing a deque
d = deque([1, 2, 3])

# Extending deque from right and left
d.extend([4, 5])  # Adds at the right
d.extendleft([0, -1])  # Adds at the left (reversed order)
print(d)  # Output: deque([-1, 0, 1, 2, 3, 4, 5])

# Rotating deque
d.rotate(2)  # Right rotate by 2 steps
print(d)  # Output: deque([4, 5, -1, 0, 1, 2, 3])

d.rotate(-2)  # Left rotate by 2 steps
print(d)  # Output: deque([-1, 0, 1, 2, 3, 4, 5])
```

### 3. Reversing and Clearing Deque
```python
from collections import deque

d = deque([1, 2, 3, 4, 5])
d.reverse()
print(d)  # Output: deque([5, 4, 3, 2, 1])

d.clear()
print(d)  # Output: deque([])
```

## Time Complexity Analysis
| Operation | Complexity |
|-----------|------------|
| append() | O(1) |
| appendleft() | O(1) |
| pop() | O(1) |
| popleft() | O(1) |
| extend() | O(k) |
| extendleft() | O(k) |
| rotate() | O(k) |
| reverse() | O(n) |
| clear() | O(n) |

## Applications of Deque
- **Sliding window problems** (e.g., maximum of all subarrays of size `k`)
- **Undo/Redo operations**
- **Palindrome checking**
- **Job scheduling**
- **Tree level-order traversal (BFS)**

## Conclusion
Deque is a powerful and flexible data structure that provides O(1) operations for inserting and removing elements from both ends. **collections.deque** is the recommended way to implement deques in Python.





