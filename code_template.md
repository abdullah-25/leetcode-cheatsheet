# Code Templates

_Report Issue_  

Here are code templates for common patterns for all the data structures and algorithms looked at in LICC.

---

## Two Pointers
- **One input, opposite ends**
- **Two inputs, exhaust both**

---

## Sliding Window

---

## Prefix Sum
- Build a prefix sum

---

## Efficient String Building
In JavaScript, benchmarking shows that concatenation with `+=` is faster than using `.join()`.

---

## Linked List
- Fast and slow pointer
- Reversing a linked list

---

## Subarrays
- Find number of subarrays that fit an exact criteria

---

## Monotonic Structures
- Monotonic increasing stack  
- The same logic can be applied to maintain a monotonic queue.

---

## Binary Tree
- DFS (recursive)
- DFS (iterative)
- BFS

---

## Graph
For the graph templates, assume the nodes are numbered from `0` to `n - 1` and the graph is given as an adjacency list.  
Depending on the problem, you may need to convert the input into an equivalent adjacency list before using the templates.

- DFS (recursive)
- DFS (iterative)
- BFS

---

## Heaps
- Find top k elements with heap

---

## Binary Search
- Basic binary search
- Duplicate elements: left-most insertion point
- Duplicate elements: right-most insertion point
- For greedy problems:
  - If looking for a minimum
  - If looking for a maximum

---

## Backtracking

---

## Dynamic Programming
- **Top-down memoization**

### Converting top-down to bottom-up
1. Initialize an array `dp` sized according to the state variables.  
   Example: input array `nums` and integer `k` (max actions allowed) → `dp` would be 2D: `[nums.length][k]`.

   - Top-down `dp(4,6)` → bottom-up `dp[4][6]`.

2. Set base cases (same as in top-down).  
   Example: `dp(0) = dp(1) = 0` → initialize array values to `0`.

3. Write for-loop(s) over state variables.  
   - Use nested loops for multiple variables.  
   - Start from base cases and end at answer state.

4. Each iteration = one state (equivalent to function call in top-down).  
   - Copy-paste logic from top-down function.  
   - Replace function calls `dp(...)` → array access `dp[...]`.

5. Done!  
   - Return `dp[...]` instead of `dp(...)`.

---

## Trie
- Build a trie

---

## Graph Algorithms
- Dijkstra's algorithm
