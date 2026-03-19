# Solution

## Task 3 — Permutations with Repeated Elements

When some objects are **identical**, simply using $n!$ overcounts: swapping two identical items gives the same arrangement. We divide by the factorials of the repetition counts.

**Formula:** For $n$ objects with $n_1$ of type 1, $n_2$ of type 2, …, $n_r$ of type $r$ (where $n_1 + n_2 + \cdots + n_r = n$):

$$
\frac{n!}{n_1! \, n_2! \, \cdots \, n_r!}
$$

---

# 1. Arrangements of MISSISSIPPI

**Problem:** How many distinct arrangements of the letters in MISSISSIPPI?

**Step 1 — Count letters:** M: $1$, I: $4$, S: $4$, P: $2$. Total: $11$ letters.

**Step 2 — Apply formula:**

$$
\frac{11!}{1! \cdot 4! \cdot 4! \cdot 2!} = \frac{39\,916\,800}{24 \cdot 24 \cdot 2} = 34\,650
$$

**Interpretation:** There are 34,650 distinguishable “words” formed by rearranging the letters of MISSISSIPPI (including the original spelling).

---

# 2. Arrangements of STATISTICS

**Problem:** How many distinct arrangements of STATISTICS?

**Step 1 — Count letters:** S: $3$, T: $3$, A: $1$, I: $2$, C: $1$. Total: $10$ letters.

**Step 2 — Apply formula:**

$$
\frac{10!}{3! \cdot 3! \cdot 1! \cdot 2! \cdot 1!} = \frac{3\,628\,800}{6 \cdot 6 \cdot 2} = 50\,400
$$

**Answer:** 50,400 arrangements.

---

# 3. Arrangements of STATISTICS that start with S

**Problem:** How many of these arrangements begin with the letter S?

**Strategy:** Fix the first position as S. Count arrangements of the **remaining 9 letters**.

**Remaining letters:** One S is used, so we have S: $2$, T: $3$, A: $1$, I: $2$, C: $1$.

$$
\frac{9!}{2! \cdot 3! \cdot 1! \cdot 2! \cdot 1!} = \frac{362\,880}{2 \cdot 6 \cdot 2} = 15\,120
$$

**Answer:** 15,120 arrangements start with S.

---

# Summary

- MISSISSIPPI — $\frac{11!}{1!4!4!2!} = 34\,650$
- STATISTICS — $\frac{10!}{3!3!1!2!1!} = 50\,400$
- STATISTICS (starts with S) — $\frac{9!}{2!3!1!2!1!} = 15\,120$
