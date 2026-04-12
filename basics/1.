# Reverse Number in Python

## 🧩 Problem

Given an integer, reverse its digits.

### Example

```
Input: 5872  
Output: 2785
```

---

## ✅ Correct Approach

```python
def reverseNumber(num):
    res = 0
    while num > 0:
        n = num % 10          # Extract last digit
        res = res * 10 + n    # Shift left and append
        num = num // 10       # Remove last digit
    return res

print(reverseNumber(5872))
```

---

## 🔥 Output

```
2785
```

---

## 🧠 Key Concepts

* `num % 10` → Extract last digit
* `res * 10` → Shift digits left
* `+ n` → Add extracted digit
* `num // 10` → Remove last digit

---

## ⏱ Time Complexity

* **O(log₁₀(n))**

---

## 🚀 Interview Tips

Be ready to discuss:

* Handling **negative numbers**
* Handling **integer overflow**
* Edge cases like `0`

---

## 💡 Bonus: Handle Negative Numbers

```python
def reverseNumber(num):
    sign = -1 if num < 0 else 1
    num = abs(num)
    
    res = 0
    while num > 0:
        res = res * 10 + num % 10
        num //= 10
    
    return sign * res
```
