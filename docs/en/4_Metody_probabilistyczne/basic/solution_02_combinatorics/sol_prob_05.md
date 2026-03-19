# Solution

## Task 5 — Combinations

A **combination** is a selection of objects where **order does not matter**. Choosing $k$ from $n$ distinct objects:

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

---

# 1. Committee of 4 from 12 students

**Problem:** How many committees of 4 people can be formed from 12 students?

**Reasoning:** A committee is a **set** — the order of selection does not matter. We choose 4 from 12 without repetition.

$$
\binom{12}{4} = \frac{12!}{4! \cdot 8!} = \frac{12 \cdot 11 \cdot 10 \cdot 9}{4 \cdot 3 \cdot 2 \cdot 1} = 495
$$

**Answer:** 495 committees.

---

# 2. Committees that contain a particular student

**Problem:** How many committees include a specific student (e.g. Anna)?

**Strategy:** Anna is fixed. We choose the remaining **3** members from the other **11** students.

$$
\binom{11}{3} = \frac{11 \cdot 10 \cdot 9}{3 \cdot 2 \cdot 1} = 165
$$

**Answer:** 165 committees contain Anna.

---

# 3. Committees that contain at least one of two particular students

**Problem:** How many committees include **at least one** of two specific students (Anna or Bob)?

**Strategy:** Use the **complement**: total committees minus committees that contain **neither** Anna nor Bob.

- Total committees: $\binom{12}{4} = 495$
- Committees with neither: choose all 4 from the other 10: $\binom{10}{4} = 210$

$$
495 - 210 = 285
$$

**Answer:** 285 committees contain at least one of the two.

---

# 4. Committees with exactly two women (7 men, 5 women)

**Problem:** The group has 7 men and 5 women. How many committees of 4 have **exactly 2 women**?

**Strategy:** Choose 2 women from 5 and 2 men from 7. By the product rule:

$$
\binom{5}{2} \cdot \binom{7}{2} = \frac{5 \cdot 4}{2} \cdot \frac{7 \cdot 6}{2} = 10 \cdot 21 = 210
$$

**Answer:** 210 committees with exactly two women.

---

# Summary

- 4 from 12 — $\binom{12}{4} = 495$
- Include one specific student — $\binom{11}{3} = 165$
- At least one of two students — $\binom{12}{4} - \binom{10}{4} = 285$
- Exactly 2 women — $\binom{5}{2}\binom{7}{2} = 210$
