# Leetcode Progress Tracker

**Goal:** 3 problems per week. Build confidence across all core patterns.
**Started:** 2026-07-18

---

## Weekly Progress
*(Mon–Sun weeks. Target: 3/week)*

| Week | Completed | Target | Status |
|------|-----------|--------|--------|
| 2026-11-23 – 2026-11-29 | 1 new (3 reviews) | 3 | 🔄 in progress |
| 2026-11-16 – 2026-11-22 | 0 new (7 reviews) | 3 | 🔄 warm-up sprint after 82-day gap |
| 2026-08-31 – 2026-09-06 | 0 new (1 review) | 3 | 🔄 warm-up sprint continues |
| 2026-08-24 – 2026-08-30 | 0 new (2 reviews) | 3 | 🔄 warm-up sprint after 42-day gap |
| 2026-07-13 – 2026-07-19 | 5 | 3 | ✅ target exceeded |

---

## Stats
- Total solved: 6
- Easy: 6 | Medium: 0 | Hard: 0
- Tracker active since: 2026-07-18

---

## Problem Log
*(sorted most recent first | Attempts = number of submissions before accepted)*

| Date | # | Title | Difficulty | Category | Attempts | Notes |
|------|---|-------|------------|----------|----------|-------|
| 2026-11-25 | 121 | Best Time to Buy and Sell Stock | Easy | Sliding Window | 1 | **Review** (not a new solve — Stats/Pattern Targets unchanged). On time. **Pass, conf 5** (self-graded; coach suggested 4 for Q3 nudges, user kept 5). Q1 clean (O(n²), re-scans the future per buy day). Q2 clean (running min). Q3 first answer "min from the past ≤ current price" — `[7,1]` counterexample drew out the min-update-before-profit ordering; one follow-up drew out the second guarantee (`maxProfit = 0` init + `Math.max`). Named both this time (11-22 named only `Math.max`). Code identical to prior solves, correct first try. |
| 2026-11-25 | 125 | Valid Palindrome | Easy | Two Pointers | 1 | **Review** (not a new solve — Stats/Pattern Targets unchanged). On time. **Pass, conf 4** — self-graded 5, settled on 4 after discussion (Q2 nudge). Q3 clean (`'0'`/`'P'` differ by 32 → `Character.toLowerCase`). Q1 needed a second round, partly due to coach wording; then stated it fully: unguarded skip loop on `".,"` reaches `charAt(2)` → out of bounds, and the outer `left < right` is only re-checked between iterations. Q2 first answered `left < right`; the `",a"` trace (`left == right == 1`) corrected it to `left ≤ right`. Code identical to the last two reviews, correct first try. |
| 2026-11-23 | 242 | Valid Anagram | Easy | Arrays & Hashing | 2 | First new problem since July. Conf 5 (self-graded). Pre-code: Q1 clean (same length + same per-char counts); Q2 right on sort = O(n log n) and counting instead, but muddled it with "time O(n) too"; Q3 clean (`int[26]`, O(1) space since size is fixed). Solved independently with two frequency arrays, single loop (safe after the length check), 26-slot compare. Couldn't get the single-array form unaided — after a hint (`freqS[i] - freqT[i] != 0` → store the difference) wrote `++` for `s`, `--` for `t`, check all zero. |
| 2026-11-23 | 167 | Two Sum II — Input Array Is Sorted | Easy | Two Pointers | 1 | **Review** (not a new solve — Stats/Pattern Targets unchanged). Next-day retry after yesterday's fail. **Pass, conf 4** — self-graded 5, settled on 4 after discussion (Q2/Q3 nudges). Q1 clean: cited O(1)-space as why the hashmap is out, binary search O(n log n) vs. two-pointer O(n). Q2 discard proof built himself for the first time in three sessions — first draft checked only `left+1` and stopped at the element inequality; after a nudge generalized to every `k ≥ left` and carried it to the sum (> target), and explained indices below `left` as already eliminated. Q3: reasoned from "elements can't be the same" — refined to same *index*, not value (`[3,3]` target 6 is valid). Java code correct first try: three-way branch, `left < right`, 1-indexed return. |
| 2026-11-22 | 167 | Two Sum II — Input Array Is Sorted | Easy | Two Pointers | 1 | **Review** (not a new solve — Stats/Pattern Targets unchanged). **Fail, conf 2** (self-graded 2 on recommendation) after 84 days. Reached for per-element binary search (O(n log n), O(1)) first; didn't cite the O(1)-space constraint as why the hashmap is out. Needed the converge-from-both-ends hint for the O(n) approach. Q2 discard proof given after two partial attempts ("left already moved forward"). Q3 picked `<` but reasoned from the one-solution guarantee rather than "`left == right` = same element twice". Code after the hint correct and clean: three-way branch, `left < right`, 1-indexed return. |
| 2026-11-22 | 1 | Two Sum | Easy | Arrays & Hashing | 1 | **Review** (not a new solve — Stats/Pattern Targets unchanged). 84 days since last review, conf 3 (self-graded — couldn't produce the check-before-insert correctness reason). Java one-pass: complement check, then `put`. Q1 brute force O(n²) correct but omitted the O(n) space trade until asked. Q2 order right, reason missing — after a `[3,3]` trace, stated insert-first finds itself (`[0,0]`). Same nudge needed in August. Q3 clean (key = number for O(1) lookup by value, value = index to return). Nit repeated in Java: `containsKey` + `get` = two lookups; single `get` + null check. |
| 2026-11-22 | 125 | Valid Palindrome | Easy | Two Pointers | 1 | **Review** (not a new solve — Stats/Pattern Targets unchanged). Next-day retry after yesterday's fail. **Pass, conf 4** — self-graded 5, settled on 4 after discussion (one nudge). Q1 clean (pre-clean O(n), in-place O(1) — yesterday's slip fixed). Q3 clean (`'0'`=48 vs `'P'`=80, use `Character.toLowerCase`). Q2 ambiguous ("bound check after the skip") — traced the after-loop version on `".,"` and identified the `StringIndexOutOfBoundsException` himself. Code identical to yesterday, guard inside the left loop body. Sentinel answer close: said "leftmost char is alphanumeric" — refined to `s[left]` alphanumeric **and** `left ≤ right`. |
| 2026-11-22 | 121 | Best Time to Buy and Sell Stock | Easy | Sliding Window | 1 | **Review** (not a new solve — Stats/Pattern Targets unchanged). Next-day retry after yesterday's fail. Independent re-solve, conf 5, no peeking. Pre-code: named the redundant re-scan and the running-min reframe; explained non-negativity via min-update-before-profit ordering. Missed brute-force complexity (answered O(n) for the optimized one; brute force is O(n²)). On the swapped-lines follow-up credited `Math.max` alone — also needs `maxProfit = 0` init. Code identical in shape to July: `minPrice = MAX_VALUE`, update min, then `max(maxProfit, price - minPrice)`. |
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
| 643 | Maximum Average Subarray I | 2026-11-21 | 1 | 2.70 | 3 | 2026-11-24 | 0 | 0 |
| 1 | Two Sum | 2026-11-22 | 1 | 2.46 | 3 | 2026-11-25 | 0 | 0 |
| 167 | Two Sum II — Input Array Is Sorted | 2026-11-23 | 1 | 2.38 | 3 | 2026-11-26 | 0 | 0 |
| 242 | Valid Anagram | 2026-11-23 | 0 | 2.50 | 3 | 2026-11-26 | 0 | 0 |
| 125 | Valid Palindrome | 2026-11-25 | 2 | 2.28 | 7 | 2026-12-02 | 0 | 0 |
| 121 | Best Time to Buy and Sell Stock | 2026-11-25 | 2 | 2.48 | 7 | 2026-12-02 | 0 | 0 |

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
| Arrays & Hashing | 10 | 2 | **8** | 2026-11-23 | 0 | 🔥 urgent |
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
| Arrays & Hashing | 2 | Hashmap complement trick (#1); fixed-alphabet frequency array, single balance array `++`/`--` (#242) |
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

- **Reasoning decays faster than code** (surfaced 2026-08-31 on #125). After 42 days he re-wrote a correct O(1)-space solution first try but could not recall the two variants, the reason for the skip guard, or the `"0P"` case-fold trap. Implication for reviews: lead with the pre-code questions and grade on those, since a clean solve alone overstates retention. **Confirmed 2026-11-21:** #125's guard and `"0P"` questions went blank on two reviews in a row; #121's approach itself was gone. **Escalated:** at 125 days #121's approach itself was gone (fail, needed old submission). Long gaps are the root problem — steady cadence matters more than any single review. **Recovering 2026-11-22:** next-day retries of #121 and #125 both passed with pre-code reasoning largely intact — short-interval re-drill after a fail works.
- **Justifying an elimination, not just performing it** (surfaced 2026-08-30 on #167). Pointer/branch moves are correct, but the stated reason defends the direction chosen rather than proving the discarded candidates are all invalid. Matters the moment loop bounds get non-obvious — Binary Search will punish it. Re-check when Binary Search opens. **Recurred 2026-11-22 on #1:** check-before-insert ordering performed correctly but the correctness reason (no self-pairing on `[3,3]`) needed a trace — same nudge as August. **Recurred again 2026-11-22 on #167:** discard proof had to be given in full after two partial attempts. **Improving 2026-11-23 on #167:** next-day retry — built the proof himself with one nudge (generalize from `left+1` to every `k ≥ left`, carry the inequality to the sum). Precision is the remaining gap: name *every* candidate eliminated, and finish the chain to the conclusion.

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

### 2026-11-25 — Session 8
- 2 days since last entry → normal session. Due: #643 (1 day late, ratio 1.33 → no decay), #121, #125, #1. No skip candidates (#121/#125 have failed; #643/#1 below Reps 2). Plan: #125 → #121 → #643/#1, then new #49 Group Anagrams for the weekly target.
- #125 Valid Palindrome — **pass, conf 4** (self-graded 5, settled on 4). Third review running where the code came out identical and correct; the reasoning is now the variable.
- Q2 slip: invariant stated as `left < right`. `",a"` → left skip stops at `left == right == 1`, so it's `left ≤ right`. Also refined: the outer loop doesn't break immediately — the iteration finishes with a harmless self-compare of `s[1]`, then `left++/right--` ends it.
- Q1: original question was misread as "delete the skip loop" (coach wording ambiguous). Once clarified: `charAt(2)` throws; outer condition is only checked between iterations.
- SM-2: on time, Reps 1→2, EF 2.28 (unchanged at grade 4), Interval 7 → next 2026-12-02.
- #121 Best Time to Buy and Sell Stock — **pass, conf 5** (user's grade; coach suggested 4 — Q3 needed a counterexample + one follow-up). Q1/Q2 clean, including the O(n²) brute force that slipped on 11-22.
- Q3 non-negativity: two independent guarantees. (1) Min updated before profit → `minPrice ≤ price` → every candidate ≥ 0. (2) `maxProfit = 0` + `Math.max` → a negative candidate can never win, even with the lines swapped. First answer ("min from the past ≤ price") is false for a strictly-past min — `[7,1]` gives −6.
- SM-2: on time, Reps 1→2, EF 2.38→2.48, Interval 7 → next 2026-12-02.

### 2026-11-23 — Session 7
- 1 day since last entry → normal session. Due: #167 (next-day retry after fail). New week opens 0/3.
- #167 Two Sum II — **pass, conf 4** (self-graded 5, settled on 4 — Q2/Q3 needed nudges). On time, no decay.
- Discard proof: first time in three sessions he produced it himself. First draft only checked `left+1` and stopped at `numbers[left+1] ≥ numbers[left]`; nudged to all `k` in `[left, right-1]` and to the sum: `numbers[k] + numbers[right] ≥ current sum > target`. Indices below `left` = already eliminated by earlier `left++` moves (same argument flipped). Each comparison eliminates a whole row/column → O(n). Binary Search is the same move, eliminating half.
- Q3 precision: "can't use the same element twice" means same *index*, not value — `[3,3]` target 6 → `[1,2]` is valid.
- Overflow aside: `numbers[left] + numbers[right]` safe under ±1000 constraints; with large values compare against `target - numbers[right]`. Same trap as `mid = (lo + hi) / 2`.
- Grading calibration held for the second day running: self-graded 5, agreed on 4 for nudge-dependent reasoning.
- SM-2: Fails 1→0, Reps 0→1, EF 2.38 (unchanged at grade 4), Interval 3 → next 2026-11-26.
- #242 Valid Anagram — **first new problem since 2026-07-19** (127 days). Conf 5, 2 submissions. Arrays & Hashing 1→2.
- Two-array solution independent and O(n)/O(1). Single-array version needed a hint: the final check `freqS[i] != freqT[i]` is `freqS[i] - freqT[i] != 0`, so store only the difference.
- Aha: you don't need each string's counts, only whether they **balance** — `++` for `s`, `--` for `t`, all zeros at the end. Same "store only what you'll compare" instinct as #1's complement.
- Early exit: in the interleaved loop a slot can go negative mid-way on valid input (`"ab"`/`"ba"`), so no early return there. Count all of `s` first, then decrement for `t` and return false on any negative — with equal lengths that also removes the final 26-slot scan.
- Q2 slip: stated sort as both O(n) and O(n log n). Sorting is O(n log n) time; the O(n) piece is the `toCharArray` copy (Java strings are immutable).
- New SR entry defaults → next 2026-11-26.

### 2026-11-22 — Session 6
- 1 day since last entry → normal session; warm-up sprint continues. Due: #121, #125 (next-day retries after fails), #1, #167 (81 days overdue; decay ratio ≈ 28 → Reps 1→0).
- #121 Best Time to Buy and Sell Stock — **pass, conf 5**, one day after failing it. Running-min reframe recalled unprompted; non-negativity argued from line ordering (`minPrice ≤ price` after the update).
- Gaps: gave the optimized complexity when asked for brute force (O(n²)). Non-negativity under swapped lines rests on two pieces together — `maxProfit = 0` init *and* `Math.max`; credited only the latter. Same theme as #167/#125: name every piece that makes the guarantee hold.
- SM-2: on time (no decay), Reps 0→1, EF 2.28→2.38, Interval 3 → next 2026-11-25.
- #125 Valid Palindrome — **pass, conf 4**, one day after failing it. First review where Q1 and Q3 came back clean. Q2 answer "check after the skip" was ambiguous between after-each-step (safe) and after-loop-exits (crashes on `".,"` at `charAt(2)`); traced it himself once set up. Showed the idiomatic guard: `while (left < right && !isLetterOrDigit(...))` — short-circuit replaces the early return.
- Sentinel invariant now nearly precise ("leftmost char is alphanumeric") vs. yesterday's "no non-alphanumerics remain". Missing piece: `left ≤ right`, guaranteed by the early return.
- Grading calibration held: self-graded 5, agreed on 4 (one nudge, not answer-given → pass, not fail). EF stays 2.28.
- SM-2: Reps 0→1, EF 2.28 (unchanged at grade 4), Interval 3 → next 2026-11-25.
- #1 Two Sum — **pass, conf 3** (self-graded). 81 days past due: decay ratio = 81/3 + 1 = 28 → Reps 1→0. Code clean; check-before-insert performed but the correctness reason (insert-first returns `[0,0]` on `[3,3]`) needed a trace — **second time** this exact nudge was needed (also 2026-08-30). Filed under the "justify, not perform" weak spot.
- SM-2: Reps 0→1, EF 2.60→2.46, Interval 3 → next 2026-11-25.
- #167 Two Sum II — **fail, conf 2**. 84 days since review (decay → Reps 0). Reached for binary search on the complement — valid but O(n log n); the two-pointer converge needed a hint. Q2/Q3 answers were framed for binary search ("middle value", `<=`) until redirected.
- Discard proof, complete form given: remaining partners of `right` are `numbers[k]`, `k ≥ left` → `numbers[k] ≥ numbers[left]` → every such sum ≥ current sum > target. **Third session** this argument needed supplying (2026-08-30, today). Binary Search will lean on the same proof shape.
- Contrast with #1 same day: #1's approach survived 84 days, #167's didn't. #167 is the reframe-style problem (sortedness ⇒ eliminate a whole column) — same fragility as #121 yesterday.
- SM-2: Fails 1, Reps 0, EF 2.70→2.38, Interval 1 → retry 2026-11-23.
- Week closes 0 new / 7 reviews. Sprint has cleared every overdue item; new-problem work can resume next session.

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
