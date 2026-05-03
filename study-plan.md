# 2-Month LeetCode Study Plan for SWE Interviews

---

## How to Identify the Right Algorithm

Before each problem, ask yourself:

1. **What's the input shape?** (array, string, tree, graph, linked list)
2. **What are you optimizing?** (min/max, count, find, check existence)
3. **Are there constraints that hint at O(n) or O(n log n)?**
4. **Does the problem involve subarrays/substrings?** → Sliding Window or Two Pointer
5. **Do you need to track recent history?** → Stack/Queue
6. **Do you need to "remember" previous subproblem results?** → DP
7. **Does the problem involve choices/paths?** → BFS/DFS/Backtracking

---

## WEEK 1 — Arrays (Basics & Two Pointers)

**What you'll learn:** Core array manipulation, in-place operations, and the two-pointer technique.

**General idea:** Arrays are contiguous memory. Two pointers reduces O(n²) brute force to O(n) by moving pointers from ends toward center or in the same direction.

**How to identify Two Pointer:** Problem involves a sorted array, finding a pair/triplet that meets a condition, or reversing/partitioning.

| Day | Focus | Examples |
|-----|-------|---------|
| Mon | Easy arrays | Two Sum, Best Time to Buy/Sell Stock, Contains Duplicate |
| Tue | Easy arrays | Move Zeroes, Merge Sorted Array, Remove Duplicates |
| Wed | Two Pointer (Easy) | Valid Palindrome, Reverse String, Squares of Sorted Array |
| Thu | Two Pointer (Medium) | 3Sum, Container With Most Water |
| Fri | Two Pointer (Medium) | Remove Nth Node, Sort Colors (Dutch flag) |
| Sat | Two Pointer (Hard) | Trapping Rain Water |
| Sun | Review & re-do 2 problems from scratch | — |

---

## WEEK 2 — Sliding Window & Prefix Sum

**What you'll learn:** Efficiently computing subarray/substring sums and finding optimal contiguous windows.

**General idea:** A window of fixed or variable size slides across the array without re-computing the full sum each time. Prefix sum precomputes cumulative totals.

**How to identify Sliding Window:** Keywords like "subarray," "substring," "contiguous," "at most K," "longest/shortest window."

| Day | Focus | Examples |
|-----|-------|---------|
| Mon | Sliding Window Fixed (Easy) | Maximum Average Subarray I |
| Tue | Sliding Window Variable (Easy/Med) | Longest Substring Without Repeating Characters |
| Wed | Sliding Window (Medium) | Minimum Window Substring setup, Fruit Into Baskets |
| Thu | Sliding Window (Medium/Hard) | Minimum Window Substring, Longest Repeating Character Replacement |
| Fri | Prefix Sum (Easy/Med) | Subarray Sum Equals K, Range Sum Query |
| Sat | Mixed review | Sliding Window Maximum (Hard) |
| Sun | Review & re-do 2 problems from scratch | — |

---

## WEEK 3 — Stacks & Queues

**What you'll learn:** LIFO and FIFO structures for tracking history, monotonic properties, and BFS foundations.

**General idea:** Stack = last-in-first-out, great for "most recent." Queue = first-in-first-out, great for "oldest first." Monotonic stack maintains increasing/decreasing order.

**How to identify Stack:** "Next greater element," parentheses matching, evaluating expressions, undo operations, nested structures.  
**How to identify Queue/Deque:** Level-order traversal, sliding window max/min, scheduling.

| Day | Focus | Examples |
|-----|-------|---------|
| Mon | Stack (Easy) | Valid Parentheses, Min Stack, Implement Queue using Stacks |
| Tue | Stack (Medium) | Daily Temperatures, Evaluate Reverse Polish Notation |
| Wed | Monotonic Stack (Medium) | Next Greater Element I & II |
| Thu | Monotonic Stack (Hard) | Largest Rectangle in Histogram |
| Fri | Queue/Deque (Easy/Med) | Implement Stack using Queues, Number of Recent Calls |
| Sat | Deque (Hard) | Sliding Window Maximum |
| Sun | Review & re-do 2 problems from scratch | — |

---

## WEEK 4 — Linked Lists & Hash Maps

**What you'll learn:** Pointer manipulation for linked lists; O(1) lookup with hash maps.

**General idea:** Linked list problems almost always use two pointers (fast/slow). Hash maps trade space for time, reducing O(n²) lookups to O(n).

**How to identify Linked List:** Problem explicitly uses a linked list or asks about cycles, reversal, merging.  
**How to identify Hash Map:** "Find duplicate," "group by," "count frequency," "two sum style" pairing.

| Day | Focus | Examples |
|-----|-------|---------|
| Mon | Linked List (Easy) | Reverse Linked List, Merge Two Sorted Lists, Palindrome Linked List |
| Tue | Linked List (Medium) | Add Two Numbers, Reorder List |
| Wed | Fast/Slow Pointer (Medium) | Linked List Cycle II, Find the Duplicate Number |
| Thu | Linked List (Hard) | Merge K Sorted Lists, Reverse Nodes in K-Group |
| Fri | Hash Map (Easy/Med) | Group Anagrams, Top K Frequent Elements, Valid Anagram |
| Sat | Hash Map (Medium) | Longest Consecutive Sequence, LRU Cache |
| Sun | Review & re-do 2 problems from scratch | — |

---

## WEEK 5 — Trees (BFS & DFS)

**What you'll learn:** Recursive and iterative tree traversals; breadth-first vs depth-first strategies.

**General idea:** DFS goes deep before wide (use recursion or stack). BFS explores level by level (use queue). Most tree problems reduce to: "what do I return up from children?"

**How to identify DFS on trees:** Path problems, check structural properties (balanced, symmetric), compute values at leaves.  
**How to identify BFS on trees:** Level-order output, minimum depth, nodes at distance K.

| Day | Focus | Examples |
|-----|-------|---------|
| Mon | Tree DFS (Easy) | Invert Binary Tree, Max Depth, Same Tree |
| Tue | Tree DFS (Medium) | Path Sum II, Lowest Common Ancestor, Binary Tree Right Side View |
| Wed | Tree BFS (Easy/Med) | Level Order Traversal, Minimum Depth |
| Thu | BST (Medium) | Validate BST, Kth Smallest in BST |
| Fri | Tree (Hard) | Binary Tree Maximum Path Sum, Serialize/Deserialize Binary Tree |
| Sat | Trie (Medium) | Implement Trie, Word Search II |
| Sun | Review & re-do 2 problems from scratch | — |

---

## WEEK 6 — Graphs (BFS, DFS, Union-Find)

**What you'll learn:** Traversals on general graphs, cycle detection, connected components, and shortest paths.

**General idea:** BFS = shortest unweighted path. DFS = exploring all paths, cycle detection. Union-Find = efficiently grouping nodes into connected components.

**How to identify Graph:** Grid problems, "connected components," "can you reach from A to B," "course prerequisites."

| Day | Focus | Examples |
|-----|-------|---------|
| Mon | Graph DFS (Medium) | Number of Islands, Clone Graph, Flood Fill |
| Tue | Graph BFS (Medium) | Rotting Oranges, Word Ladder |
| Wed | Topological Sort (Medium) | Course Schedule I & II |
| Thu | Union-Find (Medium) | Number of Connected Components, Redundant Connection |
| Fri | Shortest Path (Medium/Hard) | Network Delay Time (Dijkstra), Cheapest Flights Within K Stops |
| Sat | Graph (Hard) | Word Ladder II, Alien Dictionary |
| Sun | Review & re-do 2 problems from scratch | — |

---

## WEEK 7 — Dynamic Programming (1D & 2D)

**What you'll learn:** Breaking problems into overlapping subproblems; memoization vs tabulation.

**General idea:** DP = recursion + caching. Ask: "What is the minimum info I need at each step?" then define your state and transition.

**How to identify DP:** "How many ways," "minimum cost," "maximum profit," "can you reach," choices at each step with optimal substructure.

| Day | Focus | Examples |
|-----|-------|---------|
| Mon | 1D DP (Easy/Med) | Climbing Stairs, House Robber, Min Cost Climbing Stairs |
| Tue | 1D DP (Medium) | Coin Change, Jump Game I & II |
| Wed | 1D DP (Medium) | Longest Increasing Subsequence, Word Break |
| Thu | 2D DP (Medium) | Unique Paths, Minimum Path Sum |
| Fri | 2D DP (Medium/Hard) | Longest Common Subsequence, Edit Distance |
| Sat | 2D DP (Hard) | Burst Balloons, Regular Expression Matching |
| Sun | Review & re-do 2 problems from scratch | — |

---

## WEEK 8 — Mixed Review, Heaps, Binary Search & System Design Prep

**What you'll learn:** Heaps for top-K problems; binary search beyond sorted arrays; consolidation of all topics.

**General idea:** Heap = O(log n) insert/delete with O(1) min/max access. Binary search applies wherever the search space is monotonic (not just sorted arrays).

**How to identify Heap:** "Top K," "Kth largest/smallest," "merge K sorted," streaming data.  
**How to identify Binary Search:** "Find in sorted array," "minimum possible maximum," "search rotated array."

| Day | Focus | Examples |
|-----|-------|---------|
| Mon | Heap/Priority Queue (Medium) | Kth Largest Element, Top K Frequent Words, Merge K Sorted Lists |
| Tue | Heap (Hard) | Find Median from Data Stream, Task Scheduler |
| Wed | Binary Search (Easy/Med) | Binary Search, Search in Rotated Array, Find Minimum in Rotated Array |
| Thu | Binary Search (Medium/Hard) | Median of Two Sorted Arrays, Koko Eating Bananas |
| Fri | Backtracking (Medium) | Subsets, Permutations, Combination Sum |
| Sat | Mock Interview | Pick 3 random medium problems under timed conditions (45 min each) |
| Sun | Full mock interview | 2 mediums + 1 hard, with written explanations of approach before coding |

---

## Daily Refresher Habit (15–20 min/day throughout all 8 weeks)

Each morning before your new topic, spend 15–20 minutes on one of these:

- Re-solve yesterday's hardest problem from memory (no peeking)
- Write out the pattern name + recognition cue + time/space complexity
- Review your "mistake log" — a running note of every problem you got wrong and *why*

---

## Pattern Recognition Cheat Sheet

| You see this... | Think... |
|-----------------|----------|
| Sorted array + find pair | Two Pointer |
| Longest/shortest subarray/substring | Sliding Window |
| Nested structures, matching brackets | Stack |
| Level-by-level, shortest path unweighted | BFS |
| All paths, tree/graph exploration | DFS |
| Connected components, grouping | Union-Find |
| "How many ways" / optimal choices | DP |
| Top-K, streaming min/max | Heap |
| "Find in sorted" / minimize max | Binary Search |
| All combinations/permutations | Backtracking |