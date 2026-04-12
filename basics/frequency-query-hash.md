# Frequency Query (Python)

## 🧩 Problem

Given two arrays:

* `m` → main array
* `n` → query array

For each element in `n`, print how many times it appears in `m`.

---

## ✅ Solution 1: Brute Force

```python
m = [5,3,2,2,1,5,5,7,5,10]
n = [10,111,1,9,5,6,7,2]

def find_count(m,n):
    for num in m:
        count=0
        for no in n:
            if num == no:
                count +=1
        print(count)

find_count(m,n)
```

---

## ✅ Solution 2: Using Hash Map (Dictionary)

```python
def find_count(m,n):
    hash={}
    for num in m:
        hash[num] = hash.get(num,0)+1
    for num in n:
        if num in hash:
            print(hash[num])
        else:
            print(0)

find_count(m,n)
```

---

## ✅ Solution 3: Using Hash Array

```python
def find_count(m,n):
    hash_list = [0]*11
    for num in m:
        hash_list[num] +=1
    for num in n:
        if num<0 or num>10:
            print(0)
        else:
            print(hash_list[num])

find_count(m,n)
```

---

## 🧠 Key Concepts

* Brute force → nested loops
* Hash map → fast lookup
* Hash array → works when range is small

---

## ⏱ Time Complexity

| Approach    | Complexity |
| ----------- | ---------- |
| Brute Force | O(m × n)   |
| Hash Map    | O(m + n)   |
| Hash Array  | O(m + n)   |

---

## 🚀 Interview Tips

* Start with **brute force**, then optimize
* Prefer **hash map** for general case
* Explain trade-offs clearly
