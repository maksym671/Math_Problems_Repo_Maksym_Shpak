# Solution

## Task 9

**Given:** A good is produced by **3 plants**. One item is taken from each plant (3 items in total). The probability that an item from plant $i$ is first-quality is $0.97$, $0.90$, and $0.86$ for $i = 1, 2, 3$ respectively.

**Find:** The probability that a **randomly chosen** one of these three items (one from each plant) is first-quality.

---

**Reasoning:** The chosen item is equally likely to come from any of the three plants, so $P(\text{from plant } i) = \frac{1}{3}$ for $i = 1, 2, 3$. By the **total probability formula**:

$$
P(\text{first quality}) = \sum_{i=1}^{3} P(\text{from plant } i)\cdot P(\text{first quality} \mid \text{from plant } i).
$$

With $p_1 = 0.97$, $p_2 = 0.90$, $p_3 = 0.86$:

$$
P(\text{first quality}) = \frac{1}{3}\cdot 0.97 + \frac{1}{3}\cdot 0.90 + \frac{1}{3}\cdot 0.86 = \frac{1}{3}(0.97 + 0.90 + 0.86) = \frac{2.73}{3} = 0.91.
$$

**Answer:**

$$
\boxed{P(\text{first quality}) = 0.91 \;\text{(91\%)}.}
$$
