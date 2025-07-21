---
title: Fibonacci
date: 2025-07-21
author: Your Name
cell_count: 12
score: 10
---

```python
# 20250721
```


```python
https://chatgpt.com/c/687d381f-a7cc-8012-aa0e-4d36b9b1488c
```


```python
def recursive_fib(k):
        if k <= 1:
            return k
        return recursive_fib(k - 1) + recursive_fib(k - 2)
```


```python
def fibonacci(n, return_list=False, use_recursion=False):
    if n <= 0:
        print("Please enter a positive integer.")
        return [] if return_list else None
```


```python
result = []
    if use_recursion:
        for i in range(n):
            result.append(recursive_fib(i))
```


```python
else:
        a, b = 0, 1
        for _ in range(n):
            result.append(a)
            a, b = b, a + b
```


```python
if return_list:
        return result
```


```python
else:
```


```python
 print("Fibonacci Sequence:")
```


```python
print(" ".join(map(str, result)))
```


```python

```


```python

```


---
**Score: 10**