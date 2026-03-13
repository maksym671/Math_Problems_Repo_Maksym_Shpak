# Solution

## Task 10

**Given:** Three sequences are sent: **AAAA** (prob. $0.4$), **BBBB** ($0.3$), **CCCC** ($0.3$). Each letter is distorted independently according to the table (rows = transmitted, columns = received):

| Transmitted \ Received | A   | B   | C   |
| :---                   | :---| :---| :---|
| **A**                  | 0.8 | 0.1 | 0.1 |
| **B**                  | 0.1 | 0.8 | 0.1 |
| **C**                  | 0.1 | 0.1 | 0.8 |

**Find:** (1) $P(\text{received } AAAA)$, (2) $P(\text{received } ACAA)$.

We use the **total probability formula** over the three hypotheses “sent AAAA”, “sent BBBB”, “sent CCCC”. For each received 4-letter word we multiply the per-symbol probabilities (independence).

---

**1. $P(\text{received } AAAA)$**

- Sent **AAAA**: all four A’s received as A $\Rightarrow$ $0.8^4 = 0.4096$.
- Sent **BBBB**: all four B’s received as A $\Rightarrow$ $0.1^4 = 0.0001$.
- Sent **CCCC**: all four C’s received as A $\Rightarrow$ $0.1^4 = 0.0001$.

$$
P(\text{AAAA}) = 0.4\cdot 0.4096 + 0.3\cdot 0.0001 + 0.3\cdot 0.0001 = 0.16384 + 0.00006 = 0.1639.
$$

**Answer 1:** $0.1639$ (about 16.4%).

---

**2. $P(\text{received } ACAA)$**

We need positions 1–4 to be A, C, A, A.

- Sent **AAAA**: A→A (0.8), A→C (0.1), A→A (0.8), A→A (0.8) $\Rightarrow$ $0.8\cdot 0.1\cdot 0.8\cdot 0.8 = 0.0512$.
- Sent **BBBB**: each B→A or B→C with prob. 0.1 $\Rightarrow$ $0.1^4 = 0.0001$.
- Sent **CCCC**: C→A (0.1), C→C (0.8), C→A (0.1), C→A (0.1) $\Rightarrow$ $0.1\cdot 0.8\cdot 0.1\cdot 0.1 = 0.0008$.

$$
P(\text{ACAA}) = 0.4\cdot 0.0512 + 0.3\cdot 0.0001 + 0.3\cdot 0.0008 = 0.02048 + 0.00003 + 0.00024 = 0.02075.
$$

**Answer 2:** $0.02075$ (about 2.08%).
