# Solution

## Task 7 — k-Permutations (Ordered Selections Without Repetition)

When we choose $k$ from $n$ distinct objects and **order matters**, with **no repetition**, we use **k-permutations**:

$$
P(n,k) = \frac{n!}{(n-k)!} = n(n-1)(n-2) \cdots (n-k+1)
$$

---

# 1. First three places among 12 runners

**Problem:** In how many ways can gold, silver, and bronze be assigned among 12 runners?

**Reasoning:** Order matters — 1st, 2nd, 3rd are different. Each medal goes to a different runner. We assign 3 distinct positions to 3 different people.

$$
P(12,3) = 12 \cdot 11 \cdot 10 = 1\,320
$$

**Answer:** 1,320 ways.

---

# 2. 4-digit numbers with distinct digits from 1–9

**Problem:** How many 4-digit numbers have **all different digits** from the set $\{1, 2, \ldots, 9\}$?

**Reasoning:** A 4-digit number has positions: thousands, hundreds, tens, units. No leading zero. Digits must all be different.

- Thousands: 9 choices ($1$–$9$)
- Hundreds: 8 remaining
- Tens: 7 remaining
- Units: 6 remaining

$$
P(9,4) = 9 \cdot 8 \cdot 7 \cdot 6 = 3\,024
$$

**Answer:** 3,024 numbers.

---

# 3. Such numbers divisible by 5

**Problem:** How many of these 4-digit numbers (distinct digits from 1–9) are **divisible by 5**?

**Reasoning:** Divisible by 5 $\Rightarrow$ last digit is **5**.

- Fix last digit: 5 (1 choice)
- First 3 digits: choose 3 distinct from $\{1, 2, 3, 4, 6, 7, 8, 9\}$ (8 digits), in order

$$
P(8,3) = 8 \cdot 7 \cdot 6 = 336
$$

**Answer:** 336 numbers divisible by 5.

---

# Summary

- Top 3 from 12 runners — $P(12,3) = 1\,320$
- 4-digit, distinct 1–9 — $P(9,4) = 3\,024$
- Divisible by 5 — $P(8,3) = 336$
