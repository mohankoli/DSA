# Character Frequency Query (Python)

## 🧩 Problem

Given:

* A string `s`
* A list of query characters `q`

For each character in `q`, print how many times it appears in `s`.

---

## ✅ Solution 1: Using Hash Map (Dictionary)

```python id="c7v2qa"
s = "azyxyyzaaa"
q = ["a","z","t","y","p"]

def freq_char_count(s,q):
    hash_list = {}
    for ch in s:
        hash_list[ch] = hash_list.get(ch,0)+1
    print(hash_list)
    for ch in q:
        if ch in hash_list:
            print(hash_list[ch])
        else:
            print(0)

freq_char_count(s,q)
```

---

## ✅ Solution 2: Using ASCII (Hash Array)

```python id="3t4fsl"
def freq_char_count(s,q):
    hash_list = [0]*26
    for ch in s:
        ascii_values = ord(ch)
        index = ascii_values - 97
        hash_list[index] +=1
    for ch in q:
        ascii_values = ord(ch)
        index = ascii_values - 97
        print(hash_list[index])

freq_char_count(s,q)
```

---

## 🧠 Key Concepts

* Dictionary → works for any characters
* Array hashing → works for lowercase `a-z`
* `ord('a') = 97` → used for indexing

---

## ⏱ Time Complexity

* **O(n + q)**

---

## 🚀 Interview Tips

* Use dictionary for general cases
* Use array hashing when input is limited (a-z)
* Explain ASCII mapping clearly
