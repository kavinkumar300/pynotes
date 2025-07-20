---
title: Dsa
date: 2025-07-21
author: Your Name
cell_count: 34
score: 30
---

```python
# 20250721
```


```python

```


```python
print("=== Linear Search ===")
```

    === Linear Search ===
    


```python
arr = [5, 3, 8, 6, 7]
target = 6
found = False
```


```python
for i in range(len(arr)):
    if arr[i] == target:
        print(f"Found {target} at index {i}")
        found = True
        break
```

    Found 6 at index 3
    


```python
if not found:
    print(f"{target} not found")
```


```python
print("\n=== Bubble Sort ===")
arr = [64, 34, 25, 12, 22, 11, 90]
```

    
    === Bubble Sort ===
    


```python
print("Unsorted:", arr)
n = len(arr)
for i in range(n):
    for j in range(0, n - i - 1):
        if arr[j] > arr[j + 1]:
            arr[j], arr[j + 1] = arr[j + 1], arr[j]
```

    Unsorted: [64, 34, 25, 12, 22, 11, 90]
    


```python
print("Sorted:", arr)
```

    Sorted: [11, 12, 22, 25, 34, 64, 90]
    


```python
print("\n=== Stack Using List ===")
stack = []
stack.append(1)
stack.append(2)
stack.append(3)
```

    
    === Stack Using List ===
    


```python
print("Stack after pushing:", stack)
```

    Stack after pushing: [1, 2, 3]
    


```python
stack.pop()
print("Stack after popping:", stack)
```

    Stack after popping: [1, 2]
    


```python
print("\n=== Queue Using deque ===")
from collections import deque
queue = deque()
queue.append(10)
queue.append(20)
queue.append(30)
```

    
    === Queue Using deque ===
    


```python
print("Queue after enqueue:", list(queue))
```

    Queue after enqueue: [10, 20, 30]
    


```python
queue.popleft()
print("Queue after dequeue:", list(queue))
```

    Queue after dequeue: [20, 30]
    


```python
print("\n=== Binary Search ===")
```

    
    === Binary Search ===
    


```python
arr = [2, 4, 6, 8, 10, 12, 14]
target = 10
low = 0
high = len(arr) - 1
found = False
```


```python
while low <= high:
    mid = (low + high) // 2
    if arr[mid] == target:
        print(f"Found {target} at index {mid}")
        found = True
        break
```


```python
elif arr[mid] < target:
        low = mid + 1
```


```python
else:
        high = mid - 1
```


```python
if not found:
    print(f"{target} not found")
```


```python
print("\n=== Factorial Using Recursion ===")
def factorial(n):
    if n == 1:
        return 1
    return n * factorial(n - 1)
```


```python
print("5! =", factorial(5))
```


```python
print("\n=== Simple Singly Linked List ===")
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
```


```python
head = Node(1)
second = Node(2)
third = Node(3)
```


```python
head.next = second
second.next = third
```


```python
current = head
while current:
```


```python
print(current.data, end=" -> ")
    current = current.next
print("None")
```


```python
print("\n=== Dictionary (Hash Table style) ===")
```


```python
hash_map = {}
```


```python
hash_map["apple"] = 100
```


```python
hash_map["banana"] = 200
```


```python
hash_map["orange"] = 150
```


```python
for key in hash_map:
    print(f"{key} => {hash_map[key]}")
```


---
**Score: 30**