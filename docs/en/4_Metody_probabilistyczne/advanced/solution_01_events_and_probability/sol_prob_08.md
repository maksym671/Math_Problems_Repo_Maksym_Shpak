# Solution

## Task 8

**Given:** Seven pulses in a random order: **4** of type $A$, **2** of type $B$, **1** of type $C$. All orderings are equally likely.

**Find:**

1. $P(\text{first pulse} = A)$
2. $P(\text{first pulse} = A \text{ or } C)$
3. $P(\text{first} = A \text{ and second} = C)$ (in that order)

---

**1. First received pulse is $A$**

There are 4 pulses of type $A$ out of 7. Under random arrangement, the first position is equally likely to be any of the 7 pulses, so

$$
P(\text{1st} = A) = \frac{4}{7}.
$$

---

**2. First received pulse is $A$ or $C$**

Favourable outcomes for the first position: any of the 4 type-$A$ or the 1 type-$C$ pulse, i.e. 5 out of 7:

$$
P(\text{1st} = A \cup C) = \frac{4 + 1}{7} = \frac{5}{7}.
$$

---

**3. First two pulses are $A$ then $C$ (in that order)**

$$
P(\text{1st} = A,\, \text{2nd} = C) = P(\text{1st} = A)\cdot P(\text{2nd} = C \mid \text{1st} = A).
$$

We have $P(\text{1st} = A) = \frac{4}{7}$. Given the first is $A$, 6 pulses remain (3 $A$, 2 $B$, 1 $C$), so $P(\text{2nd} = C \mid \text{1st} = A) = \frac{1}{6}$. Hence

$$
P(\text{1st} = A,\, \text{2nd} = C) = \frac{4}{7} \cdot \frac{1}{6} = \frac{4}{42} = \frac{2}{21}.
$$

**Summary**

| Event              | Probability   |
|--------------------|---------------|
| 1st = $A$          | $\frac{4}{7}$ |
| 1st = $A$ or $C$   | $\frac{5}{7}$ |
| 1st = $A$, 2nd = $C$ | $\frac{2}{21}$ |
