# 📘 DSA Pattern Recognition Sheet (Topic-wise with Keywords)

Each section is grouped by **topic**, showing:
- 🔢 Index
- 🧩 Pattern Name
- 🎯 How to Identify
- 🔍 Keywords / Triggers

---

## 📐 Arrays & Strings

| #   | Pattern Name            | How to Identify                                                    | Keywords / Triggers                              |
| --- | ----------------------- | ------------------------------------------------------------------ | ------------------------------------------------ |
| 1   | Sliding Window          | Look for fixed or variable size subarrays or substrings            | subarray, window, longest, exact size, at most K |
| 2   | Two Pointers            | Use two indices to move inward or outward (sorted input common)    | sorted, pair, reverse, move pointers             |
| 3   | Prefix Sum / Cumulative | Optimize subarray or range queries by storing sums                 | sum between, subarray sum, range, prefix sum     |
| 4   | Binary Search           | Search in a sorted array or on answer space                        | sorted, find, search, boundary, Kth, minimum     |
| 5   | Greedy                  | Choose best option at each step                                    | minimize, maximize, earliest, latest, optimal    |
| 6   | Monotonic Stack         | Maintain increasing or decreasing structure to track next elements | next greater, stock span, histogram, increasing  |

---

## 🔗 Linked Lists

| #   | Pattern Name         | How to Identify                                            | Keywords / Triggers                            |
| --- | -------------------- | ---------------------------------------------------------- | ---------------------------------------------- |
| 1   | Two Pointers         | Move two pointers at different speeds or toward each other | reverse list, remove nth node, merge, mid node |
| 2   | Fast & Slow Pointers | Use different speeds to detect cycles or find midpoint     | cycle detection, palindrome, loop, find middle |

---

## 📊 Intervals & Scheduling

| #   | Pattern Name           | How to Identify                                     | Keywords / Triggers                         |
| --- | ---------------------- | --------------------------------------------------- | ------------------------------------------- |
| 1   | Merge Intervals        | Combine overlapping time ranges or detect conflicts | intervals, calendar, overlap, merge, ranges |
| 2   | Greedy                 | Select most efficient schedule/order                | meeting room, max activity, minimize time   |
| 3   | Sorting + Two Pointers | Sort intervals and compare start/end                | events scheduling, overlapping intervals    |

---

## 🔁 Recursion & Backtracking

| #   | Pattern Name       | How to Identify                                   | Keywords / Triggers                                 |
| --- | ------------------ | ------------------------------------------------- | --------------------------------------------------- |
| 1   | Backtracking       | Generate all valid combinations/paths, undo steps | all ways, permutations, combinations, sudoku, paths |
| 2   | Recursion          | Solve by dividing problem into smaller parts      | repeated calls, divide and solve, decision tree     |
| 3   | Divide and Conquer | Split input, process recursively, merge results   | merge sort, quick sort, binary search               |

---

## 📈 Dynamic Programming

| #   | Pattern Name        | How to Identify                   | Keywords / Triggers                            |
| --- | ------------------- | --------------------------------- | ---------------------------------------------- |
| 1   | Dynamic Programming | Optimize overlapping subproblems  | count ways, max value, longest subsequence     |
| 2   | Memoization         | Top-down recursion with caching   | reduce recomputation, cache subproblem results |
| 3   | Tabulation          | Bottom-up DP using table or array | iterative, no recursion, build up solution     |

---

## 🌐 Graphs & Trees

| #   | Pattern Name        | How to Identify                                         | Keywords / Triggers                                |
| --- | ------------------- | ------------------------------------------------------- | -------------------------------------------------- |
| 1   | BFS (Breadth First) | Level-wise or shortest path exploration                 | shortest path, level order, queue, minimum moves   |
| 2   | DFS (Depth First)   | Fully explore paths or components recursively           | connected components, traversal, maze, grid        |
| 3   | Union Find (DSU)    | Grouping nodes or detecting cycles in undirected graphs | union, find, disjoint sets, connected, components  |
| 4   | Topological Sort    | Sort tasks based on dependencies (DAGs)                 | prerequisites, dependencies, ordering, build order |

---

## 🧮 Math & Bit Manipulation

| #   | Pattern Name         | How to Identify                                                 | Keywords / Triggers                            |
| --- | -------------------- | --------------------------------------------------------------- | ---------------------------------------------- |
| 1   | Bit Manipulation     | Work with individual bits for toggling, counting, or uniqueness | set bit, power of 2, XOR, AND, odd/even        |
| 2   | Math / Number Theory | Divisibility, primes, GCD/LCM, modular arithmetic               | prime, factors, mod, GCD, LCM, base conversion |

---

## 🔤 Tries (Prefix Trees)

| #   | Pattern Name       | How to Identify                            | Keywords / Triggers                                  |
| --- | ------------------ | ------------------------------------------ | ---------------------------------------------------- |
| 1   | Trie (Prefix Tree) | Efficient search by prefix or autocomplete | starts with, dictionary, autocomplete, prefix search |

---

## 🔁 Multi-Topic / Universal Patterns

| #   | Pattern Name  | Used In                                | Keywords / Triggers                             |
| --- | ------------- | -------------------------------------- | ----------------------------------------------- |
| 1   | Two Pointers  | Arrays, Strings, Linked Lists          | sorted, pair, move inward, overlap              |
| 2   | Greedy        | Arrays, Graphs, Intervals, Scheduling  | maximize/minimize, earliest/latest, profit      |
| 3   | Binary Search | Arrays, Strings, Search Space Problems | sorted, find Kth, minimum/max, left/right bound |
| 4   | Backtracking  | Grids, Strings, Recursion problems     | combinations, permutations, search, constraints |

---


****✅ Tip: If you're stuck on a problem:
- Look for **keywords**
- Identify the **structure** (array, list, graph, etc.)
- Match it with the **right pattern**

