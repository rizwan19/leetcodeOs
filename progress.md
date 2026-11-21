# Leetcode Progress Tracker

**Goal:** 3 problems per week. Build confidence across all core patterns.
**Started:** 2026-07-18

---

## Weekly Progress
*(Mon–Sun weeks. Target: 3/week)*

| Week | Completed | Target | Status |
|------|-----------|--------|--------|
| 2026-11-16 – 2026-11-22 | 0 new (3 reviews) | 3 | 🔄 warm-up sprint after 82-day gap |
| 2026-08-31 – 2026-09-06 | 0 new (1 review) | 3 | 🔄 warm-up sprint continues |
| 2026-08-24 – 2026-08-30 | 0 new (2 reviews) | 3 | 🔄 warm-up sprint after 42-day gap |
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
| 2026-11-21 | 125 | Valid Palindrome | Easy | Two Pointers | 2 | **Review** (not a new solve — Stats/Pattern Targets unchanged). **Fail, conf 2** — self-graded 4, re-graded to 2 per rubric (hints needed). Code correct and independent: in-place O(1), `Character.toLowerCase` compare, left skip loop guarded by increment-then-`if (left > right) return true`, right loop unguarded but safe. Pre-code: named both variants but called pre-clean O(1) (it's O(n)); Q2 (guard placement / `".,"` crash) and Q3 (`"0P"` trap) blank for the **second review running** — Q2 needed the answer, Q3 a nudge. First version missed `".,"`. Explained the unguarded right loop as "no non-alphanumerics remain" — actual invariant is `s[left]` is alphanumeric and `left ≤ right`, so it acts as a sentinel. |
| 2026-11-21 | 643 | Maximum Average Subarray I | Easy | Sliding Window | 1 | **Review** (not a new solve — Stats/Pattern Targets unchanged). Independent re-solve, conf 5, no peeking. All three pre-code answers correct: O(n·k) brute force vs. O(1) delta per slide, track max sum not average (constant `k` preserves order), cast before dividing. Seeded `maxSum` with the first window's sum (not 0), so all-negative input is correct. Correct on `k == n`. Style nit: `for (i = k; i < n; i++) sum += nums[i] - nums[i-k]` indexes by the incoming element. |
| 2026-11-21 | 121 | Best Time to Buy and Sell Stock | Easy | Sliding Window | 1 | **Review** (not a new solve — Stats/Pattern Targets unchanged). **Fail, conf 2** — could not recall the approach after 125 days; looked at the old submission, then wrote a correct running-min solution (`minPrice = Integer.MAX_VALUE`, update min then `maxProfit = max(maxProfit, price - minPrice)`). Self-graded 3, re-graded to 2 per rubric (needed solution). Pre-code answers partial: named the brute force but not O(n²) or the redundant re-scan; said `minPrice` starts at 7 while code uses `MAX_VALUE`; didn't state why the result can't go negative. |
| 2026-08-31 | 125 | Valid Palindrome | Easy | Two Pointers | 1 | **Review** (not a new solve — Stats/Pattern Targets unchanged). Conf 4, **hints given**. Code came out correct first try and clean: guarded inner skip loops (`left < right` inside both), real `lowercaseChar()` compare, O(1) space. But he couldn't answer any of the three pre-code questions — didn't recall the two variants, guessed the guard was half-length, didn't know the `"0P"` trap — so all three were explained before he coded. Self-graded 4 for exactly that reason. First split between retained *code shape* and lost *reasoning* — worth watching. |
| 2026-08-30 | 167 | Two Sum II — Input Array Is Sorted | Easy | Two Pointers | 1 | **Review** (not a new solve — Stats/Pattern Targets unchanged). Independent re-solve, conf 5. Kotlin three-way branch on `sum` vs `target`, `while (left < right)`, 1-indexed return. Nailed the sortedness-replaces-the-hashmap point and both traps (1-indexing, strict `<` so no self-pairing). Needed one nudge on the discard proof: he argued *why not move left*, rather than the stronger claim that `numbers[right]` is eliminated from every remaining pair (all remaining candidates are ≥ `numbers[left]`, so all those sums exceed target) — that's what makes it O(n) instead of O(n²). |
| 2026-08-30 | 1 | Two Sum | Easy | Arrays & Hashing | 1 | **Review** (not a new solve — Stats/Pattern Targets unchanged). Independent re-solve, conf 5 — up from conf 4 on the original. Kotlin one-pass, `forEachIndexed` with non-local return. Answered all three pre-code questions correctly and went straight to one-pass, closing the July conf-4 gap. Extended the look-before-insert rule from an efficiency argument to a correctness one after a nudge — insert-first returns `[0,0]` on `[3,3]`. Nit raised: `containsKey` + `getValue` = two map lookups; single-lookup form is `numMap[secondNum]?.let { ... }`. |
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
| 1 | Two Sum | 2026-08-30 | 1 | 2.60 | 3 | 2026-09-02 | 0 | 0 |
| 167 | Two Sum II — Input Array Is Sorted | 2026-08-30 | 1 | 2.70 | 3 | 2026-09-02 | 0 | 0 |
| 121 | Best Time to Buy and Sell Stock | 2026-11-21 | 0 | 2.28 | 1 | 2026-11-22 | 1 | 0 |
| 125 | Valid Palindrome | 2026-11-21 | 0 | 2.28 | 1 | 2026-11-22 | 1 | 0 |
| 643 | Maximum Average Subarray I | 2026-11-21 | 1 | 2.70 | 3 | 2026-11-24 | 0 | 0 |

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

- **Reasoning decays faster than code** (surfaced 2026-08-31 on #125). After 42 days he re-wrote a correct O(1)-space solution first try but could not recall the two variants, the reason for the skip guard, or the `"0P"` case-fold trap. Implication for reviews: lead with the pre-code questions and grade on those, since a clean solve alone overstates retention. **Confirmed 2026-11-21:** #125's guard and `"0P"` questions went blank on two reviews in a row; #121's approach itself was gone. **Escalated:** at 125 days #121's approach itself was gone (fail, needed old submission). Long gaps are the root problem — steady cadence matters more than any single review.
- **Justifying an elimination, not just performing it** (surfaced 2026-08-30 on #167). Pointer/branch moves are correct, but the stated reason defends the direction chosen rather than proving the discarded candidates are all invalid. Matters the moment loop bounds get non-obvious — Binary Search will punish it. Re-check when Binary Search opens.

---

## Requested Problems
*(Problems from interviews or specific areas to practice — prioritize these in upcoming sessions)*

| # | Title | Source | Date Added | Status |
|---|-------|--------|------------|--------|

---

## Session Notes
<!-- Add notes from each session here -->

### 2026-08-30 — Session 3 (warm-up sprint after 42-day gap)
- 42 days since the last entry (2026-07-19). Gap ≥ 30 → warm-up sprint of high-confidence reviews before any new pattern.
- All 5 SR items were ~40 days past due against `Interval 3`. Lateness decay: `ratio = 40/3 + 1 ≈ 14.3` → `floor(log2 14.3) = 3` → pre-grade `Reps = max(0, 1-3) = 0` for #1/#167/#125; `ratio = 39/3 + 1 = 14` → same `Reps = 0` for #121/#643. No skip candidates — decay floored every one.
- #1 Two Sum re-solved independently, conf 5 (was conf 4 in July). The July gap — one-pass not obvious — is now closed; he went straight to one-pass.
- Aha reinforced: storing what you've already seen turns O(n²) pair-scanning into O(n) — space traded for the second scan.
- New depth on an old rule: he justified look-before-insert on efficiency (skip the insert on a hit). Nudged him to the correctness argument — insert-first returns `[0,0]` on `[3,3]`, so the ordering is what enforces "can't use the same element twice," not just an optimization.
- #167 Two Sum II re-solved independently, conf 5. Both traps cleared unprompted: 1-indexed return, and `while (left < right)` (not `<=`) so no element pairs with itself.
- Weak spot surfaced — *justifying* the discard, not performing it. He moved the right pointer correctly but defended it as "moving left would only increase the sum." The load-bearing argument is that `numbers[right]` is dead in every remaining pair, since all surviving candidates are ≥ `numbers[left]`. Eliminating a whole column per comparison is what buys O(n). Same instinct binary search needs — watch whether it transfers when Binary Search opens.
- Remaining in sprint: #121, #643.

### 2026-08-31 — Session 4 (sprint continued past midnight)
- #125 Valid Palindrome, conf 4 — first non-5 of the sprint, and the most informative result so far. Code was correct first try; the *reasoning* behind it was gone.
- Couldn't name the two variants (pre-clean O(n) vs. in-place O(1)), guessed the skip guard was half-length, and didn't know the `"0P"` trap. All three explained before he coded.
- Why half-length fails: skipping is data-dependent, so the pointers meet at the midpoint of the *cleaned* content at unknown original indices — never at `n/2`. Guard belongs inside the skip loops; without it `".,"` walks `left` past the end into a `StringIndexOutOfBoundsException`.
- `"0P"` trap: `abs(a - b) == 32` as a case-fold. `'0'`=48, `'P'`=80 differ by exactly 32, so the shortcut returns true on a non-palindrome. ±32 is a fact about ASCII's letter range, not a general case-fold; digits have no case. Use `lowercaseChar()`.
- Noted for him: when a skip loop exits on `left == right`, the code compares that char with itself — always passes, and cheaper than branching around it.
- **Pattern across the sprint:** muscle memory for code survived 42 days; the derivations did not. #1 and #167 hid this because their reasoning is short enough to re-derive live. Reviews should keep leading with the questions, not the code.

### 2026-11-21 — Session 5 (warm-up sprint after 82-day gap)
- 82 days since the last entry (2026-08-31). Gap ≥ 30 → warm-up sprint. Lateness decay floored every SR item to `Reps = 0` (ratios ≈27–42); all > 60 days since review, so no skip candidates.
- Sprint order: #121, #643 (unfinished from last sprint, 125 days since solve), then #125 (conf 4 last time on reasoning).
- #121 Best Time to Buy and Sell Stock — **first fail**. Couldn't recall the approach; looked at the old submission. Self-graded 3, re-graded to 2 per rubric. `Fails = 1`, `EF 2.60 → 2.28`, back tomorrow (2026-11-22).
- Decay escalated: at 42 days the code survived and reasoning faded (#125); at 125 days the approach itself was gone. Short, aha-dependent problems are the most fragile — the one insight *is* the solution.
- Gaps in pre-code answers worth re-drilling tomorrow: brute force is O(n²) because each buy day re-scans the future; running min makes that scan redundant. Non-negative result is guaranteed by `maxProfit = 0` init + `max`, and min-before-profit ordering makes every candidate ≥ 0.
- #643 Maximum Average Subarray I — independent re-solve, conf 5, all pre-code questions answered without looking. Contrast with #121 on the same day/gap: #643's solution is mechanical (build window, slide delta) and survives; #121 hinges on a single reframe ("best fact behind me") and didn't. Reframe-style insights need more frequent review than mechanical ones.
- #125 Valid Palindrome — **fail, conf 2** (self-graded 4, re-graded per rubric). Code independent and correct; reasoning blank on the same two questions as August. Confirms the August conf 4 was too generous — hints-then-high-grade let the gap slip through.
- Key lesson filed: **a loop that moves a pointer must check the bound in its own condition** — the outer `while (left < right)` is only re-checked between iterations. Without it, `".,"` → `StringIndexOutOfBoundsException`, not a clean exit.
- Sentinel invariant: after the left skip loop, `s[left]` is alphanumeric and `left ≤ right`, so the right loop always stops at `left` at worst. Their first explanation ("no non-alphanumerics remain") was imprecise — same theme as #167: name exactly what makes a move safe.
- `"0P"`: ±32 is only a case relationship between letters (`'0'`=48, `'P'`=80). Use `Character.toLowerCase` rather than char arithmetic.
- Grading calibration: when pre-code questions need hints, grade 2 regardless of how clean the code is. Applied to both fails today.

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
