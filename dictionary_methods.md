
# Dictionary Methods in Python

## 1. Introduction
Dictionary is a built-in data type in Python.
It stores data in key-value pairs.
Dictionary is mutable and unordered (before Python 3.7).
From Python 3.7+, insertion order is maintained.
It is implemented using Hash Table.
Average Time Complexity:
- Access: O(1)
- Insert: O(1)
- Delete: O(1)

---

## 2. Creating Dictionary

```python
student = {"name": "Abhay", "age": 21, "branch": "CSE"}
print(student)
```

Explanation:
Here we created a dictionary with three key-value pairs.

---

## 3. Accessing Elements

```python
print(student["name"])
print(student.get("age"))
```

get() is safer because it does not give error if key is missing.

---

## 4. Adding and Updating

```python
student["city"] = "Delhi"
student.update({"age": 22})
print(student)
```

---

## 5. Removing Elements

```python
student.pop("city")
print(student)
```

---

## 6. Looping Through Dictionary

```python
for key in student:
    print(key, student[key])

for key, value in student.items():
    print(key, value)
```

---

## 7. Dictionary Comprehension

```python
squares = {x: x*x for x in range(1, 6)}
print(squares)
```

---

## Conclusion
Dictionary is very useful for storing structured data.
It provides fast lookup using hashing.
