---
title: Simple Task Manager
date: 2025-07-21
author: Your Name
cell_count: 55
score: 55
---

```python
# 20250721
```


```python

```


```python
import os
```


```python
TASKS_FILE = "tasks.txt"
```


```python
def load_tasks():
    tasks = []
```


```python
if os.path.exists(TASKS_FILE):
        with open(TASKS_FILE, 'r') as f:
```


```python
 for line in f:
                parts = line.strip().split('|')
```


```python
 if len(parts) == 2:
                    task, status = parts
                    tasks.append({'task': task, 'done': status == 'done'})
```


```python
 return tasks
```


```python
def save_tasks(tasks):
    with open(TASKS_FILE, 'w') as f:
```


```python
 for task in tasks:
            status = 'done' if task['done'] else 'pending'
            f.write(f"{task['task']}|{status}\n")
```


```python
def show_tasks(tasks):
    print("\n📝 Your Tasks:")
```


```python
if not tasks:
        print("  No tasks yet.")
```


```python
 else:
        for i, task in enumerate(tasks, 1):
            status = "✅" if task['done'] else "❌"
```


```python
print(f"  {i}. {task['task']} [{status}]")
    print()
```


```python
def add_task(tasks):
    task = input("Enter new task: ").strip()
```


```python
if task:
        tasks.append({'task': task, 'done': False})
        print("✅ Task added.")
```


```python
 else:
        print("⚠️ Task cannot be empty.")
```


```python
try:
        num = int(input("Enter task number to mark done: "))
```


```python
if 1 <= num <= len(tasks):
            tasks[num - 1]['done'] = True
            print("✔️ Task marked as done.")
```


```python
 print("✔️ Task marked as done.")
```


```python
 else:
            print("⚠️ Invalid task number.")
```


```python
except ValueError:
        print("❌ Please enter a number.")
```


```python
def delete_task(tasks):
    show_tasks(tasks)
```


```python
try:
        num = int(input("Enter task number to delete: "))
```


```python
if 1 <= num <= len(tasks):
            removed = tasks.pop(num - 1)
```


```python
 print(f"🗑️ Deleted: {removed['task']}")
```


```python
 else:
            print("⚠️ Invalid task number.")
```


```python
except ValueError:
        print("❌ Please enter a number.")

```


```python
def clear_tasks(tasks):
    confirm = input("Are you sure you want to clear all tasks? (y/n): ").lower()
```


```python
if confirm == 'y':
        tasks.clear()
```


```python
print("🧹 All tasks cleared.")
```


```python
else:
        print("Cancelled.")
```


```python
def show_menu():
```


```python
print("\n📋 Task Manager")
```


```python
print("1. View Tasks")
```


```python
print("2. Add Task")
```


```python
print("3. Mark Task as Done")
```


```python
print("4. Delete Task")
```


```python
 print("5. Clear All Tasks")
```


```python
 print("6. Exit")
```


```python
def main():
    tasks = load_tasks()
```


```python
while True:
        show_menu()
        choice = input("Choose an option (1-6): ").strip()
```


```python
if choice == '1':
            show_tasks(tasks)
```


```python
elif choice == '2':
            add_task(tasks)
```


```python
elif choice == '3':
            mark_done(tasks)
```


```python
elif choice == '4':
            delete_task(tasks)
```


```python
elif choice == '5':
            clear_tasks(tasks)
```


```python
elif choice == '6':
            save_tasks(tasks)
```


```python
 print("💾 Tasks saved. Goodbye!")
 break
```


```python
 else:
            print("❌ Invalid choice. Please select between 1 and 6.")
```


```python
if __name__ == "__main__":
    main()
```


```python

```


```python

```


```python

```


---
**Score: 55**