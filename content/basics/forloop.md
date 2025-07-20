---
title: Forloop
date: 2025-07-21
author: Your Name
cell_count: 9
score: 5
---

```python
# created : 20250629
```


```python

```


```python
x = [(1,2),(3,4),(4,5)]
for a,b in x:
    print(a, "plus", b, "equals" , a+b)

```

    1 plus 2 equals 3
    3 plus 4 equals 7
    4 plus 5 equals 9
    


```python
num = int(input("enter a number: "))
factorial = 1
for i in range(num, 1, -1):
    factorial = factorial * i
print("factorial:", factorial)

```

    enter a number:  5
    

    factorial: 120
    


```python
number = int(input("enter a number"))
for i in range(1,11):
    answer = number * i
    print(f"{number} x {i} = {answer}")
```

    enter a number 5
    

    5 x 1 = 5
    5 x 2 = 10
    5 x 3 = 15
    5 x 4 = 20
    5 x 5 = 25
    5 x 6 = 30
    5 x 7 = 35
    5 x 8 = 40
    5 x 9 = 45
    5 x 10 = 50
    


```python
numbers = [10,20,30,40]
total = 0
for i in numbers:
    total = total + i
    print("sum:", total)
```

    sum: 10
    sum: 30
    sum: 60
    sum: 100
    


```python
text = "kavin"
vowels = "aeiouAEIOU"
count = 0

for char in text:
    if char in vowels:
        count += 1

print(f"Number of vowels: {count}")

```

    Number of vowels: 2
    


```python
#20250721
```


```python

```


---
**Score: 5**