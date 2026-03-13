# Solution

## Task 6 — Events and Probabilities in Coin Tossing

We use the sample spaces from **Task 1**:
- $\Omega_1 = \{H, T\}$ for one toss,
- $\Omega_2 = \{(H,H), (H,T), (T,H), (T,T)\}$ for two tosses,
- $\Omega_3 = \{(H,H,H), (H,H,T), (H,T,H), (H,T,T), (T,H,H), (T,H,T), (T,T,H), (T,T,T)\}$ for three tosses.

The coin is **fair**, so all elementary outcomes in each $\Omega_n$ are **equally likely**.

### Probabilities of elementary outcomes

- For one toss: for every $\omega \in \Omega_1$,  
  $\mathbb{P}(\{\omega\}) = \tfrac{1}{2}$.
- For two tosses: for every $\omega \in \Omega_2$,  
  $\mathbb{P}(\{\omega\}) = \tfrac{1}{4}$.
- For three tosses: for every $\omega \in \Omega_3$,  
  $\mathbb{P}(\{\omega\}) = \tfrac{1}{8}$.

---

### One Coin Toss

- **Event $A_1$ — the result is heads**  
  $A_1 = \{H\} \subset \Omega_1$.  
  $\mathbb{P}(A_1) = \tfrac{1}{2}$.

- **Event $B_1$ — the result is tails**  
  $B_1 = \{T\} \subset \Omega_1$.  
  $\mathbb{P}(B_1) = \tfrac{1}{2}$.

- **Event $C_1$ — the result is not tails**  
  $C_1 = \{H\} \subset \Omega_1$.  
  $\mathbb{P}(C_1) = \tfrac{1}{2}$.

---

### Two Coin Tosses

Here each elementary outcome has probability $\tfrac{1}{4}$.

- **Event $A_2$ — exactly one head occurs**  
  $A_2 = \{(H,T), (T,H)\} \subset \Omega_2$.  
  $\mathbb{P}(A_2) = 2 \cdot \tfrac{1}{4} = \tfrac{1}{2}$.

- **Event $B_2$ — at least one head occurs**  
  $B_2 = \{(H,H), (H,T), (T,H)\} \subset \Omega_2$.  
  $\mathbb{P}(B_2) = 3 \cdot \tfrac{1}{4} = \tfrac{3}{4}$.  
  (Equivalently, $\mathbb{P}(B_2) = 1 - \mathbb{P}(\{(T,T)\}) = 1 - \tfrac{1}{4}$.)

- **Event $C_2$ — both tosses give the same result**  
  $C_2 = \{(H,H), (T,T)\} \subset \Omega_2$.  
  $\mathbb{P}(C_2) = 2 \cdot \tfrac{1}{4} = \tfrac{1}{2}$.

---

### Three Coin Tosses

Here each elementary outcome has probability $\tfrac{1}{8}$.

- **Event $A_3$ — exactly two heads occur**  
  The favorable outcomes are those with two $H$ and one $T$:  
  $A_3 = \{(H,H,T), (H,T,H), (T,H,H)\} \subset \Omega_3$.  
  $\mathbb{P}(A_3) = 3 \cdot \tfrac{1}{8} = \tfrac{3}{8}$.

- **Event $B_3$ — at least one tail occurs**  
  This is the complement of the event “no tails”, i.e. all heads:  
  $B_3 = \Omega_3 \setminus \{(H,H,H)\}$.  
  Hence  
  $\mathbb{P}(B_3) = 1 - \mathbb{P}(\{(H,H,H)\}) = 1 - \tfrac{1}{8} = \tfrac{7}{8}$.

- **Event $C_3$ — all three tosses give the same result**  
  $C_3 = \{(H,H,H), (T,T,T)\} \subset \Omega_3$.  
  $\mathbb{P}(C_3) = 2 \cdot \tfrac{1}{8} = \tfrac{1}{4}$.

---

### Additional event on $\Omega_3$

Define, for example, the event
$$
D_3 = \{\text{at least one head and at least one tail occur}\}.
$$
This is the set of all outcomes in $\Omega_3$ that contain both symbols $H$ and $T$.  
The only outcomes that do **not** belong to $D_3$ are $(H,H,H)$ and $(T,T,T)$, so
$$
\lvert D_3 \rvert = \lvert \Omega_3 \rvert - 2 = 8 - 2 = 6.
$$
Therefore
$$
\mathbb{P}(D_3) = \frac{\lvert D_3 \rvert}{\lvert \Omega_3 \rvert}
                 = \frac{6}{8}
                 = \tfrac{3}{4}.
$$

# Solution

## Task 6 — Events and Probabilities in Coin Tossing

We refer to the sample spaces from **Task 1**:
- $\Omega_1 = \{H, T\}$ for one toss,
- $\Omega_2 = \{(H,H), (H,T), (T,H), (T,T)\}$ for two tosses,
- $\Omega_3 = \{(H,H,H), (H,H,T), (H,T,H), (H,T,T), (T,H,H), (T,H,T), (T,T,H), (T,T,T)\}$ for three tosses.

The coin is **fair**, so all elementary outcomes in each $\Omega_n$ are **equally likely**.

### Probabilities of elementary outcomes

- For one toss: each outcome in $\Omega_1$ has probability  
  $\mathbb{P}(\{H\}) = \mathbb{P}(\{T\}) = \tfrac{1}{2}$.
- For two tosses: each outcome in $\Omega_2$ has probability  
  $\mathbb{P}(\{\omega\}) = \tfrac{1}{4}$ for every $\omega \in \Omega_2$.
- For three tosses: each outcome in $\Omega_3$ has probability  
  $\mathbb{P}(\{\omega\}) = \tfrac{1}{8}$ for every $\omega \in \Omega_3$.

---

### One Coin Toss

- **Event $A_1$ — the result is heads**  
  $A_1 = \{H\}$.  
  $\mathbb{P}(A_1) = \tfrac{1}{2}$.

- **Event $B_1$ — the result is tails**  
  $B_1 = \{T\}$.  
  $\mathbb{P}(B_1) = \tfrac{1}{2}$.

- **Event $C_1$ — the result is not tails**  
  $C_1 = \{H\}$ (since there are only $H$ and $T$).  
  $\mathbb{P}(C_1) = \tfrac{1}{2}$.

---

### Two Coin Tosses

Here each elementary outcome has probability $\tfrac{1}{4}$.

- **Event $A_2$ — exactly one head occurs**  
  $A_2 = \{(H,T), (T,H)\}$.  
  $\mathbb{P}(A_2) = 2 \cdot \tfrac{1}{4} = \tfrac{1}{2}$.

- **Event $B_2$ — at least one head occurs**  
  $B_2 = \{(H,H), (H,T), (T,H)\}$.  
  $\mathbb{P}(B_2) = 3 \cdot \tfrac{1}{4} = \tfrac{3}{4}$.  
  (Alternatively, $B_2$ is the complement of $\{(T,T)\}$.)

- **Event $C_2$ — both tosses give the same result**  
  $C_2 = \{(H,H), (T,T)\}$.  
  $\mathbb{P}(C_2) = 2 \cdot \tfrac{1}{4} = \tfrac{1}{2}$.

---

### Three Coin Tosses

Here each elementary outcome has probability $\tfrac{1}{8}$.

- **Event $A_3$ — exactly two heads occur**  
  The favorable outcomes are those with two $H$ and one $T$:  
  $A_3 = \{(H,H,T), (H,T,H), (T,H,H)\}$.  
  $\mathbb{P}(A_3) = 3 \cdot \tfrac{1}{8} = \tfrac{3}{8}$.

- **Event $B_3$ — at least one tail occurs**  
  This is the complement of the event “no tails”, i.e. all heads:  
  $B_3 = \Omega_3 \setminus \{(H,H,H)\}$.  
  So  
  $\mathbb{P}(B_3) = 1 - \mathbb{P}(\{(H,H,H)\}) = 1 - \tfrac{1}{8} = \tfrac{7}{8}$.

- **Event $C_3$ — all three tosses give the same result**  
  $C_3 = \{(H,H,H), (T,T,T)\}$.  
  $\mathbb{P}(C_3) = 2 \cdot \tfrac{1}{8} = \tfrac{1}{4}$.

---

### Additional event on $\Omega_3$

Define the event
$$
D_3 = \{\text{exactly one head occurs}\}.
$$
The favorable outcomes are  
$D_3 = \{(H,T,T), (T,H,T), (T,T,H)\}$.  
Thus
$$
\mathbb{P}(D_3) = 3 \cdot \tfrac{1}{8} = \tfrac{3}{8}.
$$

