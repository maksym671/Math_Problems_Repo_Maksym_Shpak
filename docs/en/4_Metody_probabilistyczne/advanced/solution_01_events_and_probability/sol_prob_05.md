# Solution

## Task 5

**Given:** Water volume (dm³/s) in a concrete culvert. Events: $A$ = “volume in $\langle 125, 250 \rangle$”, $B$ = “volume in $(200, 300\rangle$”. We have $P(A) = 0.6$, $P(B) = 0.7$, $P(A \cup B) = 0.8$.

**Find:**

1. $P(A')$
2. $P(A \cap B)$
3. $P(A' \cap B')$

---

**1. $P(A')$ (complement of $A$)**

$$
P(A') = 1 - P(A) = 1 - 0.6 = 0.4.
$$

---

**2. $P(A \cap B)$ (intersection)**

From the identity $P(A \cup B) = P(A) + P(B) - P(A \cap B)$ we get

$$
P(A \cap B) = P(A) + P(B) - P(A \cup B) = 0.6 + 0.7 - 0.8 = 0.5.
$$

(So the volume lies in the intersection of the intervals, i.e. in $(200, 250\rangle$, with probability $0.5$.)

---

**3. $P(A' \cap B')$ (volume in neither interval)**

By de Morgan’s law, $A' \cap B' = (A \cup B)'$. Hence

$$
P(A' \cap B') = P\bigl((A \cup B)'\bigr) = 1 - P(A \cup B) = 1 - 0.8 = 0.2.
$$

**Summary**

| Quantity      | Result |
|---------------|--------|
| $P(A')$       | $0.4$  |
| $P(A \cap B)$ | $0.5$  |
| $P(A' \cap B')$ | $0.2$  |
