# Solution

## Task 12 — Mixed Counting Problem

This task combines several counting models. For each part we identify the **model** and compute the **number of outcomes**.

---

# 1. Student ID Codes

Identifiers: 2 letters from $\{A,B,C,D,E\}$ followed by 3 digits from $0$–$9$.

### (1) Letters and digits may repeat

**Model:** Sequence with repetition (product rule).

- 2 letters: $5 \cdot 5 = 25$
- 3 digits: $10^3 = 1\,000$

$$
5^2 \cdot 10^3 = 25\,000
$$

### (2) Letters may not repeat, digits may repeat

**Model:** k-permutation for letters; sequence for digits.

- 2 letters: $P(5,2) = 20$
- 3 digits: $10^3 = 1\,000$

$$
20 \cdot 1\,000 = 20\,000
$$

### (3) Neither letters nor digits may repeat

**Model:** k-permutation for both.

- 2 letters: $P(5,2) = 20$
- 3 digits: $P(10,3) = 720$

$$
20 \cdot 720 = 14\,400
$$

---

# 2. Medal Assignment

12 runners; gold, silver, bronze medals.

### (1) In how many ways can medals be assigned?

**Model:** k-permutation — assign 3 distinct medals to 3 different runners; order matters.

$$
P(12,3) = 12 \cdot 11 \cdot 10 = 1\,320
$$

### (2) Two particular runners must both receive medals

**Strategy:** Choose which 2 medals go to these 2 runners: $\binom{3}{2} = 3$. Assign those 2 medals to the 2 runners: $2! = 2$. Assign the remaining medal to one of 10 others: $10$.

$$
3 \cdot 2 \cdot 10 = 60
$$

---

# 3. Committee Selection

4 people from 10 students (6 men, 4 women).

### (1) Total committees

**Model:** Combination — $\binom{10}{4} = 210$

### (2) Exactly two women

Choose 2 women from 4 and 2 men from 6:

$$
\binom{4}{2} \cdot \binom{6}{2} = 6 \cdot 15 = 90
$$

### (3) At least one woman

**Complement:** total minus committees with no women (all men):

$$
\binom{10}{4} - \binom{6}{4} = 210 - 15 = 195
$$

---

# 4. Circular Seating

Seven people around a round table.

### (1) Total arrangements

**Model:** Circular permutation — $(7-1)! = 6! = 720$

### (2) Two particular people sit next to each other

Treat the two as one block. Arrange block + 5 others in a circle: $5!$. Within block: $2!$.

$$
5! \cdot 2! = 240
$$

---

# 5. Passwords

5 characters from digits $0$–$9$ ($10$) and letters $A$–$Z$ ($26$). Total: $36$ characters.

### (1) Repetition allowed

**Model:** Sequence with repetition — $36^5 = 60\,466\,176$

### (2) No character may repeat

**Model:** k-permutation — $P(36,5) = 45\,239\,040$

### (3) Models used

- With repetition: **sequence with repetition** ($n^k$)
- Without repetition: **k-permutation** ($P(n,k)$)
