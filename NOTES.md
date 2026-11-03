   # My DSA Notes

   ## Day 2: Asymptotic analysis and complexity

**What it is:** a way to measure how an algorithm's running time grows as the input size (n) grows. It ignores the speed of the computer and looks only at the growth.

**Three notations**
- **Big-O (O):** upper bound, the worst case. "It will take at most this long."
- **Big-Omega (Ω):** lower bound, the best case.
- **Big-Theta (Θ):** tight bound, when the best and worst growth are the same.

**Growth rates, from fastest to slowest**
O(1) < O(log n) < O(n) < O(n log n) < O(n²) < O(2ⁿ) < O(n!)

**Two rules for simplifying**
1. Drop constants: n²/2 becomes O(n²).
2. Drop smaller terms: n² + n becomes O(n²).

**Examples from code**
- One loop over n items: O(n).
- A loop inside a loop: O(n²).
- A single statement, like returning nums[0]: O(1).

**My problems so far**
| Problem | Approach | Time | Space |
|---|---|---|---|
| Two Sum | Brute force (check all pairs) | O(n²) | O(1) |
| Contains Duplicate | Brute force (check all pairs) | O(n²) worst case | O(1) |

**What I noticed:** in Contains Duplicate, if the first two numbers are equal, the code stops right away, which is the best case, O(1). If there's no duplicate, it checks every pair, which is the worst case, O(n²). Big-O describes the worst case.

**Why O(n²) is a problem:** with 1 million items, n² is about 1 trillion steps. Hashing (coming on Day 3) will make these O(n).