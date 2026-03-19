# Solution

## Task 11 — Modeling Outcomes

The number of outcomes in a counting or probability problem depends on **how we record** the results: distinguishable vs indistinguishable objects, and whether **order** is recorded or ignored.

---

# 1. Distinguishable vs Indistinguishable Objects

A box contains 4 red, 4 blue, 3 green balls (11 total).

### (1) Linear arrangements — balls of same color indistinguishable

**Problem:** How many linear arrangements of all 11 balls if balls of the same color are treated as **indistinguishable**?

**Reasoning:** We arrange 11 positions with 4 R’s, 4 B’s, 3 G’s. Permutation with repeated elements:

$$
\frac{11!}{4! \cdot 4! \cdot 3!} = 11\,550
$$

### (2) Linear arrangements — every ball individually labeled

**Problem:** How many arrangements if every ball is **individually labeled** (e.g. $R_1, R_2, R_3, R_4, B_1, \ldots$)?

**Reasoning:** We arrange 11 distinct objects:

$$
11! = 39\,916\,800
$$

### (3) Why the answers differ

When balls are **indistinguishable** by color, swapping two red balls does not create a new arrangement. When balls are **labeled**, each swap gives a different arrangement. So we overcount by $4! \cdot 4! \cdot 3!$ when treating all balls as distinct; dividing by this factor gives the count for indistinguishable-by-color arrangements.

---

# 2. Recording Order vs Ignoring Order

Three balls are drawn **without replacement** from the same box.

### (1) Only the set of colors recorded (order ignored)

**Problem:** How many outcomes if we record only **which colors** appear (e.g. $\{R, B, G\}$ or $\{R, R, B\}$)?

**Reasoning:** We count combinations of 3 colors from $\{R, B, G\}$ with repetition allowed (stars and bars):

$$
\binom{3+3-1}{3} = \binom{5}{3} = 10
$$

### (2) Sequence of colors recorded

**Problem:** How many outcomes if we record the **order** of colors (e.g. $(R, B, R)$)?

**Reasoning:** Each of 3 positions is one of R, B, G. All 27 sequences are possible:

$$
3^3 = 27
$$

### (3) Why recording order changes the model

When we **ignore order**, the outcome is a multiset (e.g. “2 red, 1 blue”). When we **record order**, the outcome is a sequence (e.g. R, B, R vs R, R, B). Each unordered outcome can arise from several ordered draws, so there are fewer unordered than ordered outcomes.

---

# 3. PIN Code vs Number

### (1) 4-digit PIN codes (repetition allowed)

**Problem:** How many 4-digit PIN codes? Each position: digits $0$–$9$.

$$
10^4 = 10\,000
$$

### (2) 4-digit numbers (first digit cannot be 0)

**Problem:** How many 4-digit numbers? First digit: $1$–$9$; remaining: $0$–$9$.

$$
9 \cdot 10^3 = 9\,000
$$

### (3) Why PIN and number are counted differently

A **PIN code** can start with 0 (e.g. 0123). A **4-digit number** has no leading zeros, so the first digit is restricted to $1$–$9$. The sample spaces differ.

### (4) Why 1234 and 4321 are different outcomes

Order matters: 1234 and 4321 are different sequences. In probability, each is a distinct elementary outcome.
