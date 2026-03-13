# Solution

## Task 3

**Given:** Person $X$ completes a job in **4, 5, or 6 hours** and may commit **0, 1, or 2 errors**. The 9 elementary events (time, number of errors) are **equally likely**, so $P(\omega) = \frac{1}{9}$ for each.

Sample space (e.g. time first, errors second):

$$
\Omega = \{(4,0),(4,1),(4,2),\, (5,0),(5,1),(5,2),\, (6,0),(6,1),(6,2)\}.
$$

**Find the probabilities:**

---

**1. Job completed in 4 hours**

Favourable outcomes: $(4,0)$, $(4,1)$, $(4,2)$ — three outcomes.

$$
P(\text{4 hours}) = \frac{3}{9} = \frac{1}{3}.
$$

---

**2. Job completed flawlessly in 6 hours**

Favourable outcome: $(6,0)$ only — one outcome.

$$
P(\text{6 hours, 0 errors}) = \frac{1}{9}.
$$

---

**3. Job completed in at most 5 hours**

“At most 5” means 4 or 5 hours (any number of errors). Favourable: $(4,0)$, $(4,1)$, $(4,2)$, $(5,0)$, $(5,1)$, $(5,2)$ — six outcomes.

$$
P(\text{at most 5 hours}) = \frac{6}{9} = \frac{2}{3}.
$$

---

**4. At most 5 hours and at most one error**

Favourable: time $\in \{4,5\}$ and errors $\in \{0,1\}$: $(4,0)$, $(4,1)$, $(5,0)$, $(5,1)$ — four outcomes.

$$
P(\text{at most 5 hours} \cap \text{at most 1 error}) = \frac{4}{9}.
$$
