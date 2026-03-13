# Solution

## Task 6

**Given:** Two machines put identical products on one conveyor. Production ratio first : second = $3:2$, so a randomly chosen product comes from machine 1 with probability $\frac{3}{5}$ and from machine 2 with probability $\frac{2}{5}$. Machine 1 produces 65% first-grade; machine 2 produces 85% first-grade.

Let $M_1$ = “product from machine 1”, $M_2$ = “product from machine 2”, and $F$ = “first-grade product”. Then

$$
P(M_1) = \frac{3}{5}, \quad P(M_2) = \frac{2}{5}, \quad P(F \mid M_1) = 0.65, \quad P(F \mid M_2) = 0.85.
$$

---

**1. Probability that a randomly selected product is first-grade (total probability formula)**

$$
P(F) = P(M_1)\,P(F \mid M_1) + P(M_2)\,P(F \mid M_2) = \frac{3}{5}\cdot 0.65 + \frac{2}{5}\cdot 0.85.
$$

$$
P(F) = 0.39 + 0.34 = 0.73.
$$

**Answer 1:** $P(F) = 0.73$ (73%).

---

**2. Given that the product is first-grade, probability it was produced by the first machine (Bayes’ theorem)**

$$
P(M_1 \mid F) = \frac{P(M_1)\,P(F \mid M_1)}{P(F)} = \frac{\frac{3}{5}\cdot 0.65}{0.73} = \frac{0.39}{0.73} = \frac{39}{73} \approx 0.534.
$$

**Answer 2:** $P(M_1 \mid F) = \frac{39}{73} \approx 0.534$ (about 53.4%).
