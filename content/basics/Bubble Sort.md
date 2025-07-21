---
title: Bubble Sort
date: 2025-07-21
author: Your Name
cell_count: 8
score: 5
---

```python
# 20250721
```


```python
https://chatgpt.com/c/687d381f-a7cc-8012-aa0e-4d36b9b1488c
```


```python
def bubble_sort(arr):
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
 return arr
```


```python
print(bubble_sort([5, 1, 4, 2, 8]))
```


---
**Score: 5**