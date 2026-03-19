# Solution

## Task 8 — Sequences with Repetition

When each of $k$ positions is filled **independently** from an $n$-element set, with **repetition allowed**, the number of sequences is

$$
n^k
$$

---

# 1. 5-digit PIN codes (digits may repeat)

**Problem:** How many 5-digit PIN codes are possible if digits may repeat?

**Reasoning:** Each of 5 positions: 10 choices (digits $0$–$9$). Positions are independent.

$$
10^5 = 100\,000
$$

**Answer:** 100,000 codes.

---

# 2. Codes with at least one repeated digit

**Problem:** How many 5-digit codes contain **at least one** repeated digit?

**Strategy:** Use the **complement** — total codes minus codes with **all digits different**.

- Total: $10^5 = 100\,000$
- All different: $P(10,5) = 10 \cdot 9 \cdot 8 \cdot 7 \cdot 6 = 30\,240$

$$
100\,000 - 30\,240 = 69\,760
$$

**Answer:** 69,760 codes have at least one repeated digit.

---

# 3. Codes with all digits different

**Problem:** How many 5-digit codes have **all digits different**?

**Reasoning:** Choose 5 distinct digits and place them in order — k-permutation.

$$
P(10,5) = 10 \cdot 9 \cdot 8 \cdot 7 \cdot 6 = 30\,240
$$

**Answer:** 30,240 codes with all digits different.

---

# Summary

- All 5-digit codes — $10^5 = 100\,000$
- At least one repeated — $10^5 - P(10,5) = 69\,760$
- All digits different — $P(10,5) = 30\,240$
