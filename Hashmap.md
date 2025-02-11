# HashMap in Python

## Introduction
A **HashMap** (also known as a dictionary in Python) is a data structure that stores key-value pairs. It provides **fast insertion, deletion, and lookup** operations using a **hashing mechanism**. Python implements HashMap using the built-in `dict` type.

## Key Features of HashMap
- Stores key-value pairs
- Provides O(1) average time complexity for lookup, insert, and delete operations
- Keys must be **immutable** (e.g., strings, numbers, tuples)
- Values can be of any data type

## Operations in HashMap
1. **Insertion** - Adding a key-value pair
2. **Deletion** - Removing a key-value pair
3. **Accessing elements** - Retrieving values using keys
4. **Checking existence** - Checking if a key exists
5. **Iterating over elements**
6. **Getting the size** of the HashMap

## Implementing HashMap in Python

### 1. Creating a HashMap
```python
# Creating a HashMap
hash_map = {}

# Another way using dict()
hash_map = dict()
```

### 2. Inserting Key-Value Pairs
```python
hash_map['name'] = 'Alice'
hash_map['age'] = 25
hash_map['city'] = 'New York'
print(hash_map)  # Output: {'name': 'Alice', 'age': 25, 'city': 'New York'}
```

### 3. Accessing Elements
```python
print(hash_map['name'])  # Output: Alice

# Using get() to avoid KeyError
print(hash_map.get('country', 'Not Found'))  # Output: Not Found
```

### 4. Deleting Elements
```python
del hash_map['age']
print(hash_map)  # Output: {'name': 'Alice', 'city': 'New York'}

# Using pop()
age = hash_map.pop('age', 'Key Not Found')
print(age)  # Output: Key Not Found
```

### 5. Checking if a Key Exists
```python
print('name' in hash_map)  # Output: True
print('age' in hash_map)  # Output: False
```

### 6. Iterating Over a HashMap
```python
# Iterating over keys
for key in hash_map:
    print(key, hash_map[key])

# Iterating over key-value pairs
for key, value in hash_map.items():
    print(key, value)
```

### 7. Getting the Size of a HashMap
```python
print(len(hash_map))  # Output: 2
```

## Time Complexity Analysis
| Operation     | Average Case | Worst Case |
|--------------|-------------|------------|
| Insert       | O(1)        | O(n)       |
| Delete       | O(1)        | O(n)       |
| Lookup       | O(1)        | O(n)       |
| Iteration    | O(n)        | O(n)       |

## Applications of HashMap
- Implementing caches (e.g., LRU Cache)
- Storing configuration settings
- Counting occurrences of elements
- Indexing in databases
- Storing adjacency lists in graph algorithms

## Conclusion
HashMaps (dictionaries in Python) are one of the most powerful and widely used data structures. They provide **fast operations** and are used in a variety of applications ranging from **caching to graph traversal**.

