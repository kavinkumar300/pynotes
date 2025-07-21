---
title: Dsa Structures Algorithms
date: 2025-07-21
author: Your Name
cell_count: 56
score: 55
---

```python
# 20250721
```


```python
https://chatgpt.com/c/687e332e-1d00-8012-b8a4-92d0fc133b42
```


```python
from collections import deque, defaultdict
import heapq
```


```python
class Stack:
```


```python
def __init__(self):
        self.items = []

```


```python
  def push(self, item):
        print(f"Stack push: {item}")
        self.items.append(item)

```


```python
 def pop(self):
        if self.items:
            item = self.items.pop()
            print(f"Stack pop: {item}")
            return item
        return None
```


```python
def is_empty(self):
        return len(self.items) == 0

```


```python
class Queue:
    def __init__(self):
        self.items = deque()

```


```python
def enqueue(self, item):
        print(f"Queue enqueue: {item}")
        self.items.append(item)

```


```python
 def dequeue(self):
        if self.items:
            item = self.items.popleft()
            print(f"Queue dequeue: {item}")
            return item
        return None
```


```python
def is_empty(self):
        return len(self.items) == 0

```


```python
class TreeNode:
    def __init__(self, val):
        self.val = val
        self.left = None
        self.right = None

```


```python
def bfs_tree(root):
    print("\nBinary Tree BFS:")
```


```python
if not root:
        return
    queue = Queue()
    queue.enqueue(root)
```


```python
while not queue.is_empty():
        node = queue.dequeue()
        print(node.val, end=' ')
```


```python
if node.left:
            queue.enqueue(node.left)
```


```python
if node.right:
            queue.enqueue(node.right)

```


```python
def dfs_inorder(root):
    if root:
        dfs_inorder(root.left)
        print(root.val, end=' ')
        dfs_inorder(root.right)

```


```python
def merge_sort(arr):
    if len(arr) <= 1:
        return arr
        print(f"Sorting: {arr}")
```


```python
 mid = len(arr) // 2
    left = merge_sort(arr[:mid])
```


```python
 right = merge_sort(arr[mid:])
    return merge(left, right)

```


```python
def merge(left, right):
    result = []
    i = j = 0
```


```python
 print(f"Merging {left} & {right}")
    while i < len(left) and j < len(right):
```


```python
 if left[i] < right[j]:
            result.append(left[i])
            i += 1
```


```python
else:
            result.append(right[j])
            j += 1
```


```python
 result.extend(left[i:])
    result.extend(right[j:])
    return result
```


```python
def binary_search(arr, target):
    print(f"\nBinary Search for {target} in {arr}")
    low, high = 0, len(arr) - 1
```


```python
 while low <= high:
        mid = (low + high) // 2
```


```python
 if arr[mid] == target:
            print(f"Found at index {mid}")
     return mid
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
    print("Not found")
    return -1

```


```python
def min_heap_example(elements):
    print("\nMin Heap:")
```


```python
 heap = []
    for el in elements:
        heapq.heappush(heap, el)
```


```python
 print(f"Pushed {el}, Heap: {heap}")
    print(f"Min Element: {heapq.heappop(heap)}")

```


```python
class Graph:
    def __init__(self):
        self.graph = defaultdict(list)

```


```python
def add_edge(self, u, v):
        self.graph[u].append(v)
        print(f"Added edge: {u} -> {v}")
```


```python
def dfs(self, start):
        print("\nGraph DFS:")
        visited = set()
        stack = Stack()
        stack.push(start)
```


```python
 while not stack.is_empty():
            node = stack.pop()
            if node not in visited:
```


```python
print(node, end=' ')
                visited.add(node)
                for neighbor in reversed(self.graph[node]):
                    stack.push(neighbor)
```


```python
def bfs(self, start):
        print("\nGraph BFS:")
        visited = set()
        queue = Queue()
```


```python
 queue.enqueue(start)
        visited.add(start)
```


```python
   while not queue.is_empty():
            node = queue.dequeue()
```


```python
  print(node, end=' ')
```


```python
for neighbor in self.graph[node]:
                if neighbor not in visited:
                    visited.add(neighbor)
                    queue.enqueue(neighbor)

```


```python
if __name__ == "__main__":
```


```python
print("\n--- Binary Tree ---")
    root = TreeNode(10)
    root.left = TreeNode(5)
```


```python
 root.right = TreeNode(15)
    root.left.left = TreeNode(2)
    root.left.right = TreeNode(7)
    bfs_tree(root)
```


```python
   print("\nIn-order DFS:")
    dfs_inorder(root)

```


```python
  print("\n\n--- Merge Sort & Binary Search ---")
    arr = [9, 1, 6, 3, 5, 2, 8]
```


```python
sorted_arr = merge_sort(arr)
    print("Sorted array:", sorted_arr)
    binary_search(sorted_arr, 5)
```


```python
 min_heap_example([4, 1, 7, 3, 2, 6])
```


```python
 print("\n\n--- Graph ---")
    g = Graph()
    g.add_edge('A', 'B')
    g.add_edge('A', 'C')
    g.add_edge('B', 'D')
```


```python
 g.add_edge('C', 'D')
    g.add_edge('D', 'E')
    g.dfs('A')
    g.bfs('A')
```


```python

```


---
**Score: 55**