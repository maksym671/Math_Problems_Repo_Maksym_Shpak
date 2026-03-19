# Solution

## Task 10 — Urn Models

An urn contains 5 red, 4 blue, and 3 green balls. Total: 12 balls. We draw 3 balls **without replacement**. The number of outcomes depends on whether we record **order** or only the **set** of colors.

---

# 1. Three balls drawn without replacement, order ignored

**Problem:** How many different **samples** (sets of 3 balls) are possible?

**Reasoning:** We choose 3 balls from 12; order does not matter. This is a combination.

$$
\binom{12}{3} = \frac{12 \cdot 11 \cdot 10}{3 \cdot 2 \cdot 1} = 220
$$

**Answer:** 220 different samples.

---

# 2. Such samples with exactly two red balls

**Problem:** How many samples contain **exactly 2 red** balls?

**Strategy:** Choose 2 red from 5 and 1 non-red from 7 (4 blue + 3 green).

$$
\binom{5}{2} \cdot \binom{7}{1} = 10 \cdot 7 = 70
$$

**Answer:** 70 samples with exactly 2 red balls.

---

# 3. Three balls drawn, order of colors recorded

**Problem:** We draw 3 balls and record the **sequence** of colors (e.g. R, B, R). How many outcomes?

**Reasoning:** Each outcome is an ordered triple of colors from $\{R, B, G\}$. With 5 red, 4 blue, 3 green, every such triple is possible (e.g. RRR, BBB, GGG).

$$
3^3 = 27
$$

**Answer:** 27 ordered color sequences.

---

# 4. Such outcomes with exactly two red balls

**Problem:** How many ordered color sequences have **exactly 2 red**?

**Strategy:** We need sequences of length 3 with exactly 2 R and 1 other color.

- 2 R, 1 B: permutations of $(R,R,B)$ $\Rightarrow$ $\frac{3!}{2! \cdot 1!} = 3$
- 2 R, 1 G: permutations of $(R,R,G)$ $\Rightarrow$ $3$

$$
3 + 3 = 6
$$

**Answer:** 6 ordered sequences with exactly 2 red balls.

---

# Summary

- 3 balls, order ignored — $\binom{12}{3} = 220$
- Exactly 2 red, order ignored — $\binom{5}{2} \binom{7}{1} = 70$
- Order of colors recorded — $3^3 = 27$
- Exactly 2 red, order recorded — $6$
