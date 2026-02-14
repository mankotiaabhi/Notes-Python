# List Methods in Python

## 1. Introduction
List is ordered and mutable data type.
It allows duplicate values.
List is stored in continuous memory.

Time Complexity:
- Access: O(1)
- Insert middle: O(n)

---

## 2. Creating List

```python
numbers = [1, 2, 3, 4]
print(numbers)
```

---

## 3. Adding Elements

```python
numbers.append(5)
numbers.insert(1, 100)
print(numbers)
```

---

## 4. Removing Elements

```python
numbers.remove(3)
numbers.pop()
print(numbers)
```

---

## 5. Sorting and Reversing

```python
numbers.sort()
numbers.reverse()
print(numbers)
```

---

## 6. List Comprehension

```python
squares = [x*x for x in range(1, 6)]
print(squares)
```

---

## 7. Looping Through List

```python
for num in numbers:
    print(num)
```

---

## Conclusion
List is flexible and widely used.
Sorting uses Timsort algorithm (O(n log n)).
