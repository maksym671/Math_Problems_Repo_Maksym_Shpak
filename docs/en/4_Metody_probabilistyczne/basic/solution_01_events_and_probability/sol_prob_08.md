# Solution

## Task 8 — Events and Probabilities in Card Drawing

We consider a standard 52‑card deck (13 ranks in each of 4 suits: hearts, diamonds, clubs, spades).  
The deck is well‑shuffled, and each ordered sequence of draws (with the given replacement rule) is equally likely.

### Basic counts

- Total cards: $52$.
- Hearts in the deck: $13$.
- Kings in the deck: $4$.
- Face cards (J, Q, K): $3$ per suit, $12$ in total.

---

### One Card Drawn

Each card has probability $\tfrac{1}{52}$.

- **Event $A_1$ — the card is a heart**  
  There are $13$ hearts.  
  \[
  \mathbb{P}(A_1) = \tfrac{13}{52} = \tfrac{1}{4}.
  \]

- **Event $B_1$ — the card is a king**  
  There are $4$ kings.  
  \[
  \mathbb{P}(B_1) = \tfrac{4}{52} = \tfrac{1}{13}.
  \]

- **Event $C_1$ — the card is not a face card (not J, Q, or K)**  
  Face cards: $12$ in total, so non‑face cards: $52 - 12 = 40$.  
  \[
  \mathbb{P}(C_1) = \tfrac{40}{52} = \tfrac{10}{13}.
  \]

---

### Two Cards Drawn (with replacement)

For each draw, we have a full deck of $52$ cards again.  
The sample space $\Omega_2$ consists of $52^2$ ordered pairs, each with probability $\tfrac{1}{52^2}$.

- **Event $A_2$ — both cards are hearts**  
  Probability that the first card is a heart: $\tfrac{13}{52} = \tfrac{1}{4}$.  
  The second draw is independent with the same probability.  
  \[
  \mathbb{P}(A_2) = \left(\tfrac{1}{4}\right)^2 = \tfrac{1}{16}.
  \]

- **Event $B_2$ — both cards have the same rank**  
  On the first draw, any rank may appear.  
  On the second draw, to match that rank, we must draw one of the $4$ cards of that rank out of $52$:
  \[
  \mathbb{P}(B_2) = \tfrac{4}{52} = \tfrac{1}{13}.
  \]

- **Event $C_2$ — at least one card is an ace**  
  It is convenient to use the complement “no aces in either draw”.  
  Probability that one draw is **not** an ace: $1 - \tfrac{4}{52} = \tfrac{48}{52} = \tfrac{12}{13}$.  
  Two independent draws:
  \[
  \mathbb{P}(\text{no ace}) = \left(\tfrac{12}{13}\right)^2.
  \]
  Hence
  \[
  \mathbb{P}(C_2)
  = 1 - \left(\tfrac{12}{13}\right)^2
  = 1 - \tfrac{144}{169}
  = \tfrac{25}{169}.
  \]

---

### Two Cards Drawn (without replacement)

Now the second card is drawn from the remaining $51$ cards.  
The sample space $\Omega_2'$ consists of $52 \cdot 51$ ordered pairs.

- **Event $A_3$ — both cards are hearts**  
  First card a heart: $\tfrac{13}{52} = \tfrac{1}{4}$.  
  Second card a heart given the first was a heart: $\tfrac{12}{51}$.  
  \[
  \mathbb{P}(A_3) = \tfrac{13}{52} \cdot \tfrac{12}{51}
                  = \tfrac{1}{4} \cdot \tfrac{12}{51}
                  = \tfrac{12}{204}
                  = \tfrac{1}{17}.
  \]

- **Event $B_3$ — both cards have the same rank**  
  An ordered pair “same rank” is: choose the rank and then choose **two distinct cards** of that rank and order them.

  - Choose the rank: $13$ ways.
  - Choose the first card in that rank: $4$ ways.
  - Choose the second card (same rank, different card): $3$ ways.

  So
  \[
  \lvert B_3 \rvert = 13 \cdot 4 \cdot 3 = 156.
  \]
  Total number of ordered pairs: $52 \cdot 51 = 2652$.  
  Therefore
  \[
  \mathbb{P}(B_3) = \tfrac{156}{2652} = \tfrac{1}{17}.
  \]

- **Event $C_3$ — one card is a king and the other is a queen (in any order)**  
  We count ordered pairs:

  - Case 1: first king, second queen.  
    First card: one of $4$ kings.  
    Second card: one of $4$ queens.  
    Outcomes: $4 \cdot 4 = 16$.
  - Case 2: first queen, second king.  
    Similarly: $4 \cdot 4 = 16$.

  Total favorable ordered pairs: $16 + 16 = 32$.  
  Thus
  \[
  \mathbb{P}(C_3) = \tfrac{32}{52 \cdot 51}
                  = \tfrac{32}{2652}
                  = \tfrac{8}{663}.
  \]

---

### Additional event on $\Omega_2'$

Define, for example, the event
$$
D_3 = \{\text{both cards are red (hearts or diamonds)}\}.
$$
There are $26$ red cards in total.

Probability that the first card is red: $\tfrac{26}{52} = \tfrac{1}{2}$.  
Given that, there remain $25$ red cards out of $51$:
\[
\mathbb{P}(D_3) = \tfrac{26}{52} \cdot \tfrac{25}{51}
                = \tfrac{1}{2} \cdot \tfrac{25}{51}
                = \tfrac{25}{102}.
\]

