# Python Fundamentals

[← Back to index](../README.md)

## Variables and output
```python
name = "Student"
age = 20
print(f"Hello, {name}! Age: {age}")
```

## Control flow
```python
for i in range(3):
    print(i)

if age >= 18:
    print("adult")
else:
    print("minor")
```

## Lists and dictionaries
```python
nums = [1, 2, 3]
nums.append(4)
user = {"name": "Ana", "role": "admin"}
print(user["role"])
```

## Functions
```python
def add(a, b):
    return a + b
```

## Security example: hashing
```python
import hashlib
print(hashlib.sha256(b"hello").hexdigest())
```

## My Reflection
I learned how Python can be used to create programs through variables, data types, conditions, loops, and other basic programming concepts. The activity helped me understand how instructions are written and executed by a computer. I realized that debugging is an important part of programming because errors can help me identify what needs to be corrected. Python is also useful in cybersecurity for automation, data processing, and security-related scripting.

## Review Questions
1. Difference between a list and a dictionary?
2. What does a function's `return` do?
3. Why is hashing different from encryption?
