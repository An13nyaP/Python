# Arrays in Python

## Introduction
An **array** is a collection of elements stored in contiguous memory locations. In Python, lists serve as dynamic arrays, allowing flexible size and operations.

## Array Operations
### 1. Creating an Array (List in Python)
```python
# Creating an array (list)
numbers = [1, 2, 3, 4, 5]
print(numbers)  # Output: [1, 2, 3, 4, 5]
```

### 2. Accessing Elements
```python
print(numbers[0])  # Output: 1
print(numbers[-1])  # Output: 5 (Last element)
```

### 3. Modifying Elements
```python
numbers[1] = 10  # Modifies second element
print(numbers)  # Output: [1, 10, 3, 4, 5]
```

### 4. Adding Elements
```python
numbers.append(6)  # Adds at the end
print(numbers)  # Output: [1, 10, 3, 4, 5, 6]
```

### 5. Inserting at a Specific Position
```python
numbers.insert(2, 99)  # Insert 99 at index 2
print(numbers)  # Output: [1, 10, 99, 3, 4, 5, 6]
```

### 6. Removing Elements
```python
numbers.remove(99)  # Removes first occurrence of 99
print(numbers)  # Output: [1, 10, 3, 4, 5, 6]
```

### 7. Deleting Elements by Index
```python
del numbers[1]  # Deletes second element
print(numbers)  # Output: [1, 3, 4, 5, 6]
```

### 8. Popping Elements
```python
last_element = numbers.pop()  # Removes last element
print(last_element)  # Output: 6
print(numbers)  # Output: [1, 3, 4, 5]
```

### 9. Iterating Through an Array
```python
for num in numbers:
    print(num)
```

### 10. Searching for an Element
```python
if 4 in numbers:
    print("4 is in the list")  # Output: 4 is in the list
```

### 11. Sorting an Array
```python
numbers.sort()
print(numbers)  # Output: [1, 3, 4, 5]
```

### 12. Reversing an Array
```python
numbers.reverse()
print(numbers)  # Output: [5, 4, 3, 1]
```

### 13. Finding the Length of an Array
```python
print(len(numbers))  # Output: 4
```

## Time Complexity Analysis
| Operation | Complexity |
|-----------|------------|
| Access (indexing) | O(1) |
| Append (end) | O(1) |
| Insert (middle) | O(n) |
| Delete by value | O(n) |
| Delete by index | O(n) |
| Pop (end) | O(1) |
| Pop (arbitrary index) | O(n) |
| Search | O(n) |
| Sort | O(n log n) |

## Conclusion
Arrays (lists in Python) provide flexibility in storage and manipulation of elements. Understanding these operations and their time complexities is essential for efficient coding and problem-solving.

---

# Strings in Python

## Introduction
A **string** is a sequence of characters enclosed in quotes. Strings in Python are immutable, meaning their content cannot be changed after creation.

## String Operations
### 1. Creating a String
```python
# Single and double quotes
string1 = 'Hello'
string2 = "World"
print(string1, string2)  # Output: Hello World
```

### 2. Accessing Characters
```python
word = "Python"
print(word[0])  # Output: P
print(word[-1])  # Output: n
```

### 3. Slicing Strings
```python
print(word[0:4])  # Output: Pyth
print(word[:3])  # Output: Pyt
print(word[2:])  # Output: thon
```

### 4. Modifying Strings (Immutable)
```python
word = "Hello"
word = "World"  # Reassigning a new value
print(word)  # Output: World
```

### 5. String Concatenation
```python
str1 = "Hello"
str2 = " World"
result = str1 + str2
print(result)  # Output: Hello World
```

### 6. String Repetition
```python
print("Hello " * 3)  # Output: Hello Hello Hello
```

### 7. Checking Substrings
```python
sentence = "Python is fun"
print("Python" in sentence)  # Output: True
print("Java" in sentence)  # Output: False
```

### 8. String Methods
```python
text = "hello world"
print(text.upper())  # Output: HELLO WORLD
print(text.lower())  # Output: hello world
print(text.title())  # Output: Hello World
print(text.replace("world", "Python"))  # Output: hello Python
```

### 9. Splitting and Joining Strings
```python
sentence = "Python is fun"
words = sentence.split()  # Splits by space
print(words)  # Output: ['Python', 'is', 'fun']

new_sentence = "-".join(words)
print(new_sentence)  # Output: Python-is-fun
```

### 10. Removing Whitespaces
```python
text = "  hello  "
print(text.strip())  # Output: hello
print(text.lstrip())  # Output: 'hello  '
print(text.rstrip())  # Output: '  hello'
```

## Time Complexity Analysis
| Operation | Complexity |
|-----------|------------|
| Access (indexing) | O(1) |
| Concatenation | O(n) |
| Slicing | O(k) |
| Searching | O(n) |
| Length Calculation | O(1) |
| Splitting | O(n) |
| Joining | O(n) |

## Conclusion
Strings are fundamental in Python and widely used in text processing and manipulation. Understanding their properties and methods is crucial for efficient problem-solving.


