---
title: Dsa Example
date: 2025-07-21
author: Your Name
cell_count: 33
score: 30
---

```python
# 20250721
```


```python
https://chatgpt.com/c/687e332e-1d00-8012-b8a4-92d0fc133b42
```


```python
class Stack:
    def __init__(self):
        self.stack = []
```


```python
def push(self, item):
        print(f"Pushed {item}")
        self.stack.append(item)

```


```python
 def pop(self):
        if not self.is_empty():
            print(f"Popped {self.stack[-1]}")
            return self.stack.pop()
        return None
```


```python
def is_empty(self):
        return len(self.stack) == 0

```


```python
 def peek(self):
        return self.stack[-1] if self.stack else None

```


```python
def display(self):
        print("Stack:", self.stack)
```


```python
class Queue:
    def __init__(self):
        self.queue = []

```


```python
 def enqueue(self, item):
        print(f"Enqueued {item}")
        self.queue.append(item)

```


```python
 def dequeue(self):
        if not self.is_empty():
            print(f"Dequeued {self.queue[0]}")
            return self.queue.pop(0)
        return None

```


```python
 def is_empty(self):
        return len(self.queue) == 0

```


```python
  def display(self):
        print("Queue:", self.queue)

```


```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
```


```python
class LinkedList:
    def __init__(self):
        self.head = None
```


```python
def insert_end(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            print(f"Inserted {data} at head")
```


```python
 else:
            temp = self.head
            while temp.next:
                temp = temp.next
            temp.next = new_node
            print(f"Inserted {data} at end")
```


```python
  def display(self):
        temp = self.head
        print("LinkedList:", end=" ")
        while temp:
            print(temp.data, end=" -> ")
            temp = temp.next
        print("None")
```


```python
class TreeNode:
    def __init__(self, val):
        self.val = val
        self.left = None
        self.right = None
```


```python

def inorder(root):
    if root:
        inorder(root.left)
        print(root.val, end=" ")
        inorder(root.right)
```


```python

def preorder(root):
    if root:
        print(root.val, end=" ")
        preorder(root.left)
        preorder(root.right)
```


```python
def postorder(root):
    if root:
        postorder(root.left)
        postorder(root.right)
        print(root.val, end=" ")

```


```python
class BST:
    def __init__(self):
        self.root = None

```


```python
 def insert(self, val):
        self.root = self._insert(self.root, val)
```


```python
def _insert(self, node, val):
        if not node:
            print(f"Inserted {val}")
            return TreeNode(val)
        if val < node.val:
            node.left = self._insert(node.left, val)
        else:
            node.right = self._insert(node.right, val)
        return node
```


```python
    def inorder(self):
        print("Inorder Traversal:")
        inorder(self.root)
        print()
```


```python
if __name__ == "__main__":
    print("--- Stack ---")
    s = Stack()
    s.push(1)
    s.push(2)
    s.pop()
    s.display()
```


```python
   print("\n--- Queue ---")
    q = Queue()
    q.enqueue(10)
    q.enqueue(20)
    q.dequeue()
    q.display()
```


```python
 print("\n--- Linked List ---")
    ll = LinkedList()
    ll.insert_end(5)
    ll.insert_end(10)
    ll.display()
```


```python
 print("\n--- Binary Tree Traversals ---")
    bt_root = TreeNode(1)
    bt_root.left = TreeNode(2)
    bt_root.right = TreeNode(3)
    bt_root.left.left = TreeNode(4)
    bt_root.left.right = TreeNode(5)
```


```python
print("Inorder:")
    inorder(bt_root)
    print("\nPreorder:")
    preorder(bt_root)
    print("\nPostorder:")
    postorder(bt_root)
```


```python
 print("\n\n--- Binary Search Tree ---")
    bst = BST()
```


```python
for val in [7, 3, 9, 1, 5]:
        bst.insert(val)
    bst.inorder()

```


---
**Score: 30**