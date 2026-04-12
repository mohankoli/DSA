# Armstrong Number (Python)

## 🧩 Problem

Given an integer, check whether it is an Armstrong number.

An Armstrong number is a number that is equal to the sum of its digits raised to the power of the number of digits.

### Example

```
Input: 1634  
Output: True
```

---

## ✅ Approach

```python
num = 1634

def check_armstrong(num):
    n = num
    total = 0
    numOfDigit = len(str(n))
    
    while n > 0:
        rem = n % 10
        total = total + (rem ** numOfDigit)
        n = n // 10
        
    return total == num

print(check_armstrong(num))
```

---

## 🔥 Output

```
True
```

---

## 🧠 Key Concepts

* Count digits using `len(str(n))`
* Extract digits using `n % 10`
* Raise each digit to power of total digits
* Sum and compare with original number

---

## ⏱ Time Complexity

* **O(log₁₀(n))**

---

## 🚀 Interview Tips

Be ready to discuss:

* Why we use **power of number of digits**
* Difference between Armstrong and normal numbers
* Edge case: `0` → Armstrong number

---

## 💡 Bonus: Without String Conversion

```python
def count_digits(n):
    count = 0
    while n > 0:
        count += 1
        n //= 10
    return count

def check_armstrong(num):
    n = num
    total = 0
    numOfDigit = count_digits(n)
    
    while n > 0:
        rem = n % 10
        total += rem ** numOfDigit
        n //= 10
        
    return total == num
```
