# Find All Divisors of a Number (Python)

## 🧩 Problem

Given an integer, return all its divisors.

---

## ✅ Solution 1

```python
num = 20

def find_divisible(num):
    res = []
    for i in range(1, num+1):
        if num%i == 0:
            res.append(i)
    return res

print(find_divisible(num))
```

---

## ✅ Solution 2

```python
def find_divisible(num):
    res = []
    for i in range(1,num//2):
        if num%i == 0:
            res.append(i)
    res.append(num)
    return res

print(find_divisible(num))
```
