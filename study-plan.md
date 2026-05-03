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

---

### Monday — Easy Arrays

- [ ] **Morning Review (20 min):** You're starting fresh — read the *How to Identify the Right Algorithm* section above. Write down in your own words what an array is and why indexing is O(1). Recall the brute-force O(n²) approach to finding a pair.

**Today's Problems:**
- [ ] [Two Sum](https://leetcode.com/problems/two-sum/) *(Easy)* — Hash map to find complement in one pass.
- [ ] [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/) *(Easy)* — Track min price seen so far; update max profit each day.
- [ ] [Contains Duplicate](https://leetcode.com/problems/contains-duplicate/) *(Easy)* — Hash set for O(n) solution.

- [ ] **End of Day Review (20 min):** Write the pattern for each problem solved today. Key takeaway: a **hash map/set** turns O(n²) pair lookups into O(n). Recall how you'd explain the Two Sum solution in an interview. Note any edge cases you missed (empty array, duplicates, negative numbers).

---

### Tuesday — Easy Arrays

- [ ] **Morning Review (20 min):** Re-solve Two Sum from yesterday from memory (no peeking). Write out: input → hash map lookup → output. Note: what happens if there are duplicate values?

**Today's Problems:**
- [ ] [Move Zeroes](https://leetcode.com/problems/move-zeroes/) *(Easy)* — Two pointers: one writes non-zero values, one scans ahead.
- [ ] [Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/) *(Easy)* — Fill from the back to avoid overwriting; three-pointer approach.
- [ ] [Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/) *(Easy)* — Slow pointer marks the next write position.

- [ ] **End of Day Review (20 min):** These three problems all use in-place two-pointer tricks. Write the invariant for each: *"slow always points to the next valid write slot."* Summarize: sorted array + in-place modification → two-pointer write pattern. Check your solutions handle arrays of length 0 and 1.

---

### Wednesday — Two Pointer (Easy)

- [ ] **Morning Review (20 min):** Rewrite Move Zeroes from memory. Then write out the general two-pointer template: `left = 0, right = n-1; while left < right: ...`. Understand when to move each pointer.

**Today's Problems:**
- [ ] [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/) *(Easy)* — Skip non-alphanumeric; compare chars from both ends.
- [ ] [Reverse String](https://leetcode.com/problems/reverse-string/) *(Easy)* — Classic two-pointer swap in-place.
- [ ] [Squares of a Sorted Array](https://leetcode.com/problems/squares-of-a-sorted-array/) *(Easy)* — Two pointers from both ends; fill result from the back.

- [ ] **End of Day Review (20 min):** Recall the two flavors of two pointers: (1) opposite ends converging and (2) same-direction fast/slow. Today was flavor 1. Key insight for Squares: the largest square is always at one of the two ends. Write out the time/space complexity for each problem today.

---

### Thursday — Two Pointer (Medium)

- [ ] **Morning Review (20 min):** Write out the two-pointer template for a sorted array. Recall Valid Palindrome. Then think: how would you extend Two Sum to handle a sorted input? How about finding *three* numbers that sum to zero?

**Today's Problems:**
- [ ] [3Sum](https://leetcode.com/problems/3sum/) *(Medium)* — Sort first, then fix one element and use two pointers on the rest. Skip duplicates carefully.
- [ ] [Container With Most Water](https://leetcode.com/problems/container-with-most-water/) *(Medium)* — Move the shorter wall inward to try to find a taller one.

- [ ] **End of Day Review (20 min):** These are the canonical medium two-pointer problems. For 3Sum, write out *why* you skip duplicates and *where* exactly you do it. For Container: argue *why* moving the shorter side is always safe. These explanations are what interviewers want to hear — practice saying them aloud.

---

### Friday — Two Pointer (Medium)

- [ ] **Morning Review (20 min):** Redo Container With Most Water from scratch (5 min). Then review: what does it mean for an algorithm to be greedy? Two-pointer on Container is a greedy choice — moving the shorter wall is always at least as good as moving the taller one.

**Today's Problems:**
- [ ] [Remove Nth Node From End of List](https://leetcode.com/problems/remove-nth-node-from-end-of-list/) *(Medium)* — Two pointers with an N-step gap; when fast reaches end, slow is at target.
- [ ] [Sort Colors](https://leetcode.com/problems/sort-colors/) *(Medium)* — Dutch National Flag: three pointers `low`, `mid`, `high`.

- [ ] **End of Day Review (20 min):** Dutch Flag is a classic interview problem — write its invariant: *elements < low are 0, elements between low and mid are 1, elements > high are 2.* For Remove Nth: draw the pointer positions on a 5-node list. Understand why a dummy head node simplifies edge cases.

---

### Saturday — Two Pointer (Hard)

- [ ] **Morning Review (20 min):** Write out Sort Colors from memory. Think about the harder version: what if there were 4 colors? Review your time/space complexity notes from the week.

**Today's Problems:**
- [ ] [Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/) *(Hard)* — For each position, water level = `min(maxLeft, maxRight) - height[i]`. Two pointers avoid the O(n) extra arrays.

- [ ] **End of Day Review (20 min):** Trapping Rain Water is one of the most popular hard problems. Write out both solutions: (1) precompute left/right max arrays O(n) space, (2) two-pointer O(1) space. Understand *why* the two-pointer solution works: whichever side has the smaller max is the bottleneck. Make sure you can code both from scratch.

---

### Sunday — Week 1 Review

- [ ] **Morning Review (20 min):** Skim your notes/solutions from Mon–Sat. Identify the 2 problems you found hardest.

**Tasks:**
- [ ] Re-solve your 2 hardest problems from scratch (no looking at previous solution).
- [ ] Write a one-sentence description of the pattern used in each problem this week.
- [ ] Review the *Pattern Recognition Cheat Sheet* at the bottom of this document.

- [ ] **End of Week Review (20 min):** Summarize Week 1 in your own words: *"Arrays are O(1) access. Two pointers reduce brute-force O(n²) to O(n) by maintaining invariants about what each pointer represents. I should reach for two pointers when the array is sorted, or when I need to partition/compare from both ends."* Write any mistakes you made this week into a "mistake log."

---

## WEEK 2 — Sliding Window & Prefix Sum

**What you'll learn:** Efficiently computing subarray/substring sums and finding optimal contiguous windows.

**General idea:** A window of fixed or variable size slides across the array without re-computing the full sum each time. Prefix sum precomputes cumulative totals.

**How to identify Sliding Window:** Keywords like "subarray," "substring," "contiguous," "at most K," "longest/shortest window."

---

### Monday — Sliding Window Fixed (Easy)

- [ ] **Morning Review (20 min):** Recall last week's two-pointer technique. Notice the similarity: a fixed-size window is just two pointers exactly `k` apart. Write out: *"Instead of recomputing the sum from scratch, I add the new element entering the window and subtract the one leaving."*

**Today's Problems:**
- [ ] [Maximum Average Subarray I](https://leetcode.com/problems/maximum-average-subarray-i/) *(Easy)* — Maintain a running sum; slide the window one step at a time.

- [ ] **End of Day Review (20 min):** Key pattern: **fixed window = add right, remove left.** Write out the template: `windowSum += nums[i]; if i >= k: windowSum -= nums[i - k]; if i >= k - 1: update answer`. Understand why this is O(n) instead of O(n·k).

---

### Tuesday — Sliding Window Variable (Easy/Medium)

- [ ] **Morning Review (20 min):** Rewrite Maximum Average Subarray I from memory. Then think: what if the window size isn't fixed but depends on a condition? How would you know when to shrink the window?

**Today's Problems:**
- [ ] [Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/) *(Medium)* — Expand right; when a duplicate enters, shrink from the left until no duplicate.

- [ ] **End of Day Review (20 min):** Variable window template: `expand right always; shrink left when constraint is violated; update answer when valid.` Write it out. Key data structure: a hash map (char → last index) or a set. Make sure you handle the edge case where the duplicate is outside the current window.

---

### Wednesday — Sliding Window (Medium)

- [ ] **Morning Review (20 min):** Write the variable sliding window template from memory. Then think about the "at most K distinct elements" pattern — how does that differ from "no duplicates"?

**Today's Problems:**
- [ ] [Fruit Into Baskets](https://leetcode.com/problems/fruit-into-baskets/) *(Medium)* — At most 2 distinct values in window; use a frequency map to track counts and shrink when `len(map) > 2`.
- [ ] [Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/) *(Hard — attempt setup only today)* — Read the problem and write a plan: what does "valid window" mean? What counts do you need to track?

- [ ] **End of Day Review (20 min):** Fruit Into Baskets is "at most K distinct" — a very common interview variant. Write: *"Sliding window with a frequency map: expand right, add to map. If map grows beyond K, shrink from left and remove from map when count hits 0."* For Minimum Window, write your plan before coding tomorrow.

---

### Thursday — Sliding Window (Medium/Hard)

- [ ] **Morning Review (20 min):** Re-read your Minimum Window plan from yesterday. Recall the two-pointer/sliding window template. Think about what "have" vs "need" means in the context of character frequencies.

**Today's Problems:**
- [ ] [Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/) *(Hard)* — Track `need` (frequency of chars in `t`) and `have` (how many chars currently satisfied). Shrink window when all chars are covered.
- [ ] [Longest Repeating Character Replacement](https://leetcode.com/problems/longest-repeating-character-replacement/) *(Medium)* — Key insight: `windowLen - maxFreq <= k` means the window is valid (replace everything that isn't the most frequent char).

- [ ] **End of Day Review (20 min):** Both are classic medium/hard slider problems. For Minimum Window, write out what `have` and `need` track and when you update them. For Character Replacement, write *why* `windowLen - maxFreq` is the number of replacements needed. These explanations matter more than the code in interviews.

---

### Friday — Prefix Sum (Easy/Medium)

- [ ] **Morning Review (20 min):** Recall the sliding window pattern. Now think about a different approach: what if you precompute `prefix[i] = sum of first i elements`? Then `sum(l, r) = prefix[r+1] - prefix[l]` in O(1). Write that formula.

**Today's Problems:**
- [ ] [Range Sum Query - Immutable](https://leetcode.com/problems/range-sum-query-immutable/) *(Easy)* — Build `prefix` array in constructor; answer each query in O(1).
- [ ] [Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/) *(Medium)* — `prefix[j] - prefix[i] == k` → look for `prefix[j] - k` in a hash map of previously seen prefix sums.

- [ ] **End of Day Review (20 min):** Prefix sum is a foundational technique. Write: *"prefix[i] = nums[0] + ... + nums[i-1]. sum(l,r) = prefix[r+1] - prefix[l]."* For Subarray Sum Equals K, make sure you understand why a hash map is needed and why you initialize `{0: 1}`. This is a very common interview problem.

---

### Saturday — Hard Sliding Window

- [ ] **Morning Review (20 min):** Write the sliding window template and the prefix sum formula from memory. Review Subarray Sum Equals K — make sure you can explain the hash map approach without looking.

**Today's Problems:**
- [ ] [Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/) *(Hard)* — Use a **monotonic deque**: maintain indices in decreasing order of their values. The front of the deque is always the max of the current window.

- [ ] **End of Day Review (20 min):** This problem combines sliding window + deque (monotonic). Write the invariant: *"deque stores indices in decreasing value order; values smaller than the new element are popped from the back (they can never be the max); indices outside the window are popped from the front."* This is a very common hard problem — make sure you can reproduce it from the invariant alone.

---

### Sunday — Week 2 Review

- [ ] **Morning Review (20 min):** Skim your Week 2 solutions. Pick the 2 you found hardest.

**Tasks:**
- [ ] Re-solve your 2 hardest Week 2 problems from scratch.
- [ ] Write the sliding window template (fixed and variable) and the prefix sum formula in your notes.
- [ ] Add any bugs or edge cases you missed to your mistake log.

- [ ] **End of Week Review (20 min):** *"Sliding window avoids redundant recomputation by maintaining a running state. Fixed window: add right, subtract left. Variable window: expand right, shrink left when invalid. Prefix sum turns range-sum queries from O(n) to O(1) at the cost of O(n) preprocessing. Monotonic deque extends sliding window to handle range max/min in O(n) total."*

---

## WEEK 3 — Stacks & Queues

**What you'll learn:** LIFO and FIFO structures for tracking history, monotonic properties, and BFS foundations.

**General idea:** Stack = last-in-first-out, great for "most recent." Queue = first-in-first-out, great for "oldest first." Monotonic stack maintains increasing/decreasing order.

**How to identify Stack:** "Next greater element," parentheses matching, evaluating expressions, undo operations, nested structures.  
**How to identify Queue/Deque:** Level-order traversal, sliding window max/min, scheduling.

---

### Monday — Stack (Easy)

- [ ] **Morning Review (20 min):** Recall last week's monotonic deque. Write out the difference between a stack (LIFO) and a queue (FIFO). Think: when is "most recent item" useful? (undo, matching brackets, backtracking). Write the Python/JS stack operations: push (append), pop, peek (stack[-1]).

**Today's Problems:**
- [ ] [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/) *(Easy)* — Push open brackets; when a close bracket appears, check top of stack matches.
- [ ] [Min Stack](https://leetcode.com/problems/min-stack/) *(Medium)* — Maintain a second stack that tracks the current minimum at each level.
- [ ] [Implement Queue using Stacks](https://leetcode.com/problems/implement-queue-using-stacks/) *(Easy)* — Two stacks: one for push, one for pop. Move all elements lazily.

- [ ] **End of Day Review (20 min):** Key insight for Valid Parentheses: the stack stores "what I'm waiting to close." For Min Stack: the auxiliary min-stack stores the minimum *as of each push*, not globally. For Queue with Stacks: amortized O(1) — explain *why* each element crosses from stack1 to stack2 at most once.

---

### Tuesday — Stack (Medium)

- [ ] **Morning Review (20 min):** Re-solve Valid Parentheses from memory. Think about what "monotonic" means: a monotonic increasing stack pops whenever a smaller element arrives. Why is this useful for "next greater element" style problems?

**Today's Problems:**
- [ ] [Daily Temperatures](https://leetcode.com/problems/daily-temperatures/) *(Medium)* — Monotonic decreasing stack of indices; pop when a warmer day arrives.
- [ ] [Evaluate Reverse Polish Notation](https://leetcode.com/problems/evaluate-reverse-polish-notation/) *(Medium)* — Push numbers; when an operator appears, pop two, compute, push result.

- [ ] **End of Day Review (20 min):** Daily Temperatures is the canonical monotonic stack problem. Write the invariant: *"stack always contains indices of temperatures waiting for a warmer day, in decreasing order."* For RPN: the stack is acting as an implicit expression tree. Trace through `["2","1","+","3","*"]` by hand to solidify.

---

### Wednesday — Monotonic Stack (Medium)

- [ ] **Morning Review (20 min):** Re-write Daily Temperatures from memory. State the monotonic stack invariant: *"when processing element i, pop all indices j where nums[j] < nums[i] — those have found their answer."*

**Today's Problems:**
- [ ] [Next Greater Element I](https://leetcode.com/problems/next-greater-element-i/) *(Easy)* — Process `nums2` with a monotonic stack to build a map of next-greater; then look up each element of `nums1`.
- [ ] [Next Greater Element II](https://leetcode.com/problems/next-greater-element-ii/) *(Medium)* — Circular array: loop twice (use `i % n`). Same monotonic stack approach.

- [ ] **End of Day Review (20 min):** Both problems are variations on the same pattern. Key for circular: iterating `2n` times with `i % n` elegantly handles wrap-around. Write out why you don't need to actually duplicate the array. Complexity: O(n) time, O(n) space for stack + result.

---

### Thursday — Monotonic Stack (Hard)

- [ ] **Morning Review (20 min):** Re-read your notes on the monotonic stack invariant. Now think: could you apply it to 2D? In a histogram, each bar's "width" is how far left and right it can extend — sounds like "previous smaller" and "next smaller" elements.

**Today's Problems:**
- [ ] [Largest Rectangle in Histogram](https://leetcode.com/problems/largest-rectangle-in-histogram/) *(Hard)* — Monotonic increasing stack. When a shorter bar is found, pop and compute the rectangle with the popped bar as the shortest.

- [ ] **End of Day Review (20 min):** This is considered one of the hardest stack problems. Write out the approach: *"maintain a stack of indices with increasing heights. When heights[i] < heights[stack.top()], the popped bar is the height; the width is from current i to the new top of stack."* Trace through `[2,1,5,6,2,3]` by hand. Then try: how does this relate to Trapping Rain Water?

---

### Friday — Queue/Deque (Easy/Medium)

- [ ] **Morning Review (20 min):** Recall last week's Sliding Window Maximum (monotonic deque). Write the difference: a monotonic *stack* is LIFO; a monotonic *deque* allows popping from both ends. Write out the queue operations: enqueue (append right), dequeue (pop left).

**Today's Problems:**
- [ ] [Implement Stack using Queues](https://leetcode.com/problems/implement-stack-using-queues/) *(Easy)* — Re-queue all but the last element on each pop, or maintain a "rotate" approach.
- [ ] [Number of Recent Calls](https://leetcode.com/problems/number-of-recent-calls/) *(Easy)* — Use a deque/queue; dequeue calls older than `t - 3000`.

- [ ] **End of Day Review (20 min):** These cement the conceptual difference between stacks and queues. For Number of Recent Calls: the queue naturally maintains calls in time order, and you just evict the outdated ones from the front — O(1) amortized. Think about how a deque generalizes both.

---

### Saturday — Deque (Hard)

- [ ] **Morning Review (20 min):** Review Week 2's Sliding Window Maximum (you solved this then). Now re-examine it through the lens of the monotonic deque — the deque stores candidates for the max.

**Today's Problems:**
- [ ] [Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/) *(Hard)* — Revisit with deeper understanding: write out the invariant and trace through `[1,3,-1,-3,5,3,6,7]` with `k=3`.

- [ ] **End of Day Review (20 min):** After two exposures to this problem, you should be able to code it cold. Write out the complete solution from the invariant. Confirm O(n) time — each element enters and leaves the deque at most once. This problem links Week 2 (sliding window) to Week 3 (deque) — note that connection.

---

### Sunday — Week 3 Review

- [ ] **Morning Review (20 min):** Skim Week 3 solutions. Identify 2 hardest.

**Tasks:**
- [ ] Re-solve Largest Rectangle in Histogram and one other hard problem from scratch.
- [ ] Write the monotonic stack invariant in one sentence.
- [ ] Add mistakes to your log.

- [ ] **End of Week Review (20 min):** *"Stack = LIFO; great for matching/nesting problems and 'next greater/smaller' patterns. Monotonic stack processes each element in O(1) amortized by ensuring the stack is always sorted. Queue = FIFO; great for level-order traversal and time-window problems. Deque = double-ended; combines both and enables O(n) sliding window max/min."*

---

## WEEK 4 — Linked Lists & Hash Maps

**What you'll learn:** Pointer manipulation for linked lists; O(1) lookup with hash maps.

**General idea:** Linked list problems almost always use two pointers (fast/slow). Hash maps trade space for time, reducing O(n²) lookups to O(n).

**How to identify Linked List:** Problem explicitly uses a linked list or asks about cycles, reversal, merging.  
**How to identify Hash Map:** "Find duplicate," "group by," "count frequency," "two sum style" pairing.

---

### Monday — Linked List (Easy)

- [ ] **Morning Review (20 min):** Draw a singly linked list on paper. Write the node definition. Practice: given a head pointer, how do you traverse? How do you reverse? The key mental model: *you need to save `node.next` before you overwrite it.*

**Today's Problems:**
- [ ] [Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/) *(Easy)* — Iterative: `prev`, `curr`, `next`. Recursive: return the new head from the base case.
- [ ] [Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/) *(Easy)* — Dummy head simplifies edge cases; compare and advance the smaller pointer.
- [ ] [Palindrome Linked List](https://leetcode.com/problems/palindrome-linked-list/) *(Easy)* — Find midpoint (fast/slow), reverse the second half, compare.

- [ ] **End of Day Review (20 min):** Write Reverse Linked List from memory — both iterative and recursive. For Palindrome: trace through a 5-node list showing where `slow` and `fast` end up. The dummy head pattern: *always use a dummy node when you might need to insert before the current head.*

---

### Tuesday — Linked List (Medium)

- [ ] **Morning Review (20 min):** Re-write Reverse Linked List iteratively from memory. Think: what if you needed to reverse only a portion of the list? That's what *Reverse Nodes in K-Group* will require on Thursday.

**Today's Problems:**
- [ ] [Add Two Numbers](https://leetcode.com/problems/add-two-numbers/) *(Medium)* — Simulate grade-school addition; carry = `sum // 10`, digit = `sum % 10`.
- [ ] [Reorder List](https://leetcode.com/problems/reorder-list/) *(Medium)* — Three steps: (1) find midpoint, (2) reverse second half, (3) merge the two halves.

- [ ] **End of Day Review (20 min):** Reorder List is an excellent combo problem that uses find-midpoint + reverse + merge — all three basic linked list operations. Write the three-step breakdown. For Add Two Numbers: handle the carry after the loop ends (there may be one more digit).

---

### Wednesday — Fast/Slow Pointer (Medium)

- [ ] **Morning Review (20 min):** Recall the fast/slow pointer trick for finding midpoints. Now think: if the list has a cycle, `fast` will lap `slow`. Draw a cycle and show why `fast` and `slow` must meet inside the loop.

**Today's Problems:**
- [ ] [Linked List Cycle II](https://leetcode.com/problems/linked-list-cycle-ii/) *(Medium)* — Detect cycle (fast/slow meet); then to find cycle start: reset one pointer to head, advance both one step at a time until they meet.
- [ ] [Find the Duplicate Number](https://leetcode.com/problems/find-the-duplicate-number/) *(Medium)* — Treat the array as a linked list (`i → nums[i]`); apply Floyd's cycle detection.

- [ ] **End of Day Review (20 min):** Floyd's cycle detection is a classic algorithm. Write out *why* resetting one pointer to head finds the cycle entry (mathematical proof: if they meet at distance `d` into the cycle, the head is also distance `d` from the cycle entry). Find the Duplicate is a clever reduction — write the mapping `index → nums[index]` for a small example.

---

### Thursday — Linked List (Hard)

- [ ] **Morning Review (20 min):** Re-solve Linked List Cycle II from memory. Then review Reverse Linked List once more — you'll need to reverse sub-lists today.

**Today's Problems:**
- [ ] [Merge K Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/) *(Hard)* — Use a min-heap of `(val, listIndex)` pairs. Pop min, advance that list, push next node.
- [ ] [Reverse Nodes in K-Group](https://leetcode.com/problems/reverse-nodes-in-k-group/) *(Hard)* — Check k nodes exist, reverse them, recursively handle the rest, re-link.

- [ ] **End of Day Review (20 min):** These are two of the most common hard linked list problems. For Merge K Sorted Lists: complexity is O(n log k) — explain why (each of n total nodes is inserted into a heap of size k). For K-Group: trace through a 6-node list with k=2 to confirm the re-linking. Make sure you handle the case where fewer than k nodes remain.

---

### Friday — Hash Map (Easy/Medium)

- [ ] **Morning Review (20 min):** Recall week 1's Two Sum (hash map for O(n) pairing). Generalize: hash map = trade O(n) space for O(1) average lookup. Write the three use cases: (1) count frequency, (2) group by key, (3) check existence/complement.

**Today's Problems:**
- [ ] [Valid Anagram](https://leetcode.com/problems/valid-anagram/) *(Easy)* — Count char frequencies in both strings; compare maps (or use one map: increment for s, decrement for t).
- [ ] [Group Anagrams](https://leetcode.com/problems/group-anagrams/) *(Medium)* — Key = sorted word (or frequency tuple); group words with the same key.
- [ ] [Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/) *(Medium)* — Count frequencies; use a heap of size k (or bucket sort by frequency for O(n)).

- [ ] **End of Day Review (20 min):** These three problems illustrate the "count → group → rank" pipeline. For Top K: know both approaches — heap is O(n log k), bucket sort is O(n). Be ready to explain the trade-offs. For Group Anagrams: a sorted string as a key is O(m log m) per word where m = word length. Can you do O(m)?

---

### Saturday — Hash Map (Medium/Hard)

- [ ] **Morning Review (20 min):** Review Group Anagrams. Think about what other things can serve as a hash map key: coordinates, character counts (as tuples), sorted lists, etc. Recall that `defaultdict` and `Counter` (Python) simplify frequency maps.

**Today's Problems:**
- [ ] [Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/) *(Medium)* — Add all numbers to a set. Only start counting from numbers with no left neighbor (`n-1` not in set). Count forward.
- [ ] [LRU Cache](https://leetcode.com/problems/lru-cache/) *(Medium)* — Hash map + doubly linked list. Map stores `key → node`; DLL maintains access order.

- [ ] **End of Day Review (20 min):** Longest Consecutive: the "only start from the leftmost" trick gives O(n) — explain why each number is visited at most twice. For LRU Cache: this is a design question. Write out the four operations: get (move to front), put (add to front, evict tail if over capacity). Understand why you need a doubly linked list (O(1) removal).

---

### Sunday — Week 4 Review

- [ ] **Morning Review (20 min):** Skim Week 4. Identify 2 hardest problems.

**Tasks:**
- [ ] Re-solve LRU Cache and one other problem from scratch.
- [ ] Write in one sentence: how does the fast/slow pointer detect a cycle, and how does it find the cycle start?
- [ ] Add mistakes to your log.

- [ ] **End of Week Review (20 min):** *"Linked lists require careful pointer management — always save next before overwriting. Fast/slow pointers detect cycles and find midpoints. Hash maps reduce O(n²) to O(n) by trading space for lookup time. LRU Cache combines a hash map and a doubly linked list to achieve O(1) get and put — a classic design problem."*

---

## WEEK 5 — Trees (BFS & DFS)

**What you'll learn:** Recursive and iterative tree traversals; breadth-first vs depth-first strategies.

**General idea:** DFS goes deep before wide (use recursion or stack). BFS explores level by level (use queue). Most tree problems reduce to: "what do I return up from children?"

**How to identify DFS on trees:** Path problems, check structural properties (balanced, symmetric), compute values at leaves.  
**How to identify BFS on trees:** Level-order output, minimum depth, nodes at distance K.

---

### Monday — Tree DFS (Easy)

- [ ] **Morning Review (20 min):** Draw a binary tree. Write the recursive DFS template: `def dfs(node): if not node: return base_case; left = dfs(node.left); right = dfs(node.right); return combine(left, right, node.val)`. Write the three traversal orders (pre, in, post) and what each is useful for.

**Today's Problems:**
- [ ] [Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree/) *(Easy)* — At every node: swap left and right children, then recurse.
- [ ] [Maximum Depth of Binary Tree](https://leetcode.com/problems/maximum-depth-of-binary-tree/) *(Easy)* — Return `1 + max(dfs(left), dfs(right))`.
- [ ] [Same Tree](https://leetcode.com/problems/same-tree/) *(Easy)* — Both null → True; one null → False; values differ → False; else recurse both sides.

- [ ] **End of Day Review (20 min):** All three use the same DFS template — the only difference is what you "combine" at each node. Write all three solutions from the template. Key: the base case (null node) is the most important line. Make sure you handle null before accessing `.val`.

---

### Tuesday — Tree DFS (Medium)

- [ ] **Morning Review (20 min):** Re-write Maximum Depth from memory. Now think: what if you need to track the *path* from root to leaf, not just a single value? That means you need to pass information *down* (via parameters) not just return it up.

**Today's Problems:**
- [ ] [Path Sum II](https://leetcode.com/problems/path-sum-ii/) *(Medium)* — Pass current path and remaining target down; add to results when you reach a leaf with target == 0.
- [ ] [Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/) *(Medium)* — If current node is p or q, return it. LCA is the first node where both subtrees return non-null.
- [ ] [Binary Tree Right Side View](https://leetcode.com/problems/binary-tree-right-side-view/) *(Medium)* — DFS with depth tracking; the last node visited at each depth (right before left) is the right-side view.

- [ ] **End of Day Review (20 min):** These introduce two important DFS patterns: (1) pass-down (accumulate path) and (2) post-order decision (LCA). For Right Side View: compare DFS and BFS approaches — BFS is arguably cleaner here. Write both.

---

### Wednesday — Tree BFS (Easy/Medium)

- [ ] **Morning Review (20 min):** Write the BFS template: `queue = deque([root]); while queue: node = queue.popleft(); process(node); if node.left: queue.append(node.left); if node.right: queue.append(node.right)`. How do you track levels? (snapshot queue size at start of each level)

**Today's Problems:**
- [ ] [Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/) *(Medium)* — Use queue; for each level, snapshot size, process that many nodes, collect children.
- [ ] [Minimum Depth of Binary Tree](https://leetcode.com/problems/minimum-depth-of-binary-tree/) *(Easy)* — BFS is naturally optimal for minimum depth (first leaf found is the shallowest).

- [ ] **End of Day Review (20 min):** Level Order is the canonical BFS tree problem. The "snapshot queue size" trick for tracking levels is critical — write it out. For Minimum Depth: why is BFS better than DFS here? (BFS stops at the first leaf; DFS must explore all paths before knowing the minimum.)

---

### Thursday — BST (Medium)

- [ ] **Morning Review (20 min):** Recall BST property: `left.val < node.val < right.val` for all nodes. In-order traversal of a BST gives sorted output. Write: to validate a BST, pass min/max bounds down instead of comparing just with parent.

**Today's Problems:**
- [ ] [Validate Binary Search Tree](https://leetcode.com/problems/validate-binary-search-tree/) *(Medium)* — DFS with min/max bounds: `dfs(node, min_val, max_val)`. Update bounds when going left/right.
- [ ] [Kth Smallest Element in a BST](https://leetcode.com/problems/kth-smallest-element-in-a-bst/) *(Medium)* — In-order traversal (iterative or recursive with counter); the kth element visited is the answer.

- [ ] **End of Day Review (20 min):** For Validate BST: the classic mistake is only comparing with the parent. Write why that's wrong with an example. Bounds propagation is the correct approach. For Kth Smallest: understand why in-order gives sorted order — it's the definition of a BST.

---

### Friday — Tree (Hard)

- [ ] **Morning Review (20 min):** Review LCA from Tuesday — you'll use similar "return up" logic for Max Path Sum. Think: at each node, the max path through it is `node.val + max(0, leftGain) + max(0, rightGain)`. But you can only use one side when returning up.

**Today's Problems:**
- [ ] [Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/) *(Hard)* — At each node: update global max with `val + leftGain + rightGain`; return `val + max(leftGain, rightGain)` to parent.
- [ ] [Serialize and Deserialize Binary Tree](https://leetcode.com/problems/serialize-and-deserialize-binary-tree/) *(Hard)* — Pre-order traversal with null markers for serialize; reconstruct with a queue/index during deserialize.

- [ ] **End of Day Review (20 min):** Max Path Sum: write out the distinction between the "path through this node" (used to update global max) and the "gain returned to parent" (single arm only). Serialize/Deserialize: trace through a small tree. Understand why pre-order + null markers uniquely identifies any binary tree.

---

### Saturday — Trie (Medium)

- [ ] **Morning Review (20 min):** A Trie is a tree where each node represents a character, and paths from root to marked nodes form valid words. Write the TrieNode structure: `children = {}` (or array of 26), `is_end = False`.

**Today's Problems:**
- [ ] [Implement Trie (Prefix Tree)](https://leetcode.com/problems/implement-trie-prefix-tree/) *(Medium)* — Insert: follow/create nodes for each char. Search: follow nodes, check `is_end`. StartsWith: same but don't check `is_end`.
- [ ] [Word Search II](https://leetcode.com/problems/word-search-ii/) *(Hard)* — Build a Trie of all words; DFS from each cell on the board; prune when the current path isn't a Trie prefix.

- [ ] **End of Day Review (20 min):** Trie is used for efficient prefix queries. For Word Search II: understand why building a Trie is better than searching for each word separately — you can prune the DFS early and share work across words. Write the DFS with backtracking (mark cell as visited, recurse neighbors, unmark).

---

### Sunday — Week 5 Review

- [ ] **Morning Review (20 min):** Skim Week 5. Pick 2 hardest problems.

**Tasks:**
- [ ] Re-solve Binary Tree Maximum Path Sum and one other hard problem from scratch.
- [ ] Write the DFS template and the BFS template from memory.
- [ ] Add mistakes to your log.

- [ ] **End of Week Review (20 min):** *"DFS on trees = recursive post-order: compute left, compute right, combine at current node. BFS = queue with level-size snapshot for level-order. BST adds the sorted property — in-order gives sorted output; validation needs min/max bounds. Trie = prefix tree for efficient word lookups. Most tree problems ask: what do I return from children, and how do I combine it at the parent?"*

---

## WEEK 6 — Graphs (BFS, DFS, Union-Find)

**What you'll learn:** Traversals on general graphs, cycle detection, connected components, and shortest paths.

**General idea:** BFS = shortest unweighted path. DFS = exploring all paths, cycle detection. Union-Find = efficiently grouping nodes into connected components.

**How to identify Graph:** Grid problems, "connected components," "can you reach from A to B," "course prerequisites."

---

### Monday — Graph DFS (Medium)

- [ ] **Morning Review (20 min):** Recall tree DFS. Graphs add one wrinkle: cycles. Write the graph DFS template with a `visited` set: `def dfs(node): visited.add(node); for neighbor in graph[node]: if neighbor not in visited: dfs(neighbor)`. Draw a 4-node graph and trace DFS.

**Today's Problems:**
- [ ] [Number of Islands](https://leetcode.com/problems/number-of-islands/) *(Medium)* — For each unvisited '1', run DFS to mark the entire island as visited. Count DFS calls.
- [ ] [Clone Graph](https://leetcode.com/problems/clone-graph/) *(Medium)* — DFS with a `visited` map `{original → clone}`. Create clone before recursing to handle cycles.
- [ ] [Flood Fill](https://leetcode.com/problems/flood-fill/) *(Easy)* — DFS from source cell; change color of all connected cells with the original color.

- [ ] **End of Day Review (20 min):** Number of Islands is the canonical graph DFS problem on a grid. Write the 4-directional neighbor loop: `for dr, dc in [(0,1),(0,-1),(1,0),(-1,0)]`. For Clone Graph: the visited map doubles as the clone registry — explain why you add to it *before* recursing. Flood Fill: trace through a 3×3 grid.

---

### Tuesday — Graph BFS (Medium)

- [ ] **Morning Review (20 min):** Recall BFS on trees (queue). On a graph, BFS gives the **shortest path** in unweighted graphs. Write the template: start with all sources in queue, track `dist` or `steps`, expand neighbors not yet visited.

**Today's Problems:**
- [ ] [Rotting Oranges](https://leetcode.com/problems/rotting-oranges/) *(Medium)* — Multi-source BFS: start with all rotten oranges; spread to fresh neighbors each step. Answer is total steps.
- [ ] [Word Ladder](https://leetcode.com/problems/word-ladder/) *(Hard)* — BFS where each node is a word, edges connect words differing by one letter. Generate all 1-letter mutations and check against wordList set.

- [ ] **End of Day Review (20 min):** Multi-source BFS (Rotting Oranges) starts from multiple nodes simultaneously — equivalent to a single virtual source connected to all of them. For Word Ladder: the key optimization is checking against a set (`O(1)` lookup) and removing words from the set as they're visited (prevents revisiting). BFS guarantees the first time a word is reached is the shortest path.

---

### Wednesday — Topological Sort (Medium)

- [ ] **Morning Review (20 min):** A directed acyclic graph (DAG) has no cycles. Topological sort = linear ordering where every edge goes from earlier to later. Write Kahn's algorithm: in-degree array + queue of nodes with in-degree 0.

**Today's Problems:**
- [ ] [Course Schedule](https://leetcode.com/problems/course-schedule/) *(Medium)* — Build adjacency list and in-degree array. BFS (Kahn's): if all nodes are processed, no cycle exists.
- [ ] [Course Schedule II](https://leetcode.com/problems/course-schedule-ii/) *(Medium)* — Same as above, but collect the processing order as the result.

- [ ] **End of Day Review (20 min):** Topological sort is essential for dependency graphs. Write Kahn's algorithm from scratch. Also know the DFS-based approach: mark nodes as `visiting` (in current path) and `visited` (done). If you reach a `visiting` node, there's a cycle. Compare the two approaches — when is each cleaner?

---

### Thursday — Union-Find (Medium)

- [ ] **Morning Review (20 min):** Union-Find (Disjoint Set Union) maintains a collection of disjoint sets. Write the two operations: `find(x)` (returns root of x's component, with path compression) and `union(x, y)` (merges components, using rank to keep tree flat).

**Today's Problems:**
- [ ] [Number of Connected Components in an Undirected Graph](https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/) *(Medium)* — Initialize n components; for each edge, union the two nodes; if they were in different components, decrement count.
- [ ] [Redundant Connection](https://leetcode.com/problems/redundant-connection/) *(Medium)* — Process edges one by one; the first edge where both nodes are already in the same component creates a cycle — that's the redundant edge.

- [ ] **End of Day Review (20 min):** Write Union-Find with path compression and union by rank — this gives near O(1) amortized per operation. For Redundant Connection: the insight is elegant — process edges in order and detect when `find(u) == find(v)`. Write the complete Union-Find class from memory (it's short and high-value in interviews).

---

### Friday — Shortest Path (Medium/Hard)

- [ ] **Morning Review (20 min):** Recall BFS gives shortest path for unweighted graphs. For weighted graphs, use **Dijkstra's**: a greedy algorithm using a min-heap. Write: `heap = [(dist, node)]`; pop min-dist node, relax neighbors, push updated distances.

**Today's Problems:**
- [ ] [Network Delay Time](https://leetcode.com/problems/network-delay-time/) *(Medium)* — Dijkstra from source node; answer is max distance across all reachable nodes.
- [ ] [Cheapest Flights Within K Stops](https://leetcode.com/problems/cheapest-flights-within-k-stops/) *(Medium)* — Modified Dijkstra or Bellman-Ford with a constraint on number of hops. State = `(cost, node, stops_remaining)`.

- [ ] **End of Day Review (20 min):** Dijkstra's key insight: always process the globally cheapest node next (greedy). For K Stops: standard Dijkstra doesn't directly handle hop limits. Understand why `(cost, node, stops)` works as state. Compare Dijkstra (O((V+E) log V)) vs Bellman-Ford (O(V·E)) — when would you use each?

---

### Saturday — Graph (Hard)

- [ ] **Morning Review (20 min):** Review BFS (Word Ladder), Topological Sort (Course Schedule), and Dijkstra. Think: what would a bidirectional BFS look like for Word Ladder? It searches from both source and target simultaneously, reducing search space from O(b^d) to O(b^(d/2)).

**Today's Problems:**
- [ ] [Word Ladder II](https://leetcode.com/problems/word-ladder-ii/) *(Hard)* — BFS to find shortest distance to each word, then DFS/backtrack to reconstruct all shortest paths.
- [ ] [Alien Dictionary](https://leetcode.com/problems/alien-dictionary/) *(Hard)* — Compare adjacent words to extract edge constraints; topological sort to find valid character ordering; detect cycles (invalid input).

- [ ] **End of Day Review (20 min):** Word Ladder II is notoriously hard — the trick is separating BFS (to find shortest distance) from DFS (to reconstruct paths). For Alien Dictionary: the derivation of edges from comparing adjacent words is the tricky part. Write: *"Compare word[i] and word[i+1] char by char; the first differing position gives an edge `c1 → c2`."*

---

### Sunday — Week 6 Review

- [ ] **Morning Review (20 min):** Skim Week 6. Pick 2 hardest.

**Tasks:**
- [ ] Re-solve Union-Find (write the class from memory) and one other problem.
- [ ] Write the four graph algorithms: DFS, BFS, Topological Sort, Dijkstra — when to use each.
- [ ] Add mistakes to your log.

- [ ] **End of Week Review (20 min):** *"Graph DFS: explore all paths, detect cycles (use `visited` set). Graph BFS: shortest unweighted path (queue + distance tracking). Topological sort: process DAG in dependency order (Kahn's = BFS with in-degree; DFS with 3 colors). Union-Find: O(α(n)) amortized operations for connected components. Dijkstra: shortest weighted path with min-heap."*

---

## WEEK 7 — Dynamic Programming (1D & 2D)

**What you'll learn:** Breaking problems into overlapping subproblems; memoization vs tabulation.

**General idea:** DP = recursion + caching. Ask: "What is the minimum info I need at each step?" then define your state and transition.

**How to identify DP:** "How many ways," "minimum cost," "maximum profit," "can you reach," choices at each step with optimal substructure.

---

### Monday — 1D DP (Easy/Medium)

- [ ] **Morning Review (20 min):** Write the DP process: (1) define the state `dp[i]` = answer to subproblem ending at/using i, (2) write the recurrence (transition), (3) initialize base cases, (4) fill in order. Start with Fibonacci as a warm-up: `dp[i] = dp[i-1] + dp[i-2]`.

**Today's Problems:**
- [ ] [Climbing Stairs](https://leetcode.com/problems/climbing-stairs/) *(Easy)* — `dp[i] = dp[i-1] + dp[i-2]`. Identical to Fibonacci.
- [ ] [Min Cost Climbing Stairs](https://leetcode.com/problems/min-cost-climbing-stairs/) *(Easy)* — `dp[i] = cost[i] + min(dp[i-1], dp[i-2])`.
- [ ] [House Robber](https://leetcode.com/problems/house-robber/) *(Medium)* — `dp[i] = max(dp[i-1], dp[i-2] + nums[i])` — either skip this house or rob it (and skip previous).

- [ ] **End of Day Review (20 min):** All three share the same "two previous states" recurrence. Notice you only need two variables, not the full array — space optimization. Write the space-optimized versions. House Robber is the template for many DP problems: *"at each step, either include or exclude the current element."*

---

### Tuesday — 1D DP (Medium)

- [ ] **Morning Review (20 min):** Re-write House Robber from memory. Then think: what if you have unlimited "coins" and want to make exact change? That's Coin Change. Think about the recurrence before opening the problem.

**Today's Problems:**
- [ ] [Coin Change](https://leetcode.com/problems/coin-change/) *(Medium)* — `dp[amount] = min coins to make amount`. For each coin: `dp[i] = min(dp[i], dp[i - coin] + 1)`.
- [ ] [Jump Game](https://leetcode.com/problems/jump-game/) *(Medium)* — Greedy: track `maxReach`. If `i > maxReach`, return false.
- [ ] [Jump Game II](https://leetcode.com/problems/jump-game-ii/) *(Medium)* — Greedy: track current window end and furthest reach; increment jumps when you exhaust the window.

- [ ] **End of Day Review (20 min):** Coin Change is a bottom-up DP classic. Write the transition and initialization (`dp[0] = 0`, `dp[i] = infinity`). For Jump Game: notice that a greedy solution (O(n) time, O(1) space) beats DP here — write both and compare. Jump Game II is also greedy — explain why it works.

---

### Wednesday — 1D DP (Medium)

- [ ] **Morning Review (20 min):** Review Coin Change. Think about LIS: `dp[i]` = length of longest increasing subsequence ending at index i. The transition requires a nested loop: for each `j < i`, if `nums[j] < nums[i]`, update `dp[i] = max(dp[i], dp[j] + 1)`.

**Today's Problems:**
- [ ] [Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/) *(Medium)* — O(n²) DP, or O(n log n) with patience sorting (binary search on a `tails` array).
- [ ] [Word Break](https://leetcode.com/problems/word-break/) *(Medium)* — `dp[i]` = can we form `s[:i]` from the dictionary? Transition: for each `j < i`, if `dp[j]` and `s[j:i]` is in wordDict, then `dp[i] = True`.

- [ ] **End of Day Review (20 min):** LIS O(n log n) is a beautiful algorithm worth understanding deeply — write it out. For Word Break: the double loop can be optimized by checking only word lengths from the dictionary. Write the time complexity of both approaches. These are mid-level DP that frequently appear in interviews.

---

### Thursday — 2D DP (Medium)

- [ ] **Morning Review (20 min):** 2D DP extends the state to a grid: `dp[i][j]` = answer using/ending at row i, col j (or for first i rows and first j cols). Write the template: initialize first row and col, then fill row by row.

**Today's Problems:**
- [ ] [Unique Paths](https://leetcode.com/problems/unique-paths/) *(Medium)* — `dp[i][j] = dp[i-1][j] + dp[i][j-1]`. Initialize first row/col to 1.
- [ ] [Minimum Path Sum](https://leetcode.com/problems/minimum-path-sum/) *(Medium)* — `dp[i][j] = grid[i][j] + min(dp[i-1][j], dp[i][j-1])`.

- [ ] **End of Day Review (20 min):** Both problems have the same grid traversal structure — you can only move right or down. Write the space-optimized 1D versions (rolling array: `dp[j]` represents the current row). Understand: Unique Paths has a combinatorial closed-form answer `C(m+n-2, m-1)` — can you derive it?

---

### Friday — 2D DP (Medium/Hard)

- [ ] **Morning Review (20 min):** Review Unique Paths. Now think about two sequences: `dp[i][j]` = answer using first i chars of s1 and first j chars of s2. Write the LCS recurrence: if `s1[i] == s2[j]`: `dp[i][j] = dp[i-1][j-1] + 1`, else `dp[i][j] = max(dp[i-1][j], dp[i][j-1])`.

**Today's Problems:**
- [ ] [Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/) *(Medium)* — Classic 2D DP on two strings. Apply the LCS recurrence above.
- [ ] [Edit Distance](https://leetcode.com/problems/edit-distance/) *(Medium)* — `dp[i][j]` = min edits to convert `word1[:i]` to `word2[:j]`. Three operations: insert, delete, replace.

- [ ] **End of Day Review (20 min):** These are the two most fundamental 2D string DP problems. Write the Edit Distance recurrence from memory: `if chars match: dp[i][j] = dp[i-1][j-1]; else: dp[i][j] = 1 + min(dp[i-1][j], dp[i][j-1], dp[i-1][j-1])`. Understand what each of the three cases represents (delete from word1, insert into word1, replace).

---

### Saturday — 2D DP (Hard)

- [ ] **Morning Review (20 min):** Review Edit Distance. These hard DP problems often involve a non-obvious state definition. For Burst Balloons: think about which balloon you pop *last* in a subrange — that's the key insight.

**Today's Problems:**
- [ ] [Burst Balloons](https://leetcode.com/problems/burst-balloons/) *(Hard)* — `dp[l][r]` = max coins from bursting all balloons between l and r (exclusive). For each choice of last balloon k: `dp[l][r] = max(dp[l][k] + nums[l]*nums[k]*nums[r] + dp[k][r])`.
- [ ] [Regular Expression Matching](https://leetcode.com/problems/regular-expression-matching/) *(Hard)* — `dp[i][j]` = does `s[:i]` match `p[:j]`? Handle `*` carefully: it can mean zero or more of the preceding char.

- [ ] **End of Day Review (20 min):** Burst Balloons: the "last to pop" insight converts a hard problem into a clean interval DP. Write out why thinking "first to pop" leads to a circular dependency. For Regex Matching: trace through `s="aa"`, `p="a*"` step by step. These are some of the hardest DP problems — if you can articulate the state and transition, you've mastered DP.

---

### Sunday — Week 7 Review

- [ ] **Morning Review (20 min):** Skim Week 7 solutions. Pick 2 hardest.

**Tasks:**
- [ ] Re-solve Edit Distance and one other problem from scratch.
- [ ] Write: what are the four steps to solve any DP problem?
- [ ] Add mistakes to your log.

- [ ] **End of Week Review (20 min):** *"DP = optimal substructure + overlapping subproblems. The four steps: (1) define state, (2) write recurrence, (3) initialize base cases, (4) determine fill order. 1D DP: previous 1-2 states. 2D DP: previous row/col. String DP: states over prefix lengths. The hardest part is defining the right state — once that's clear, the recurrence usually follows."*

---

## WEEK 8 — Mixed Review, Heaps, Binary Search & System Design Prep

**What you'll learn:** Heaps for top-K problems; binary search beyond sorted arrays; consolidation of all topics.

**General idea:** Heap = O(log n) insert/delete with O(1) min/max access. Binary search applies wherever the search space is monotonic (not just sorted arrays).

**How to identify Heap:** "Top K," "Kth largest/smallest," "merge K sorted," streaming data.  
**How to identify Binary Search:** "Find in sorted array," "minimum possible maximum," "search rotated array."

---

### Monday — Heap/Priority Queue (Medium)

- [ ] **Morning Review (20 min):** Write the min-heap and max-heap API in your language. In Python: `heapq` is a min-heap; negate values for max-heap. Key operations: `heappush(h, val)` O(log n), `heappop(h)` O(log n), `h[0]` peek O(1). Recall Merge K Sorted Lists from Week 4 — that was heap usage.

**Today's Problems:**
- [ ] [Kth Largest Element in an Array](https://leetcode.com/problems/kth-largest-element-in-an-array/) *(Medium)* — Min-heap of size k: push each element; if size > k, pop. The heap's root is the kth largest.
- [ ] [Top K Frequent Words](https://leetcode.com/problems/top-k-frequent-words/) *(Medium)* — Count frequencies; heap of `(freq, word)` pairs of size k.
- [ ] [Merge K Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/) *(Hard — revisit)* — Min-heap with one node from each list; pop min, push its next.

- [ ] **End of Day Review (20 min):** Kth Largest: min-heap of size k is O(n log k) — better than sorting O(n log n) when k << n. Write the QuickSelect alternative (O(n) average). For Top K Frequent: be careful with tie-breaking — Top K Frequent *Words* requires lexicographic order when frequencies are equal.

---

### Tuesday — Heap (Hard)

- [ ] **Morning Review (20 min):** Recall the heap API. Think about streaming data — you receive numbers one at a time and must always know the median. Two heaps: a max-heap for the lower half, a min-heap for the upper half.

**Today's Problems:**
- [ ] [Find Median from Data Stream](https://leetcode.com/problems/find-median-from-data-stream/) *(Hard)* — Two heaps (max-heap `lo`, min-heap `hi`). Always keep `|lo| - |hi| <= 1`. Median is `lo[0]` or average of both tops.
- [ ] [Task Scheduler](https://leetcode.com/problems/task-scheduler/) *(Medium)* — Always execute the most frequent remaining task first (max-heap). Use a cooldown queue for tasks in their idle period.

- [ ] **End of Day Review (20 min):** Find Median from Data Stream is a classic hard design problem. Write: *"Add to `lo` (max-heap, store negated). If `lo` top > `hi` top, rebalance. If sizes differ by 2, move top to other heap."* For Task Scheduler: there's also a mathematical formula — understand both approaches.

---

### Wednesday — Binary Search (Easy/Medium)

- [ ] **Morning Review (20 min):** Write the binary search template with `lo`, `hi`, `mid`. The key: `mid = lo + (hi - lo) // 2` (avoids overflow). Understand the two variants: (1) `lo <= hi` (find exact), (2) `lo < hi` (converge to boundary). When does `lo` update vs `hi`?

**Today's Problems:**
- [ ] [Binary Search](https://leetcode.com/problems/binary-search/) *(Easy)* — Classic implementation. Practice writing it perfectly.
- [ ] [Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/) *(Medium)* — At least one half is always sorted; use that to decide which half to search.
- [ ] [Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/) *(Medium)* — Binary search for the pivot: the minimum is where the sorted order breaks.

- [ ] **End of Day Review (20 min):** Rotated array binary search is one of the most common medium interview problems. Write the invariant for Search in Rotated: *"if nums[lo] <= nums[mid], left half is sorted; otherwise right half is sorted."* Practice until you can write it from memory without bugs. Off-by-one errors are the #1 mistake in binary search.

---

### Thursday — Binary Search (Medium/Hard)

- [ ] **Morning Review (20 min):** Recall that binary search applies to any *monotonic* search space. The pattern: `lo = minPossible, hi = maxPossible; while lo < hi: mid = ...; if condition(mid): hi = mid; else: lo = mid + 1`. Think: what's the "condition" for Koko Eating Bananas?

**Today's Problems:**
- [ ] [Koko Eating Bananas](https://leetcode.com/problems/koko-eating-bananas/) *(Medium)* — Binary search on eating speed `k`. Condition: can Koko eat all piles in `h` hours at speed `k`?
- [ ] [Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/) *(Hard)* — Binary search on the partition of the shorter array. Ensure left halves together have at most `(m+n)//2` elements.

- [ ] **End of Day Review (20 min):** Koko Eating Bananas is the template for "binary search on answer" — write the pattern and list 3 other problems that use it (Ship Packages, Split Array Largest Sum, etc.). Median of Two Sorted Arrays is extremely hard — focus on understanding *why* binary search works here rather than memorizing the code. Write out the partition invariant.

---

### Friday — Backtracking (Medium)

- [ ] **Morning Review (20 min):** Backtracking = DFS + undo. Template: `def backtrack(start, current): if base_case: results.append(current[:]); return; for choice in choices[start:]: current.append(choice); backtrack(next_start, current); current.pop()`. The `.pop()` is the "undo" that makes it backtracking.

**Today's Problems:**
- [ ] [Subsets](https://leetcode.com/problems/subsets/) *(Medium)* — At each step, choose to include the current element or not. Or: iterate with a start index to avoid duplicates.
- [ ] [Permutations](https://leetcode.com/problems/permutations/) *(Medium)* — No start index needed; use a `used` array to track which elements are in the current permutation.
- [ ] [Combination Sum](https://leetcode.com/problems/combination-sum/) *(Medium)* — Same element can be reused; pass the same index forward (not `start+1`).

- [ ] **End of Day Review (20 min):** These three problems cover the three backtracking variants: subset (combinations without repetition), permutation (all orderings), combination sum (repetition allowed). Write the recurrence for each. Key: always make a copy when appending to results (e.g., `results.append(current[:])`). The time complexity of backtracking is exponential — know how to express it for each problem.

---

### Saturday — Mock Interview Day

- [ ] **Morning Review (20 min):** Review the Pattern Recognition Cheat Sheet. For each pattern, recall: (1) recognition cue, (2) algorithm, (3) time/space complexity, (4) one example problem. This is your pre-interview ritual.

**Tasks:**
- [ ] **Mock Problem 1 (45 min timer):** Pick one of: [Random Medium on LeetCode](https://leetcode.com/problems/random-one-question-from-medium/), [Combination Sum II](https://leetcode.com/problems/combination-sum-ii/), or [Pacific Atlantic Water Flow](https://leetcode.com/problems/pacific-atlantic-water-flow/). Write your approach first (2 min), code it, test with examples.
- [ ] **Mock Problem 2 (45 min timer):** Pick one of: [Partition Equal Subset Sum](https://leetcode.com/problems/partition-equal-subset-sum/), [Gas Station](https://leetcode.com/problems/gas-station/), or [Maximum Product Subarray](https://leetcode.com/problems/maximum-product-subarray/).
- [ ] **Mock Problem 3 (45 min timer):** Pick one of: [Decode Ways](https://leetcode.com/problems/decode-ways/), [Palindromic Substrings](https://leetcode.com/problems/palindromic-substrings/), or [Maximum Width of Binary Tree](https://leetcode.com/problems/maximum-width-of-binary-tree/).

- [ ] **End of Day Review (20 min):** Review each mock problem: did you identify the pattern within 2 minutes? Where did you get stuck? How was your time management? Write down what you'd do differently. This is a dry run of the real interview.

---

### Sunday — Full Mock Interview Day

- [ ] **Morning Review (20 min):** Skim your mistake log from all 8 weeks. Write down the top 5 patterns you're least confident in. Mentally rehearse: *"I see [cue], so I'll try [pattern], which works because [reason]."*

**Tasks:**
- [ ] **Mock Interview Part 1 (45 min):** Pick a random medium — write your full approach out loud (or in comments) before coding. Treat it like a real interview: no hints, no peeking.
- [ ] **Mock Interview Part 2 (45 min):** Pick another random medium from a different topic area.
- [ ] **Mock Interview Part 3 (60 min):** Pick a hard problem — spend 5 min writing your approach in plain English, then code it up. Aim for a working brute force first, then optimize.

- [ ] **End of 8-Week Review (20 min):** *Congratulations — you've completed the plan!* Write a full summary in your notes: which patterns felt natural, which need more practice, and which 5 problems you'd redo before your interview. Schedule at least 2 more mock interview days in the week before your interview. You are ready.*

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