---
title: Binary Search
date: 2025-07-21
author: Your Name
cell_count: 9
score: 5
---

```python
# 202507221
```


```python
https://chatgpt.com/c/687d381f-a7cc-8012-aa0e-4d36b9b1488c
```


```python
def binary_search(arr, target):
    low, high = 0, len(arr)-1
```


```python
while low <= high:
        mid = (low + high) // 2
```


```python
if arr[mid] == target:
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
 return -1
```


```python
print(binary_search([1, 3, 5, 7, 9], 5))
```


---
**Score: 5**