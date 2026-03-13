# Solution

## Task 7 — Events and Probabilities in Die Rolling

We use the sample spaces from **Task 2**:
- $\Omega_1 = \{1,2,3,4,5,6\}$ for one roll,
- $\Omega_2 = \{(i,j) : i,j \in \{1,\dots,6\}\}$ for two rolls,
- $\Omega_3 = \{(i,j,k) : i,j,k \in \{1,\dots,6\}\}$ for three rolls.

The die is **fair**, so all elementary outcomes in each $\Omega_n$ are **equally likely**.

### Probabilities of elementary outcomes

- For one roll: for every $\omega \in \Omega_1$,  
  $\mathbb{P}(\{\omega\}) = \tfrac{1}{6}$.
- For two rolls: for every $\omega \in \Omega_2$,  
  $\mathbb{P}(\{\omega\}) = \tfrac{1}{36}$.
- For three rolls: for every $\omega \in \Omega_3$,  
  $\mathbb{P}(\{\omega\}) = \tfrac{1}{216}$.

---

### One Die Roll

- **Event $A_1$ — the result is even**  
  $A_1 = \{2,4,6\} \subset \Omega_1$.  
  $\lvert A_1 \rvert = 3$, so  
  $\mathbb{P}(A_1) = \tfrac{3}{6} = \tfrac{1}{2}$.

- **Event $B_1$ — the result is greater than 4**  
  $B_1 = \{5,6\}$, so  
  $\mathbb{P}(B_1) = \tfrac{2}{6} = \tfrac{1}{3}$.

- **Event $C_1$ — the result is at most 3**  
  $C_1 = \{1,2,3\}$, so  
  $\mathbb{P}(C_1) = \tfrac{3}{6} = \tfrac{1}{2}$.

---

### Two Die Rolls

Each outcome in $\Omega_2$ has probability $\tfrac{1}{36}$.

- **Event $A_2$ — the sum of the results equals 7**  
  Pairs $(i,j)$ with $i+j=7$:  
  $(1,6), (2,5), (3,4), (4,3), (5,2), (6,1)$ — 6 outcomes.  
  Hence
  $\mathbb{P}(A_2) = \tfrac{6}{36} = \tfrac{1}{6}$.

- **Event $B_2$ — both results are the same**  
  $(1,1), (2,2), (3,3), (4,4), (5,5), (6,6)$ — 6 outcomes.  
  $\mathbb{P}(B_2) = \tfrac{6}{36} = \tfrac{1}{6}$.

- **Event $C_2$ — the sum of the results is at least 10**  
  We list all pairs with sum $10,11,12$:
  - Sum $10$: $(4,6),(5,5),(6,4)$ — 3 outcomes,  
  - Sum $11$: $(5,6),(6,5)$ — 2 outcomes,  
  - Sum $12$: $(6,6)$ — 1 outcome.  
  In total $3+2+1=6$ outcomes, so  
  $\mathbb{P}(C_2) = \tfrac{6}{36} = \tfrac{1}{6}$.

---

### Three Die Rolls

Each outcome in $\Omega_3$ has probability $\tfrac{1}{216}$.

- **Event $A_3$ — the sum of the results equals 10**  
  We count the number of triples $(i,j,k)$ with $i+j+k=10$, $1 \le i,j,k \le 6$.  
  The valid unordered partitions of 10 into 3 positive integers not exceeding 6 are:
  - $(1,1,8)$ — invalid (8 > 6),
  - $(1,2,7)$ — invalid,
  - $(1,3,6)$ — valid,
  - $(1,4,5)$ — valid,
  - $(2,2,6)$ — valid,
  - $(2,3,5)$ — valid,
  - $(2,4,4)$ — valid,
  - $(3,3,4)$ — valid.

  Now we count permutations:
  - Type $(1,3,6)$: all distinct → $3! = 6$ permutations,  
  - Type $(1,4,5)$: all distinct → $6$ permutations,  
  - Type $(2,2,6)$: two equal → $3$ permutations,  
  - Type $(2,3,5)$: all distinct → $6$ permutations,  
  - Type $(2,4,4)$: two equal → $3$ permutations,  
  - Type $(3,3,4)$: two equal → $3$ permutations.  

  Total number of outcomes:
  \[
  6 + 6 + 3 + 6 + 3 + 3 = 27.
  \]
  Therefore
  \[
  \mathbb{P}(A_3) = \tfrac{27}{216} = \tfrac{1}{8}.
  \]

- **Event $B_3$ — exactly two rolls give the same number**  
  Exactly two equal and the third different.  
  We proceed in two steps:
  1. Choose the value that appears twice: $6$ options.  
  2. Choose the value that appears once (different from the first): $5$ options.  
  3. Arrange the multiset $\{a,a,b\}$ in three positions: $3$ ways.  

  Total:
  \[
  6 \cdot 5 \cdot 3 = 90.
  \]
  Hence
  \[
  \mathbb{P}(B_3) = \tfrac{90}{216} = \tfrac{5}{12}.
  \]

- **Event $C_3$ — two twos and one three (in any order)**  
  Multiset $\{2,2,3\}$ has $3$ permutations:
  $(2,2,3), (2,3,2), (3,2,2)$.  
  Thus
  \[
  \mathbb{P}(C_3) = \tfrac{3}{216} = \tfrac{1}{72}.
  \]

---

### Additional event on $\Omega_3$

Define the event
$$
D_3 = \{\text{all three results are different}\}.
$$
We choose three distinct numbers from $\{1,\dots,6\}$ in $\binom{6}{3}$ ways and then permute them in $3!$ ways:
\[
\lvert D_3 \rvert = \binom{6}{3} \cdot 3! = 20 \cdot 6 = 120.
\]
Therefore
\[
\mathbb{P}(D_3) = \tfrac{120}{216} = \tfrac{5}{9}.
\]

