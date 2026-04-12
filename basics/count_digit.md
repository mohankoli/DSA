# Count Digits in a Number (Python)

## 🧩 Problem

Given an integer, count the number of digits in it.

### Example

```
Input: 5872  
Output: 4
```

---

## ✅ Approach

```python
num = 5872

def count_digit(num):
    count = 0
    while num > 0:
        count = count + 1
        num = num // 10
    return count

print(count_digit(num))
```

---

## 🔥 Output

```
4
```

---

## 🧠 Key Concepts

* `num // 10` → Removes last digit
* Loop runs until number becomes `0`
* Each iteration increases digit count

---

## ⏱ Time Complexity

* **O(log₁₀(n))**

---

## 🚀 Interview Tips

Be ready to discuss:

* Handling **0 as input** (edge case)
* Handling **negative numbers**
* Alternative approach using **string conversion**

---

## 💡 Bonus: Handle Edge Cases

```python
def count_digit(num):
    if num == 0:
        return 1
    
    num = abs(num)
    count = 0
    
    while num > 0:
        count += 1
        num //= 10
    
    return count
```
