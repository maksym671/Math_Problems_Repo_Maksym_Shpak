# Solution

## Task 2

**Given:** Circuit with element $a_1$ in **series** with a block in which $a_2$ and $a_3$ are in **parallel**. $A_i$ denotes the event “element $a_i$ is functional at time $t$”.

**Find:** Event $A$ — “current flow through the circuit will not be interrupted” — expressed using $\cup$ and $\cap$ on the events $A_i$.

---

**Reasoning:**

- **Series:** Current flows only if **every** element in the series works. So the path through $a_1$ allows current if $A_1$ occurs.
- **Parallel:** Current flows if **at least one** of the parallel elements works. So the block $\{a_2, a_3\}$ allows current if $A_2 \cup A_3$ occurs.
- The whole circuit allows current if the series part works **and** the parallel block works. So we need $A_1$ **and** ($A_2$ or $A_3$).

**Answer:**

$$
A = A_1 \cap (A_2 \cup A_3).
$$

That is: “$a_1$ is functional and at least one of $a_2$, $a_3$ is functional at time $t$”.
