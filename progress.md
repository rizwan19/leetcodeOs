# Leetcode Progress Tracker

**Goal:** 3 problems per week. Build confidence across all core patterns.
**Started:** 2026-07-18

---

## Weekly Progress
*(Mon–Sun weeks. Target: 3/week)*

| Week | Completed | Target | Status |
|------|-----------|--------|--------|
| 2026-07-13 – 2026-07-19 | 1 | 3 | 🟡 in progress |

---

## Stats
- Total solved: 1
- Easy: 1 | Medium: 0 | Hard: 0
- Tracker active since: 2026-07-18

---

## Problem Log
*(sorted most recent first | Attempts = number of submissions before accepted)*

| Date | # | Title | Difficulty | Category | Attempts | Notes |
|------|---|-------|------------|----------|----------|-------|
| 2026-07-18 | 1 | Two Sum | Easy | Arrays & Hashing | 1 | Independent solve. Two-pass hashmap; handled `[3,3]` duplicate via `i != map.get(num)` check. Conf 4 only because one-pass wasn't obvious at first — derived it on his own after. |

---

## Spaced Repetition Queue
*(SM-2 algorithm — see CLAUDE.md. Sort: ascending Next Review.)*

| # | Title | Last Review | Reps | EF | Interval (d) | Next Review | Fails | Skips |
|---|-------|-------------|------|------|--------------|-------------|-------|-------|
| 1 | Two Sum | 2026-07-18 | 1 | 2.50 | 3 | 2026-07-21 | 0 | 0 |

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
| Two Pointers | 5 | 0 | **5** | never | — | 🔥 urgent |
| Sliding Window | 6 | 0 | **6** | never | — | 🔥 urgent |
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
| Two Pointers | 0 | Not started |
| Sliding Window | 0 | Not started |
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

### 2026-07-18 — Session 1 (first session)
- Solved #1 Two Sum independently. Aha: store-what-you've-seen turns O(n²) pair-scanning into O(n).
- Duplicate edge case `[3,3]` handled correctly with `i != map.get(num)`.
- Derived the one-pass variant (check complement before insert) on his own after the two-pass solve — that was the conf-4 gap, now closed.
