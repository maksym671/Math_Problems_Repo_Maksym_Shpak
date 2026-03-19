# Solution

## Task 1 — Recognizing Counting Models

Before solving a counting problem, we answer four questions:

1. Are we using **all** objects or only **some**?
2. Does **order** matter?
3. Is **repetition** allowed?
4. Are some objects **identical**?

The answers determine which formula to use.

---

# 1. Arranging 7 students in a line

**Situation:** We place all 7 students in a row (e.g. in front of the blackboard).

**Analysis:**

- We use **all 7** students — no one is left out
- **Order matters** — the sequence (Anna, Bob, …) is different from (Bob, Anna, …)
- No repetition — each student appears exactly once
- All students are **distinguishable** — we treat each person as unique

**Model: permutation**

We count all linear arrangements of 7 distinct objects:

$$
P_7 = 7! = 7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 5\,040
$$

---

# 2. Choosing 4 members of a committee from 12 people

**Situation:** We select 4 people to form a committee.

**Analysis:**

- We choose only **some** (4 out of 12)
- **Order does not matter** — the committee $\{A, B, C, D\}$ is the same as $\{D, C, B, A\}$
- No repetition — each person is chosen at most once
- People are distinguishable

**Model: combination**

$$
\binom{12}{4} = \frac{12!}{4! \cdot 8!} = \frac{12 \cdot 11 \cdot 10 \cdot 9}{4 \cdot 3 \cdot 2 \cdot 1} = 495
$$

---

# 3. Assigning gold, silver, and bronze medals among 15 athletes

**Situation:** We award 3 different medals to 3 different athletes.

**Analysis:**

- We choose only **some** (3 out of 15)
- **Order matters** — gold, silver, bronze are distinct; (Alice gets gold, Bob silver) $\neq$ (Bob gets gold, Alice silver)
- No repetition — each athlete receives at most one medal
- Athletes are distinguishable

**Model: k-permutation** (ordered selection without repetition)

$$
P(15,3) = \frac{15!}{12!} = 15 \cdot 14 \cdot 13 = 2\,730
$$

---

# 4. Forming a 6-digit PIN code

**Situation:** A PIN has 6 positions, each a digit from 0 to 9.

**Analysis:**

- We fill 6 **positions**
- **Order matters** — 123456 and 654321 are different codes
- **Repetition is allowed** — the same digit can appear several times (e.g. 111111)
- Each position is chosen independently from $0$–$9$

**Model: sequence with repetition**

$$
10^6 = 1\,000\,000
$$

---

# 5. Arranging the letters of the word BANANA

**Situation:** We form different “words” by rearranging all letters of BANANA.

**Analysis:**

- We use **all** letters
- **Order matters** — BANANA and ANANAB are different arrangements
- **Some letters are identical** — there are 3 A’s, 2 N’s, 1 B
- Indistinguishable copies of the same letter are not distinguished

**Model: permutation with repeated elements**

Letter counts: $n_A = 3$, $n_N = 2$, $n_B = 1$. Total: $6$ letters.

$$
\frac{6!}{3! \cdot 2! \cdot 1!} = \frac{720}{6 \cdot 2 \cdot 1} = 60
$$

**Why we divide:** Swapping two A’s gives the same arrangement, so we divide by $3!$ to avoid overcounting. Similarly for N’s and B.

---

# 6. Seating 6 people around a round table

**Situation:** We seat 6 people around a circular table. Rotations count as the same arrangement.

**Analysis:**

- We use **all 6** people
- **Order matters** for relative positions (who sits next to whom)
- Arranged **in a circle** — rotating everyone does not create a new seating
- People are distinguishable

**Model: circular permutation**

Fix one person to eliminate rotations; arrange the remaining 5 in order:

$$
(6-1)! = 5! = 120
$$

---

# Summary

- 7 students in a line — Permutation: $7!$
- 4 committee members from 12 — Combination: $\binom{12}{4}$
- Gold, silver, bronze medals — k-permutation: $P(15,3)$
- 6-digit PIN code — Sequence with repetition: $10^6$
- Letters of BANANA — Permutation with repeated elements: $\frac{6!}{3! \cdot 2! \cdot 1!}$
- 6 people around round table — Circular permutation: $5!$
