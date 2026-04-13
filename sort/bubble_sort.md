# Bubble Sort (Optimized) in Python

## 📌 Input

```python
nums = [1, 2, 3, 4, 5, 6]
```

---

## ✅ Code (Optimized with Early Exit)

```python
def bubble_sort(nums):
    n = len(nums)
    for i in range(n-2, -1, -1):
        flag = False
        for j in range(0, i+1):
            if nums[j] > nums[j+1]:
                nums[j], nums[j+1] = nums[j+1], nums[j]
                flag = True
        if flag == False:
            return nums
    return nums

print(bubble_sort(nums))
```

---

## 🔍 Explanation

* Traverse the array multiple times
* Compare adjacent elements and swap if needed
* Largest element moves to the end in each pass
* Optimization: If no swaps happen (`flag == False`), array is already sorted → exit early

---

## 🧠 Example

Initial:

```python
[1, 2, 3, 4, 5, 6]
```

Since the array is already sorted:

* No swaps in first iteration
* Function exits early

Output:

```python
[1, 2, 3, 4, 5, 6]
```

---

## 🔁 Code (Without Optimization)

```python
def bubble_sort(nums):
    n = len(nums)
    for i in range(n-2, -1, -1):
        for j in range(0, i+1):
            if nums[j] > nums[j+1]:
                nums[j], nums[j+1] = nums[j+1], nums[j]
    return nums

print(bubble_sort(nums))
```

---

## ⏱️ Time Complexity

| Case    | Complexity |
| ------- | ---------- |
| Best    | O(n)       |
| Average | O(n²)      |
| Worst   | O(n²)      |

---

## 💾 Space Complexity

* O(1) → In-place sorting

---

## ⚠️ Key Points (Interview)

* Stable sorting algorithm
* Easy to implement but inefficient for large datasets
* Optimization with `flag` improves best case to O(n)
* Good for understanding sorting fundamentals

---

## ✅ Output

```python
[1, 2, 3, 4, 5, 6]
```
