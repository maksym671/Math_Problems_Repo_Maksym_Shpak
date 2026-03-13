# Solution

## Task 4

**Given:** Two elements $a_1$ and $a_2$ are connected in **parallel**. $A_i$ = “element $a_i$ remains functional for at least time $t$”. We have $P(A_1) = P(A_2) = p$ and $P(A_1 \cap A_2) = p^2$.

**Find:** Probability of **continuous current flow** through the system for at least time $t$.

---

**Reasoning:**

In a **parallel** connection, current flows if **at least one** element is functional. So the event “current flows for at least time $t$” is

$$
A_1 \cup A_2.
$$

We use the formula for the probability of the union of two events:

$$
P(A_1 \cup A_2) = P(A_1) + P(A_2) - P(A_1 \cap A_2).
$$

Substituting $P(A_1) = P(A_2) = p$ and $P(A_1 \cap A_2) = p^2$:

$$
P(A_1 \cup A_2) = p + p - p^2 = 2p - p^2 = p(2 - p).
$$

**Answer:**

$$
\boxed{P(\text{continuous current}) = P(A_1 \cup A_2) = 2p - p^2 = p(2 - p).}
$$
