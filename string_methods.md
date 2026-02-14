
# String Methods in Python

## 1. Introduction
String is immutable in Python.
Once created, it cannot be changed.

---

## 2. Basic Methods

```python
text = "  Hello World  "

print(text.strip())
print(text.lower())
print(text.upper())
print(text.replace("World", "Python"))
```

---

## 3. Splitting and Joining

```python
words = text.split()
print(words)

joined = "-".join(words)
print(joined)
```

---

## 4. Searching

```python
print(text.find("World"))
print(text.count("l"))
```

---

## 5. Checking Methods

```python
print("abc".isalpha())
print("123".isdigit())
```

---

## Conclusion
String methods always return new string.
Original string remains unchanged.
