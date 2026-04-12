# Palindrome Number (Python)

## 🧩 Problem

Given an integer, check whether it is a palindrome.

A number is a palindrome if it reads the same forward and backward.

### Example

```
Input: 121  
Output: True
```

---

## ✅ Approach

```python
num = 121

def check_palindrome(num):
    res = 0
    n = num
    
    while n > 0:
        rem = n % 10
        res = res * 10 + rem
        n = n // 10
    
    return res == num

print(check_palindrome(num))
```

---

## 🔥 Output

```
True
```

---

## 🧠 Key Concepts

* Reverse the number using:

  * `n % 10` → Extract last digit
  * `res * 10 + rem` → Build reversed number
  * `n // 10` → Remove last digit
* Compare reversed number with original

---

## ⏱ Time Complexity

* **O(log₁₀(n))**

---

## 🚀 Interview Tips

Be ready to discuss:

* Negative numbers (e.g., `-121` → Not a palindrome)
* Edge case: `0` → Palindrome
* Avoid converting to string (pure math approach preferred)

---

## 💡 Bonus: Optimized Approach (Half Reversal)

```python
def check_palindrome(num):
    if num < 0 or (num % 10 == 0 and num != 0):
        return False
    
    rev = 0
    while num > rev:
        rev = rev * 10 + num % 10
        num //= 10
    
    return num == rev or num == rev // 10
```
