# Solution

## Task 7

**Given:** Two code words are sent: **111** with probability $0.65$ and **000** with probability $0.35$. Each symbol is distorted independently: 1 is received as 0 with probability $0.2$, and 0 is received as 1 with probability $0.2$. So correct transmission has probability $0.8$ for each symbol.

**Find:** Probability of receiving (1) 111, (2) 000, (3) 010.

We use the **total probability formula** over the two hypotheses “sent 111” and “sent 000”. For each received word, we multiply symbol-wise probabilities (independence).

---

**1. $P(\text{received } 111)$**

- If sent **111**: all three symbols correct $\Rightarrow$ $0.8^3 = 0.512$.
- If sent **000**: all three received as 1 $\Rightarrow$ $0.2^3 = 0.008$.

$$
P(\text{111}) = 0.65\cdot 0.512 + 0.35\cdot 0.008 = 0.3328 + 0.0028 = 0.3356.
$$

**Answer 1:** $0.3356$.

---

**2. $P(\text{received } 000)$**

- If sent **111**: all three 1’s received as 0 $\Rightarrow$ $0.2^3 = 0.008$.
- If sent **000**: all three correct $\Rightarrow$ $0.8^3 = 0.512$.

$$
P(\text{000}) = 0.65\cdot 0.008 + 0.35\cdot 0.512 = 0.0052 + 0.1792 = 0.1844.
$$

**Answer 2:** $0.1844$.

---

**3. $P(\text{received } 010)$**

- If sent **111** (positions 1,2,3): we need 0, 1, 0 $\Rightarrow$ $0.2 \cdot 0.8 \cdot 0.2 = 0.032$.
- If sent **000**: we need 0, 1, 0 $\Rightarrow$ $0.8 \cdot 0.2 \cdot 0.8 = 0.128$.

$$
P(\text{010}) = 0.65\cdot 0.032 + 0.35\cdot 0.128 = 0.0208 + 0.0448 = 0.0656.
$$

**Answer 3:** $0.0656$.
