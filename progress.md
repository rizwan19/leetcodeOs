# Leetcode Progress Tracker

**Goal:** 3 problems per week. Build confidence across all core patterns.
**Started:** 2026-07-18

---

## Weekly Progress
*(Mon–Sun weeks. Target: 3/week)*

| Week | Completed | Target | Status |
|------|-----------|--------|--------|
| 2026-07-13 – 2026-07-19 | 5 | 3 | ✅ target exceeded |

---

## Stats
- Total solved: 5
- Easy: 5 | Medium: 0 | Hard: 0
- Tracker active since: 2026-07-18

---

## Problem Log
*(sorted most recent first | Attempts = number of submissions before accepted)*

| Date | # | Title | Difficulty | Category | Attempts | Notes |
|------|---|-------|------------|----------|----------|-------|
| 2026-07-19 | 643 | Maximum Average Subarray I | Easy | Sliding Window | 1 | Independent solve, conf 5. First true fixed-size window: build initial k-sum, then slide with subtract-one/add-one delta (`sum -= nums[i-1]; sum += nums[i+k-1]`) — O(1) per step, O(n) total. Tracked max sum, divided once at end with `maxSum/(double)k` (sidestepped the integer-division trap). Correct on the `k == n` edge. |
| 2026-07-19 | 121 | Best Time to Buy and Sell Stock | Easy | Sliding Window | 1 | Independent solve, conf 5. Single-pass running-minimum: track `minPrice` seen so far, update `maxProfit = max(maxProfit, price - minPrice)` each step. Reframed "best pair" as "best single fact behind me." Correctly diagnosed brute force as O(n²) repeating the min-search. First Sliding Window problem. |
| 2026-07-18 | 125 | Valid Palindrome | Easy | Two Pointers | 1 | Independent solve, conf 5. Wrote both variants: O(n)-space pre-clean via StringBuilder filter, then O(1)-space in-place — skip non-alphanumeric chars with move-then-compare + `continue`, `start < end` guard prevents overrun. Clear on the space tradeoff. |
| 2026-07-18 | 167 | Two Sum II — Input Array Is Sorted | Easy | Two Pointers | 1 | Independent solve, conf 5. Correctly reasoned that sortedness enables O(1)-space two-pointer converge: sum>target → move right in, sum<target → move left in. Noted O(n/2)=O(n), beats hashmap on space. Solved directly after #1 — saw why input shape changes the optimal approach. |
| 2026-07-18 | 1 | Two Sum | Easy | Arrays & Hashing | 1 | Independent solve. Two-pass hashmap; handled `[3,3]` duplicate via `i != map.get(num)` check. Conf 4 only because one-pass wasn't obvious at first — derived it on his own after. |

---

## Spaced Repetition Queue
*(SM-2 algorithm — see CLAUDE.md. Sort: ascending Next Review.)*

| # | Title | Last Review | Reps | EF | Interval (d) | Next Review | Fails | Skips |
|---|-------|-------------|------|------|--------------|-------------|-------|-------|
| 1 | Two Sum | 2026-07-18 | 1 | 2.50 | 3 | 2026-07-21 | 0 | 0 |
| 121 | Best Time to Buy and Sell Stock | 2026-07-19 | 1 | 2.60 | 3 | 2026-07-22 | 0 | 0 |
| 643 | Maximum Average Subarray I | 2026-07-19 | 1 | 2.60 | 3 | 2026-07-22 | 0 | 0 |
| 167 | Two Sum II — Input Array Is Sorted | 2026-07-18 | 1 | 2.60 | 3 | 2026-07-21 | 0 | 0 |
| 125 | Valid Palindrome | 2026-07-18 | 1 | 2.60 | 3 | 2026-07-21 | 0 | 0 |

---

## Parked Problems
*(Pulled from SR rotation after 3 consecutive fails or manually. Retry after completing bridge problems.)*

| # | Title | Pattern | Parked On | Reason | Bridge Problems |
|---|-------|---------|-----------|--------|-----------------|

*(none currently)*

---

## Retired Problems
*(Removed from active rotation by user choice — outgrown, duplicate, or personally disliked. Problem Log entries remain as history. No further reviews scheduled.)*

| # | Title | Pattern | Retired On | Reason |
|---|-------|---------|------------|--------|

*(none currently)*

---

## Pattern Targets
*(Target counts loosely aligned with NeetCode 150. Gap = Target − Solved. Prioritize patterns with high Gap and stale Last New.)*

| Pattern | Target | Solved | Gap | Last New | Days Stale | Priority |
|---------|--------|--------|-----|----------|------------|----------|
| Arrays & Hashing | 10 | 1 | **9** | 2026-07-18 | 0 | 🔥 urgent |
| Two Pointers | 5 | 2 | **3** | 2026-07-18 | 0 | 🔥 urgent |
| Sliding Window | 6 | 2 | **4** | 2026-07-19 | 0 | 🔥 urgent |
| Stack | 7 | 0 | **7** | never | — | 🔥 urgent |
| Binary Search | 7 | 0 | **7** | never | — | 🔥 urgent |
| Linked List | 10 | 0 | **10** | never | — | 🔥 urgent |
| Trees | 12 | 0 | **12** | never | — | 🔥 urgent |
| Tries | 3 | 0 | **3** | never | — | 🔥 urgent |
| Heap / Priority Queue | 7 | 0 | **7** | never | — | 🔥 urgent |
| Backtracking | 8 | 0 | **8** | never | — | 🔥 urgent |
| Graphs | 10 | 0 | **10** | never | — | 🔥 urgent |
| Dynamic Programming | 12 | 0 | **12** | never | — | 🔥 urgent |
| Greedy | 8 | 0 | **8** | never | — | 🔥 urgent |
| Intervals | 5 | 0 | **5** | never | — | 🔥 urgent |
| Bit Manipulation | 5 | 0 | **5** | never | — | 🔥 urgent |
| Math | 3 | 0 | **3** | never | — | 🔥 urgent |

---

## Category Coverage

| Category | Problems Solved | Coverage Notes |
|----------|----------------|----------------|
| Arrays & Hashing | 1 | Started — hashmap complement trick (#1) |
| Two Pointers | 2 | sorted-array converge (#167), mirror-compare + in-place skip (#125) |
| Sliding Window | 2 | Running-minimum (#121); fixed-size window slide with subtract/add delta (#643) |
| Stack | 0 | Not started |
| Binary Search | 0 | Not started |
| Linked List | 0 | Not started |
| Trees | 0 | Not started |
| Tries | 0 | Not started |
| Heap / Priority Queue | 0 | Not started |
| Backtracking | 0 | Not started |
| Graphs | 0 | Not started |
| Dynamic Programming | 0 | Not started |
| Greedy | 0 | Not started |
| Intervals | 0 | Not started |
| Bit Manipulation | 0 | Not started |
| Math | 0 | Not started |

---

## Weak Spots Summary
*(use this to prioritize new problems — fills in as you go)*

_(none yet — start solving and patterns with high Gap will surface here)_

---

## Requested Problems
*(Problems from interviews or specific areas to practice — prioritize these in upcoming sessions)*

| # | Title | Source | Date Added | Status |
|---|-------|--------|------------|--------|

---

## Session Notes
<!-- Add notes from each session here -->

### 2026-07-19 — Session 2
- Solved #121 Best Time to Buy and Sell Stock independently (conf 5). Opened the Sliding Window pattern.
- Aha: reframe "find the best pair" as "track the best single fact behind me" (running min buy price) — collapses O(n²) pair-search to one O(n) pass. Same instinct #53 Kadane's and #3 will reuse.
- Solved #643 Maximum Average Subarray I independently (conf 5). First true fixed-size window.
- Aha: reuse the previous window's work — sliding changes only two elements, so a subtract-one/add-one delta gives O(1) per step. Also cast before dividing (`maxSum/(double)k`) to dodge integer division.
- Two Sliding Window problems in one session. Weekly target exceeded: 5/3.

### 2026-07-18 — Session 1 (first session)
- Solved #1 Two Sum independently. Aha: store-what-you've-seen turns O(n²) pair-scanning into O(n).
- Duplicate edge case `[3,3]` handled correctly with `i != map.get(num)`.
- Derived the one-pass variant (check complement before insert) on his own after the two-pass solve — that was the conf-4 gap, now closed.
- Solved #167 Two Sum II independently (conf 5) right after #1. Aha: a sorted array lets each comparison discard a whole set of candidate pairs, trading the hashmap's O(n) space for O(1). Clean articulation of when to reach for two-pointer vs. hashmap based on input shape.
- Solved #125 Valid Palindrome independently (conf 5), both variants. Aha: no need to materialize a cleaned string — skip non-alphanumeric chars in place to drop from O(n) to O(1) space. Second core two-pointer shape (mirror-compare) alongside #167's converge-to-target. Hit weekly target 3/3.
