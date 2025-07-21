---
title: Student Grade Tracker 
date: 2025-07-21
author: Your Name
cell_count: 21
score: 20
---

```python
# 20250721
```


```python
https://chatgpt.com/c/687d381f-a7cc-8012-aa0e-4d36b9b1488c
```


```python
def get_student_details():
    name = input("Enter student name: ")
    roll_no = input("Enter roll number: ")
    return name, roll_no
```


```python
def get_marks(subjects):
    marks = {}
    for subject in subjects:
```


```python
while True:
            try:
                mark = float(input(f"Enter marks for {subject}: "))
```


```python
if 0 <= mark <= 100:
                    marks[subject] = mark
                    break
```


```python
 else:
                    print("Marks should be between 0 and 100.")
```


```python
except ValueError:
                print("Enter a valid number.")
    return marks
```


```python
def calculate_average(marks):
    total = sum(marks.values())
    return total / len(marks)
```


```python
def get_remark(average):
    if average >= 90:
        return "Excellent"
```


```python
elif average >= 75:
        return "Very Good"
```


```python
elif average >= 60:
        return "Good"
```


```python
elif average >= 40:
        return "Pass"
```


```python
else:
        return "Fail"
```


```python
def display_report(name, roll_no, marks, average, remark):
```


```python
print("\n--- Student Report ---")
    print(f"Name      : {name}")
    print(f"Roll No   : {roll_no}")
```


```python
 print("\nMarks:")
    for subject, mark in marks.items():
        print(f"{subject:10}: {mark}")
```


```python
 print(f"\nAverage   : {average:.2f}")
    print(f"Remark    : {remark}")
```


```python
def main():
    subjects = ["Math", "Science", "English", "History", "Computer"]
    name, roll_no = get_student_details()
    marks = get_marks(subjects)
    average = calculate_average(marks)
    remark = get_remark(average)
    display_report(name, roll_no, marks, average, remark)
```


```python
if __name__ == "__main__":
    main()
```


```python

```


---
**Score: 20**