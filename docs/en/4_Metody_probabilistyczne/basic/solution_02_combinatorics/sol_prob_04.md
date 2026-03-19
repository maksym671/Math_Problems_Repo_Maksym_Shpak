# Solution

## Task 4 — Circular Permutations

For objects arranged **in a circle**, rotations do not change the arrangement (e.g. shifting everyone one seat to the right gives the same seating). We fix one object to eliminate rotations and permute the rest.

**Formula:** For $n$ distinct objects around a circle:

$$
(n-1)!
$$

---

# 1. Seven people around a round table

**Problem:** In how many ways can 7 people sit around a round table?

**Reasoning:** Fix one person. The other 6 can be arranged in $6!$ ways. Each arrangement corresponds to a unique seating (up to rotation).

$$
(7-1)! = 6! = 720
$$

**Answer:** 720 seating arrangements.

---

# 2. Seven people — two particular people must sit next to each other

**Problem:** Same 7 people; two specific people (A and B) must sit **next to each other**.

**Strategy:** Treat A and B as one block. We arrange 6 objects around the table: the block + 5 others.

- Circular arrangements of these 6: $(6-1)! = 5!$
- Within the block, A and B can swap: $2!$ ways

$$
5! \cdot 2! = 120 \cdot 2 = 240
$$

**Answer:** 240 arrangements.

---

# 3. Seven people — two particular people must sit opposite each other

**Problem:** A and B must sit **opposite** each other (facing across the table).

**Strategy:** Fix person A in one seat. Person B has exactly **one** opposite seat. The remaining 5 people fill the other 5 seats in $5!$ ways.

$$
5! = 120
$$

**Answer:** 120 arrangements.

---

# Summary

- No restriction — $(7-1)! = 720$
- Two sit together — $5! \cdot 2! = 240$
- Two sit opposite — $5! = 120$
