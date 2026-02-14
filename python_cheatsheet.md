# Python Cheat Sheet

## 1. Map

```python
nums = [1, 2, 3]
result = list(map(lambda x: x*x, nums))
print(result)
```

---

## 2. Filter

```python
nums = [1, 2, 3, 4]
even = list(filter(lambda x: x % 2 == 0, nums))
print(even)
```

---

## 3. Sorted

```python
data = [("a", 3), ("b", 1)]
print(sorted(data, key=lambda x: x[1]))
```

---

## 4. Enumerate

```python
for index, value in enumerate(["a", "b"]):
    print(index, value)
```

---

## 5. Zip

```python
a = [1, 2]
b = [3, 4]
print(list(zip(a, b)))
```

---

## Conclusion
These built-in functions are important.
