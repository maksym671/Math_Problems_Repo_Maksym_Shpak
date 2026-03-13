# Solution

## Task 9 — Events and Probabilities in Weekly Weather Observation

We consider the sample space $\Omega_7$ of all weather sequences over seven consecutive days.  
Each day independently takes one of three states:
- Sunny ($S$),
- Cloudy ($C$),
- Rainy ($R$),
each with probability $\tfrac{1}{3}$.

Therefore, there are $\lvert \Omega_7 \rvert = 3^7$ elementary outcomes, all with probability
\[
\mathbb{P}(\{\omega\}) = \left(\tfrac{1}{3}\right)^7
\quad\text{for every } \omega \in \Omega_7.
\]

We compute probabilities using independence of days.

---

### Event $A$ — the entire weekend is sunny

Saturday and Sunday (two fixed days) must both be $S$.  
For each of these days,
\[
\mathbb{P}(\text{day is } S) = \tfrac{1}{3},
\]
and the days are independent. Hence
\[
\mathbb{P}(A) = \left(\tfrac{1}{3}\right)^2 = \tfrac{1}{9}.
\]

---

### Event $B$ — Wednesday, Thursday, and Friday are all rainy

For each of the three days (Wednesday, Thursday, Friday),
\[
\mathbb{P}(\text{day is } R) = \tfrac{1}{3}.
\]
Thus
\[
\mathbb{P}(B) = \left(\tfrac{1}{3}\right)^3 = \tfrac{1}{27}.
\]

---

### Event $C$ — at least one day during the week is sunny

It is convenient to use the complement: “no day is sunny”, i.e. all days are either $C$ or $R$.

- Probability that a single day is **not sunny**: $\mathbb{P}(\text{day} \ne S) = \tfrac{2}{3}$.  
- For seven independent days:
  \[
  \mathbb{P}(\text{no day is sunny}) = \left(\tfrac{2}{3}\right)^7.
  \]

Therefore
\[
\mathbb{P}(C) = 1 - \left(\tfrac{2}{3}\right)^7.
\]

---

### Event $D$ — no rainy day occurs during the entire week

Every day must be either $S$ or $C$, but never $R$.

- Probability that a single day is **not rainy**: $\mathbb{P}(\text{day} \ne R) = \tfrac{2}{3}$.  
- For seven independent days:
  \[
  \mathbb{P}(D) = \left(\tfrac{2}{3}\right)^7.
  \]

---

### Event $E$ — exactly two days during the week are sunny

We choose which two of the seven days are sunny and require that the remaining five are not sunny.

- Number of ways to choose the two sunny days: $\binom{7}{2}$.  
- Probability pattern for any **fixed** choice of two sunny days:
  - Two sunny days: $(\tfrac{1}{3})^2$,
  - Five non‑sunny days: $(\tfrac{2}{3})^5$.

Thus
\[
\mathbb{P}(E)
 = \binom{7}{2}
   \left(\tfrac{1}{3}\right)^2
   \left(\tfrac{2}{3}\right)^5
 = 21 \cdot \tfrac{1}{9} \cdot \tfrac{32}{243}
 = \tfrac{672}{2187}.
\]

---

### Additional event on $\Omega_7$

Define, for example, the event
$$
F = \{\text{all seven days have the same weather}\}.
$$
There are three possible constant sequences:
\[
(S,S,S,S,S,S,S),\;
(C,C,C,C,C,C,C),\;
(R,R,R,R,R,R,R).
\]
Each such sequence has probability $\left(\tfrac{1}{3}\right)^7$, so
\[
\mathbb{P}(F) = 3 \cdot \left(\tfrac{1}{3}\right)^7
              = \tfrac{3}{3^7}
              = \tfrac{1}{3^6}
              = \tfrac{1}{729}.
\]

