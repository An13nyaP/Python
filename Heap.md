# Heap in Python

## Introduction
A **heap** is a special tree-based data structure that satisfies the **heap property**. It is commonly implemented as a **binary heap**, where:
- **Min Heap**: The parent node is always smaller than or equal to its children.
- **Max Heap**: The parent node is always greater than or equal to its children.

Heaps are mainly used for priority queues and efficient selection problems like finding the k-th smallest/largest element.

## Heap Operations
The primary operations of a heap include:
- **Insertion**: Add an element while maintaining the heap property.
- **Deletion (Extract Min/Max)**: Remove the root element and reheapify.
- **Peek (Get Min/Max)**: Return the root element without removing it.
- **Heapify**: Convert an unordered array into a heap.
- **Heap Sort**: Sort elements using a heap.

## Implementing Heap in Python
Python provides a built-in `heapq` module for working with heaps.

### 1. Min Heap Implementation Using `heapq`
```python
import heapq

# Create a min heap
min_heap = []
heapq.heappush(min_heap, 10)
heapq.heappush(min_heap, 5)
heapq.heappush(min_heap, 20)
heapq.heappush(min_heap, 1)

print(heapq.heappop(min_heap))  # Output: 1 (Smallest element)
print(min_heap[0])  # Peek at the minimum element
```

### 2. Max Heap Implementation Using `heapq`
Python does not provide a direct max heap, but we can use negative values to simulate one.
```python
import heapq

# Create a max heap
max_heap = []
heapq.heappush(max_heap, -10)
heapq.heappush(max_heap, -5)
heapq.heappush(max_heap, -20)
heapq.heappush(max_heap, -1)

print(-heapq.heappop(max_heap))  # Output: 20 (Largest element)
print(-max_heap[0])  # Peek at the maximum element
```

### 3. Converting an Array into a Heap (Heapify)
```python
import heapq

arr = [10, 5, 20, 1]
heapq.heapify(arr)  # Converts the list into a min heap
print(arr)  # Output: [1, 5, 20, 10] (Heap structure)
```

### 4. Heap Sort Using `heapq`
```python
import heapq

def heap_sort(iterable):
    heapq.heapify(iterable)
    return [heapq.heappop(iterable) for _ in range(len(iterable))]

arr = [10, 5, 20, 1]
sorted_arr = heap_sort(arr)
print(sorted_arr)  # Output: [1, 5, 10, 20]
```

## Time Complexity Analysis
| Operation | Complexity |
|-----------|------------|
| Insertion | O(log n) |
| Deletion | O(log n) |
| Peek | O(1) |
| Heapify | O(n) |
| Heap Sort | O(n log n) |

## Applications of Heaps
- **Priority Queues**: Used in scheduling and graph algorithms (Dijkstra’s, Prim’s Algorithm).
- **Heap Sort**: Efficient sorting method.
- **Finding k-th Smallest/Largest Elements**.
- **Merging k Sorted Lists**.
- **Median Finding in a Stream**.

## Conclusion
Heaps are powerful data structures for efficient priority management. The `heapq` module makes heap operations easy in Python, with a default min heap implementation.

---

