# Basic Hashing (Frequency Count in Python)

## 🧩 Problem

Given a list of numbers, count the frequency of each element.

### Example

```
Input: [5,6,7,7,1,9,11,1,1,5,1]  
Output: {5:2, 6:1, 7:2, 1:4, 9:1, 11:1}
```

---

## ✅ Solution 1

```python
nums = [5,6,7,7,1,9,11,1,1,5,1]

def basic_hashing(nums):
    freq_map = {}
    for i in range(0,len(nums)):
        if nums[i] in freq_map:
            freq_map[nums[i]] += 1
        else:
            freq_map[nums[i]] = 1
    return freq_map

print(basic_hashing(nums))
```

---

## ✅ Solution 2

```python
nums = [5,6,7,7,1,9,11,1,1,5,1]

def basic_hashing(nums):
    map={}
    for i in range(0,len(nums)):
        map[nums[i]] = map.get(nums[i],0) +1
    return map

print(basic_hashing(nums))
```

---

## 🧠 Key Concepts

* Dictionary used as **hash map**
* `map.get(key, 0)` → avoids checking existence
* Efficient frequency counting

---

## ⏱ Time Complexity

* **O(n)**

---

## 🚀 Interview Tips

* Prefer `get()` method for cleaner code
* Can also use `collections.Counter` (advanced)
