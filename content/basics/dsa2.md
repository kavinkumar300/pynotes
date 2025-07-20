---
title: Dsa2
date: 2025-07-21
author: Your Name
cell_count: 84
score: 80
---

```python
# 20250721
```


```python

```


```python
print("=== Linear Search ===")
```


```python
arr = [5, 2, 9, 1, 7]
target = 9
found = False
```


```python
for i in range(len(arr)):
```


```python
if arr[i] == target:
```


```python
print(f"{target} found at index {i}")
```


```python
 found = True
        break
```


```python
if not found:
    print("Element not found")
```


```python
print("\n" + "="*50 + "\n")
```


```python
print("=== Bubble Sort ===")
arr = [64, 25, 12, 22, 11]
```


```python
print("Before sort:", arr)
n = len(arr)
```


```python
for i in range(n):
```


```python
for j in range(0, n-i-1):
```


```python
 if arr[j] > arr[j+1]:
            arr[j], arr[j+1] = arr[j+1], arr[j]
```


```python
print("After sort:", arr)
```


```python
print("\n" + "="*50 + "\n")
```


```python
print("=== Stack (LIFO) ===")
```


```python
stack = []
stack.append(10)
stack.append(20)
stack.append(30)
```


```python
print("Stack after push:", stack)
```


```python
stack.pop()
```


```python
print("Stack after pop:", stack)
```


```python
print("\n" + "="*50 + "\n")
```


```python
print("=== Queue (FIFO) ===")
from collections import deque
```


```python
queue = deque()
queue.append(100)
queue.append(200)
queue.append(300)
```


```python
print("Queue after enqueue:", list(queue))
```


```python
queue.popleft()
```


```python
print("Queue after dequeue:", list(queue))
```


```python
print("\n" + "="*50 + "\n")
```


```python
print("=== Singly Linked List ===")
```


```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
```


```python
head = Node(1)
node2 = Node(2)
node3 = Node(3)
```


```python
head.next = node2
```


```python
node2.next = node3
```


```python
temp = head
```


```python
while temp:
```


```python
  print(temp.data, end=" -> ")
```


```python
temp = temp.next
```


```python
print("None")
```


```python
print("\n" + "="*50 + "\n")
```


```python
print("=== Binary Search ===")
```


```python
arr = [1, 3, 5, 7, 9, 11]
target = 7
low = 0
high = len(arr) - 1
found = False
```


```python
while low <= high:
```


```python
mid = (low + high) // 2
```


```python
if arr[mid] == target:
```


```python
print(f"{target} found at index {mid}")
```


```python
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
    print("Element not found")
```


```python
print("\n" + "="*50 + "\n")
```


```python
print("=== Factorial Using Recursion ===")
```


```python
def factorial(n):
    if n == 1:
        return 1
    return n * factorial(n - 1)
```


```python
print("5! =", factorial(5))
```


```python
print("\n" + "="*50 + "\n")
```


```python
print("=== Merge Sort ===")
```


```python
def merge_sort(arr):
```


```python
 if len(arr) > 1:
        mid = len(arr) // 2
        L = arr[:mid]
        R = arr[mid:]
```


```python
 merge_sort(L)
        merge_sort(R)

        i = j = k = 0
```


```python
while i < len(L) and j < len(R):
            if L[i] < R[j]:
                arr[k] = L[i]
                i += 1
```


```python
  else:
                arr[k] = R[j]
                j += 1
            k += 1
```


```python
while i < len(L):
            arr[k] = L[i]
            i += 1
            k += 1
```


```python
 while j < len(R):
            arr[k] = R[j]
            j += 1
            k += 1
```


```python
merge_arr = [38, 27, 43, 3, 9, 82, 10]
print("Before sort:", merge_arr)
```


```python
merge_sort(merge_arr)
print("After sort:", merge_arr)
```


```python
print("\n" + "="*50 + "\n")
```


```python
print("=== Hash Table ===")
```


```python
hash_table = {}
hash_table["name"] = "Alice"
hash_table["age"] = 25
hash_table["city"] = "New York"

```


```python
for key in hash_table:
    print(f"{key}: {hash_table[key]}")
```


```python
print("\n" + "="*50 + "\n")
```


```python
graph = {
    'A': ['B', 'C'],
    'B': ['D', 'E'],
    'C': ['F'],
    'D': [],
    'E': ['F'],
    'F': []
}
```


```python
visited = set()
queue = []
```


```python
queue.append('A')
visited.add('A')
```


```python
while queue:
    node = queue.pop(0)
```


```python
print(node, end=" ")
```


```python
 for neighbor in graph[node]:
        if neighbor not in visited:
            visited.add(neighbor)
            queue.append(neighbor)

```


```python
print("\n" + "="*50 + "\n")
```


```python
print("=== Binary Tree Inorder Traversal ===")
```


```python
class TreeNode:
    def __init__(self, key):
        self.left = None
        self.right = None
        self.val = key
```


```python
def inorder(root):
    if root:
        inorder(root.left)
        print(root.val, end=' ')
        inorder(root.right)
```


```python
root = TreeNode(50)
root.left = TreeNode(30)
root.right = TreeNode(70)
root.left.left = TreeNode(20)
```


```python
root.left.right = TreeNode(40)
root.right.left = TreeNode(60)
root.right.right = TreeNode(80)

```


```python
print("Inorder traversal:")
inorder(root)
```


```python
print("\n" + "="*50 + "\n")
```


---
**Score: 80**