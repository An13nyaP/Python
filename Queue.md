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

Next up: **Deque in Python** 🚀

