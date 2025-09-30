# Cheatsheets

_Report Issue_

This article is a collection of cheat sheets you can use while solving problems and prepping for interviews. You’ll find:

- Time complexity (Big-O) cheat sheet
- General DS/A flowchart (when to use each DS/A)
- Stages of an interview cheat sheet

---

## Time Complexity (Big-O) Cheat Sheet

![Time Complexity Big-O Chart — Insert image here](time-complexity.png)

First, the time complexity of common operations (by data structure/algorithm). Then, reasonable complexities given input sizes.

### Arrays (dynamic array/list)
Given `n = arr.length`:
- Add/remove at end: `O(1)` amortized  
- Add/remove at arbitrary index: `O(n)`  
- Access/modify at index: `O(1)`  
- Exists (scan): `O(n)`  
- Two pointers / sliding window: `O(n · k)` where `k` = work per step  
- Build prefix sum: `O(n)`  
- Subarray sum with prefix sum: `O(1)`

### Strings (immutable)
Given `n = s.length`:
- Add/remove char: `O(n)`  
- Access at index: `O(1)`  
- Concatenate two strings: `O(n + m)`  
- Substring create: `O(m)`  
- Two pointers / sliding window: `O(n · k)`  
- Build string (join/builder): `O(n)`

### Linked Lists
Given `n` nodes:
- Add/remove with pointer **before** location: `O(1)`  
- Add/remove with pointer **at** location: `O(1)` if doubly linked  
- Add/remove at position without pointer: `O(n)`  
- Access at position without pointer: `O(n)`  
- Exists (scan): `O(n)`  
- Reverse between `i` and `j`: `O(j − i)`  
- Detect cycle: `O(n)` (fast/slow pointers or hash set)

### Hash Table / Dictionary
Given `n = dict.size`:
- Add/remove key-value: `O(1)`  
- Key exists: `O(1)`  
- Value exists: `O(n)`  
- Access/modify by key: `O(1)`  
- Iterate keys/values/entries: `O(n)`  
> Note: `O(1)` here is wrt `n`. Hashing cost depends on key size (e.g., string key length `m` → hashing `O(m)`).

### Set
Given `n = set.size`:
- Add/remove element: `O(1)`  
- Element exists: `O(1)`  
> Same hashing note applies.

### Stack *(array-backed)*
Given `n = stack.length`:
- Push: `O(1)`  
- Pop: `O(1)`  
- Peek: `O(1)`  
- Random access (array-backed): `O(1)`  
- Exists (scan): `O(n)`

### Queue *(DLL-backed baseline)*
Given `n = queue.length`:
- Enqueue: `O(1)`  
- Dequeue: `O(1)`  
- Peek front: `O(1)`  
- Random access: `O(n)`  
- Exists (scan): `O(n)`  
> Real libs may optimize beyond a simple DLL; details vary.

### Binary Tree (DFS/BFS)
Given `n` nodes:
- Many algorithms: `O(n · k)` where `k` = per-node work (often `O(1)`), assuming efficient queue for BFS.

### Binary Search Tree (BST)
Given `n` nodes:
- Insert/delete: worst `O(n)`, avg `O(log n)`  
- Exists (search): worst `O(n)`, avg `O(log n)`  
> Avg assumes balanced; worst is a chain.

### Heap / Priority Queue (min-heap)
Given `n = heap.length`:
- Insert: `O(log n)`  
- Delete-min: `O(log n)`  
- Find-min: `O(1)`  
- Exists (scan): `O(n)`

### Binary Search
- Worst-case: `O(log n)` over initial search space `n`.

### Miscellaneous
- Sorting: `O(n log n)`  
- Graph DFS/BFS: `O(n · k + e)` where `n` nodes, `e` edges, `k` per-node work (excluding edge iteration)  
- DFS/BFS space: typically `O(n)`; storing graph often `O(n + e)`  
- DP time: `O(n · k)` where `n` = #states, `k` = work/state  
- DP space: `O(n)` states

---

## Input Sizes vs Expected Complexity

- **`n ≤ 10`**  
  Likely factorial/large-base exponential acceptable (e.g., `O(n^2 · n!)`, `O(4^n)`).  
  Think brute force/backtracking.

- **`10 < n ≤ 20`**  
  Likely `O(2^n)`; larger bases/factorials too slow.  
  Subsets/subsequences patterns → backtracking/recursion fine.

- **`20 < n ≤ 100`**  
  Exponentials too slow; up to ~`O(n^3)` can pass.  
  Brute force with nests may pass; then optimize “slow” parts (hash maps/heaps).

- **`100 < n ≤ 1,000`**  
  `O(n^2)` generally acceptable/expected.

- **`1,000 < n ≤ 100,000`** *(very common: `n ≤ 1e5`)*  
  Aim `O(n)` or `O(n log n)`.  
  `O(n^2)` is usually a no-go. Techniques to replace nested loops:
  - Hash map
  - Two pointers / sliding window
  - Monotonic stack
  - Binary search
  - Heap
  - Combos of the above  
  Linear solutions can tolerate moderately large constants (e.g., `26n` in string scans).

- **`100,000 < n ≤ 1,000,000`**  
  Prefer `O(n)`; `O(n log n)` may pass with small constants. Hash maps often required.

- **`n ≥ 1,000,000`** *(sometimes up to `1e9`)*  
  Expect `O(log n)` or `O(1)`; occasionally `O(n)` in special cases.  
  Use binary search/space reduction or constant-time math/hash tricks.

---

## Sorting Algorithms

![Sorting Algorithms — Insert complexities table/diagram here](sorting.png)

All major languages expose a built-in sort; assume `O(n log n)` unless specified. (E.g., Python uses Timsort; C++ std::sort algorithm may vary.)

**Stable sort (Wikipedia):**  
“Stable sorting algorithms maintain the relative order of records with equal keys…”

---

## General DS/A Flowchart

![General DS/A Flowchart — Insert diagram here](dsa-flowchart.png)

This flowchart helps pick a DS/Algo based on problem shape.  
*(Covers LICC methods; excludes more advanced algorithms like Dijkstra’s.)*

---

## Interview Stages Cheat Sheet

A condensed summary of the “Stages of an interview” article.

### 1) Introductions
- 30–60s intro: education, work, interests.  
- Smile, confident voice; listen carefully and reference their intro later.

### 2) Problem Statement
- Paraphrase to confirm.  
- Clarify inputs (types, sortedness, emptiness, invalids) and expected sizes.  
- Walk a quick example.

### 3) Brainstorming DS&A
- Think out loud; consider patterns & tradeoffs.  
- Be receptive to hints; validate approach before coding.

### 4) Implementation
- Explain decisions as you code.  
- Clean, idiomatic, DRY code (helpers/loops).  
- Communicate if stuck; brute-force → optimize.

### 5) Testing & Debugging
- With runtime: write/expand test cases, print internals as needed.  
- Without runtime: manual walkthrough, track variables, compress trivial steps.

### 6) Explanations & Follow-ups
- Time/space (worst-case; mention average if better).  
- Why this DS/Algo/logic?  
- Can it be improved? (Be careful claiming optimal.)

### 7) Outro
- Prepare thoughtful questions (role, team, tech choices).  
- Stay engaged; smile; ask follow-ups.
