# Solution

## Task 2 — Permutations

A **permutation** is an arrangement of **all** objects in a **line**, where **order matters**. For $n$ distinct objects, the number of permutations is $n!$.

---

# 1. Arranging 8 different books on a shelf

**Problem:** In how many ways can 8 different books be placed on a shelf?

**Reasoning:** Each placement is a linear ordering of 8 distinct books. Position 1: 8 choices; position 2: 7 remaining; …; position 8: 1 remaining.

$$
8! = 8 \cdot 7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 40\,320
$$

**Answer:** 40,320 arrangements.

---

# 2. Eight people in a row — two particular people must sit next to each other

**Problem:** 8 people sit in a row; two specific people (say A and B) must sit next to each other.

**Strategy:** Treat A and B as a **single block**. We arrange 7 objects: the block + 6 other people.

- Arrange these 7 objects: $7!$ ways
- Within the block, A and B can sit as (A,B) or (B,A): $2!$ ways

$$
7! \cdot 2! = 5\,040 \cdot 2 = 10\,080
$$

**Answer:** 10,080 arrangements.

---

# 3. Eight people in a row — those two people must NOT sit next to each other

**Problem:** Same 8 people, but now A and B must **not** sit together.

**Strategy:** Use the **complement** — subtract arrangements where A and B sit together from the total.

- Total arrangements (no restriction): $8! = 40\,320$
- Arrangements where A and B sit together: $10\,080$ (from part 2)

$$
8! - 7! \cdot 2! = 40\,320 - 10\,080 = 30\,240
$$

**Answer:** 30,240 arrangements.

---

# 4. Ordering 10 questions — first question is fixed

**Problem:** 10 exam questions; the first one is fixed; we order the remaining 9.

**Reasoning:** Only the last 9 positions are free. We permute 9 distinct questions.

$$
9! = 362\,880
$$

**Answer:** 362,880 orderings.

---

# Summary

- 8 books on shelf — $8! = 40\,320$
- 8 people, 2 together — $7! \cdot 2! = 10\,080$
- 8 people, 2 apart — $8! - 7! \cdot 2! = 30\,240$
- 10 questions, 1st fixed — $9! = 362\,880$
