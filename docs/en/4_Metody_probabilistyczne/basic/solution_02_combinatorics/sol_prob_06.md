# Solution

## Task 6 — Combinations in Card Problems

A standard deck has **52 cards**: 4 suits (hearts ♥, diamonds ♦, clubs ♣, spades ♠), 13 ranks per suit (A, 2–10, J, Q, K). Hearts: 13 cards. When we draw cards **without replacement** and **order does not matter**, we use **combinations**.

---

# 1. 5-card hand with exactly 2 hearts

**Problem:** How many 5-card hands contain **exactly 2 hearts**?

**Strategy:** Choose 2 hearts from 13 and 3 non-hearts from the remaining 39. Order does not matter (a hand is a set of cards).

$$
\binom{13}{2} \cdot \binom{39}{3} = 78 \cdot 9\,139 = 712\,842
$$

**Answer:** 712,842 hands with exactly 2 hearts.

---

# 2. 5-card hand with at least one heart

**Problem:** How many 5-card hands contain **at least one** heart?

**Strategy:** Use the **complement** — total hands minus hands with **no** hearts.

- Total 5-card hands: $\binom{52}{5} = 2\,598\,960$
- Hands with no hearts: choose all 5 from 39 non-hearts: $\binom{39}{5} = 575\,757$

$$
2\,598\,960 - 575\,757 = 2\,023\,203
$$

**Answer:** 2,023,203 hands contain at least one heart.

---

# 3. 5-card hand with no face cards (J, Q, K)

**Problem:** How many 5-card hands have **no face cards**?

**Reasoning:** There are 12 face cards (J, Q, K in each of 4 suits). Non-face cards: $52 - 12 = 40$. We choose 5 from these 40.

$$
\binom{40}{5} = 658\,008
$$

**Answer:** 658,008 hands with no face cards.

---

# Summary

- Exactly 2 hearts — $\binom{13}{2}\binom{39}{3} = 712\,842$
- At least one heart — $\binom{52}{5} - \binom{39}{5} = 2\,023\,203$
- No face cards — $\binom{40}{5} = 658\,008$
