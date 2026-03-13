# Solution 1

## Task 1 — Coin Tossing

We toss a **fair coin**. The order of outcomes matters.

1. **Sample space for one coin toss**  
   The possible outcomes are  
   $\Omega_1 = \{H, T\}$,
   where $H$ denotes *heads* and $T$ denotes *tails*.

2. **Sample space for two coin tosses**  
   We list all ordered pairs $(\text{first toss}, \text{second toss})$:  
   $\Omega_2 = \{(H,H), (H,T), (T,H), (T,T)\}$.

3. **Sample space for three coin tosses**  
   We list all ordered triples $(\text{first}, \text{second}, \text{third})$:  
   $\Omega_3 = \{(H,H,H), (H,H,T), (H,T,H), (H,T,T), (T,H,H), (T,H,T), (T,T,H), (T,T,T)\}$.

4. **Number of elementary outcomes**
   - For one toss: $\lvert \Omega_1 \rvert = 2$.  
   - For two tosses: $\lvert \Omega_2 \rvert = 4 = 2^2$.  
   - For three tosses: $\lvert \Omega_3 \rvert = 8 = 2^3$.

5. **Meaning of an elementary outcome**  
   An **elementary outcome** is one completely specified result of the experiment:
   - For one toss, an elementary outcome is simply $H$ or $T$.  
   - For two tosses, an elementary outcome is one ordered pair such as $(H,T)$, meaning *heads on the first toss and tails on the second toss*.  
   - For three tosses, an elementary outcome is one ordered triple such as $(T,H,H)$, meaning *tails on the first toss, heads on the second toss, and heads on the third toss*.