# Solution

## Task 3 — Drawing Cards

We draw cards from a **standard 52-card deck**. The order of outcomes matters and we treat each outcome as an **ordered sequence** of cards.

1. **Sample space for drawing one card**  
   Each elementary outcome is a single card from the deck.  
   The sample space is  
   $\Omega_1 = \{\text{all 52 distinct cards in the deck}\}$,  
   so $\lvert \Omega_1 \rvert = 52$.

2. **Sample space for two consecutive draws with replacement**  
   After the first draw, we put the card back and reshuffle; every draw is from a full 52-card deck.  
   An elementary outcome is an ordered pair $(c_1, c_2)$ where $c_1$ and $c_2$ are cards from the deck and repetitions are allowed.  
   The sample space is  
   $\Omega_2 = \{(c_1, c_2) : c_1 \in \Omega_1,\ c_2 \in \Omega_1\}$.  
   The number of elementary outcomes is  
   $\lvert \Omega_2 \rvert = 52 \cdot 52 = 52^2$.

3. **Sample space for two consecutive draws without replacement**  
   After the first draw, we do **not** put the card back, so the second draw is from the remaining 51 cards.  
   An elementary outcome is an ordered pair $(c_1, c_2)$ of **distinct** cards.  
   The sample space is  
   $\Omega_2' = \{(c_1, c_2) : c_1, c_2 \in \Omega_1,\ c_1 \neq c_2\}$.  
   The number of elementary outcomes is  
   $\lvert \Omega_2' \rvert = 52 \cdot 51$.

4. **Meaning of an elementary outcome**  
   An **elementary outcome** is one completely specified ordered sequence of drawn cards:
   - For $\Omega_1$, an elementary outcome is one particular card, for example “Ace of Spades”.  
   - For $\Omega_2$ (with replacement), an elementary outcome might be $(\text{Ace of Spades}, \text{Ace of Spades})$ or $(\text{King of Hearts}, \text{3 of Clubs})$, where repetitions are allowed.  
   - For $\Omega_2'$ (without replacement), an elementary outcome might be $(\text{Ace of Spades}, \text{King of Hearts})$, where the two cards are necessarily different because the first card is not returned to the deck.

