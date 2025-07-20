---
title: Ifelse
date: 2025-07-21
author: Your Name
cell_count: 5
score: 5
---

```python
num = int(input("enter a number"))
if num > 0:
    print("positive")
elif num < 0:
    print("negative")
else:
    print("zero")
```

    enter a number 4
    

    positive
    


```python
a = int(input("enter number1:"))
b = int(input("enter number2:"))
if a>b:
        print("a is greater")
elif b>a:
        print("b is greater")
else:
        print("both are equal")
```

    enter number1: 3
    enter number2: 4
    

    b is greater
    


```python
num = int(input("enter a numbre"))
if num%3 == 0 and num%5 == 0:
    print("number is divisible by 3 and 5")
else:
    print("number is not divisible by 3 and 5")
```

    enter a numbre 4
    

    number is not divisible by 3 and 5
    


```python
email = input("enter your email:")

if "@" in email and "." in email and email.index('@') < email.rindex('.'):
    print("Valid email format")
else:
    print("Invalid email format")

```

    enter your email: kvnkumar2006@gmail.com
    

    Valid email format
    


```python

```


---
**Score: 5**