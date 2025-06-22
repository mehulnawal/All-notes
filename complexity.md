# 📘 Time Complexity Notes

---

## 📑 Index

- [📘 Time Complexity Notes](#-time-complexity-notes)
  - [📑 Index](#-index)
  - [1. What is Time Complexity?](#1-what-is-time-complexity)
  - [2. Common Time Complexities](#2-common-time-complexities)
  - [3. Time Complexity Table (How to Identify + Examples)](#3-time-complexity-table-how-to-identify--examples)
  - [4. Best Case vs Worst Case](#4-best-case-vs-worst-case)
  - [5. Tips to Reduce Time Complexity](#5-tips-to-reduce-time-complexity)

---

## 1. What is Time Complexity?

**Time Complexity** refers to how the runtime of an algorithm increases with the input size `n`.

It helps measure **efficiency** and compare algorithms.

---

## 2. Common Time Complexities

| Index | Big O            | Name                  |
| ----- | ---------------- | --------------------- |
| 1     | `O(1)`           | Constant Time         |
| 2     | `O(log n)`       | Logarithmic Time      |
| 3     | `O(n)`           | Linear Time           |
| 4     | `O(n log n)`     | Linearithmic Time     |
| 5     | `O(n²)`          | Quadratic Time        |
| 6     | `O(n³)`          | Cubic Time            |
| 7     | `O(2ⁿ)`          | Exponential Time      |
| 8     | `O(n!)`          | Factorial Time        |
| 9     | `O(n!)`          | Factorial Time        |
| 10    | `O(min(n1, n2))` | Min-based Linear Time |
| 11    | `O(max(n1, n2))` | Max-based Linear Time |

---

## 3. Time Complexity Table (How to Identify + Examples)

| Time Complexity  | How to Identify (Simplest Way)                                                                                         | Example Code Pattern                                          |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| `O(1)`           | No loop, constant-time operations                                                                                      | `return a + b;`                                               |
| `O(log n)`       | Input is divided by 2 (or factor) in loop/recursion                                                                    | `while (n > 0) { n = Math.floor(n / 2); }`                    |
| `O(n)`           | Single loop from 0 to `n` or over an array                                                                             | `for (let i = 0; i < n; i++)`                                 |
| `O(n log n)`     | Divide and conquer with sorting/merging                                                                                | `mergeSort(arr, 0, n - 1)`                                    |
| `O(n²)`          | Nested loop (loop inside a loop) over same input size                                                                  | `for (let i = 0; i < n; i++) { for (let j = 0; j < n; j++) }` |
| `O(n³)`          | Triple nested loop                                                                                                     | `for (i) for (j) for (k)`                                     |
| `O(2ⁿ)`          | Recursion branching into 2 calls at each level                                                                         | `fibonacci(n) { return fib(n-1) + fib(n-2) }`                 |
| `O(n!)`          | Permutations, recursion with full exploration                                                                          | `generateAllPermutations(arr)`                                |
| `O(min(n1, n2))` | Depends on the smaller of two inputs; typically used when looping till the smallest number (e.g., in GCD brute force). | `for (let i = 1; i <= Math.min(n1, n2); i++)`                 |
| `O(max(n1, n2))` | Depends on the larger of two inputs; usually appears in subtraction-based loops or unbalanced iterations.              | `while (a !== b) { a = a - b; }` where a = Math.max(n1, n2)   |


---

## 4. Best Case vs Worst Case

| Case       | Meaning                                 | Example                           |
| ---------- | --------------------------------------- | --------------------------------- |
| Best Case  | Fastest possible scenario               | Searching first element in a list |
| Worst Case | Slowest possible scenario (upper bound) | Searching last element in a list  |

---

## 5. Tips to Reduce Time Complexity

- Avoid nested loops → use hashing or prefix sums.
- Use efficient algorithms:  
  - Binary Search (`O(log n)`)  
  - Sorting with MergeSort instead of BubbleSort
- Use two-pointer, sliding window, or divide and conquer strategies.
- Precompute where possible (like sieve for primes).
- Use memoization or DP to avoid repeated work.

---

> 💡 Pro Tip: Time complexity measures **growth**, not exact time.
> Always pair it with **space complexity** and real-world constraints.

---
