# Solution

## Task 9 — Digit Restrictions

A **5-digit number** has no leading zero — the first digit is from $1$ to $9$. The remaining positions can be $0$–$9$ unless further restrictions apply.

---

# 1. Total number of 5-digit numbers

**Problem:** How many 5-digit numbers exist?

**Reasoning:**

- First digit: 9 choices ($1$–$9$)
- Digits 2–5: each has 10 choices ($0$–$9$)

$$
9 \cdot 10^4 = 90\,000
$$

**Answer:** 90,000 five-digit numbers.

---

# 2. Even 5-digit numbers

**Problem:** How many 5-digit numbers are **even**?

**Reasoning:** The last digit must be 0, 2, 4, 6, or 8 — 5 choices.

- First digit: 9 choices ($1$–$9$)
- Middle three: $10^3$ each
- Last digit: 5 choices (even)

$$
9 \cdot 10^3 \cdot 5 = 45\,000
$$

**Answer:** 45,000 even five-digit numbers.

---

# 3. 5-digit numbers with no repeated digits

**Problem:** How many 5-digit numbers have **all different digits**?

**Reasoning:**

- First digit: 9 choices ($1$–$9$)
- Second: 9 choices ($0$–$9$ excluding the first)
- Third: 8 choices
- Fourth: 7 choices
- Fifth: 6 choices

$$
9 \cdot 9 \cdot 8 \cdot 7 \cdot 6 = 27\,216
$$

**Answer:** 27,216 numbers with no repeated digits.

---

# 4. 5-digit numbers with at least one repeated digit

**Problem:** How many 5-digit numbers have **at least one** repeated digit?

**Strategy:** Use the **complement** — all 5-digit numbers minus those with all digits different.

$$
90\,000 - 27\,216 = 62\,784
$$

**Answer:** 62,784 numbers with at least one repeated digit.

---

# Summary

- All 5-digit — $9 \cdot 10^4 = 90\,000$
- Even — $9 \cdot 10^3 \cdot 5 = 45\,000$
- No repeated digits — $9 \cdot 9 \cdot 8 \cdot 7 \cdot 6 = 27\,216$
- At least one repeated — $90\,000 - 27\,216 = 62\,784$
