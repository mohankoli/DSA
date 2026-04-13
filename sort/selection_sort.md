# Selection Sort Implementation

## 📌 Input

```python
nums = [8, 6, 5, 1, 2, 5, 3, 4, 9, 10]
```

---

## ✅ Code

```python
def selection_sort(nums):
    n = len(nums)
    for i in range(0, n):
        min_idx = i
        for j in range(i+1, n):
            if nums[j] < nums[min_idx]:
                min_idx = j
        nums[i], nums[min_idx] = nums[min_idx], nums[i]
    print(nums)

selection_sort(nums)
```

---

## 🔍 Explanation

* Iterate through the array
* Assume current index `i` is the minimum
* Find the actual minimum element in the remaining array
* Swap it with the element at index `i`

---

## 🧠 Example

Initial:

```
[8, 6, 5, 1, 2, 5, 3, 4, 9, 10]
```

After sorting:

```
[1, 2, 3, 4, 5, 5, 6, 8, 9, 10]
```

---

## ⏱️ Time Complexity

* Best Case: O(n²)
* Average Case: O(n²)
* Worst Case: O(n²)

---

## 💾 Space Complexity

* O(1) → In-place sorting

---

## ⚠️ Notes

* Not a stable sorting algorithm
* Performs fewer swaps compared to Bubble Sort
* Useful for small datasets or when memory writes are costly
