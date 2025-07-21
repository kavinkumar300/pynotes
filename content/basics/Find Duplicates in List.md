---
title: Find Duplicates In List
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
def find_duplicates(lst):
    seen = set()
    duplicates = set()
```


```python
for item in lst:
```


```python
 if item in seen:
            duplicates.add(item)
```


```python
else:
            seen.add(item)
```


```python
return list(duplicates)
```


```python
print(find_duplicates([1, 2, 3, 2, 4, 1]))
```


---
**Score: 5**