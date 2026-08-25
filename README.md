<h1 align="center">🔍 Linear Search</h1>

<p align="center">
  <i>A complete, beginner-friendly learning package for the Linear Search algorithm — concept, complexity, animated walkthrough, and a clean Python implementation.</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Algorithm-Searching-4472C4?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Difficulty-Beginner-3fb950?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/License-MIT-lightgrey?style=for-the-badge"/>
</p>

---

## 📽️ Visual Walkthrough

The animation below shows exactly how Linear Search checks each element, one at a time, from left to right, until it finds the target value.

<p align="center">
  <img src="linear_search_demo.gif" alt="Linear Search animated walkthrough" width="640"/>
</p>

> 🟡 Amber = currently being checked  ·  ⚪ Gray = checked, no match  ·  🟢 Green = target found

---

## 📖 What is Linear Search?

Linear Search (also called **Sequential Search**) is the simplest searching algorithm. It walks through a list **one element at a time**, from the beginning, and compares each element to the target value. If it finds a match, it returns that position. If it reaches the end without a match, it reports that the value isn't present.

It doesn't require the list to be sorted — which is its biggest advantage over algorithms like Binary Search, at the cost of being slower on large datasets.

---

## ⚙️ How It Works

1. Start at the first element of the list (index `0`).
2. Compare the current element with the target value.
3. If it matches → return the current index. Done.
4. If it doesn't match → move to the next index and repeat.
5. If the end of the list is reached with no match → return `-1` (not found).

---

## ⏱️ Complexity Analysis

| Case | Time Complexity | Description |
|---|---|---|
| **Best Case** | `O(1)` | Target is the first element |
| **Average Case** | `O(n)` | Target is somewhere in the middle |
| **Worst Case** | `O(n)` | Target is the last element, or not present at all |
| **Space Complexity** | `O(1)` | No extra space needed — search happens in place |

---

## 🧠 Pseudocode

```text
function linearSearch(array, target):
    for index from 0 to length(array) - 1:
        if array[index] == target:
            return index
    return -1   // not found
```

---

## 🐍 Python Implementation

```python
def linear_search(arr, target):
    """
    Searches for `target` in `arr` by checking each element sequentially.

    Parameters:
        arr (list): The list to search through.
        target: The value to search for.

    Returns:
        int: The index of `target` if found, otherwise -1.
    """
    for index, value in enumerate(arr):
        if value == target:
            return index
    return -1


if __name__ == "__main__":
    numbers = [8, 23, 4, 17, 11, 42, 6, 29, 15, 37]
    target = 42

    result = linear_search(numbers, target)

    if result != -1:
        print(f"Found {target} at index {result}")
    else:
        print(f"{target} not found in the list")
```

> 💡 See [`linear_search.py`](./linear_search.py) for the full commented implementation, and the [lecture notes](./Linear%20Search%20-%20Lecture.pdf) for a deeper explanation of the concept and complexity analysis.

---

## ▶️ Running It Locally

```bash
git clone https://github.com/zain-cs/1-Linear-Search.git
cd 1-Linear-Search
python linear_search.py
```

No external dependencies required — pure Python standard library.

---

## 📂 Repository Contents

| File | Description |
|---|---|
| `linear_search.py` | Commented Python implementation of the algorithm |
| `Linear Search - Lecture.pdf` | Full concept explanation, complexity breakdown, and examples |
| `Linear Search - Lecture.docx` | Editable version of the lecture notes |

---

## 🗺️ Part of a DSA Learning Series

This repo is part of an ongoing series where I implement and document one Data Structures & Algorithms concept at a time — building a public, structured trail as I go through DSA.

📌 Explore more of the series on my [GitHub profile](https://github.com/zain-cs?tab=repositories).

---

<p align="center">
  Made with 🐍 by <a href="https://github.com/zain-cs">Muhammad Zain Ul Abidin</a>
</p>
