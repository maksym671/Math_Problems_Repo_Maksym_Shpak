# Solution

## Task 2 — Rolling a Die

We roll a **fair six-sided die**. The order of outcomes again matters.

1. **Sample space for one roll of the die**  
   The possible outcomes are the six faces:  
   $\Omega_1 = \{1, 2, 3, 4, 5, 6\}$.

2. **Sample space for two consecutive rolls**  
   We list all ordered pairs $(\text{first roll}, \text{second roll})$:  
   $\Omega_2 = \{(i,j) : i \in \{1,\dots,6\},\ j \in \{1,\dots,6\}\}$.

3. **Sample space for three consecutive rolls**  
   We list all ordered triples $(\text{first}, \text{second}, \text{third})$:  
   $\Omega_3 = \{(i,j,k) : i,j,k \in \{1,\dots,6\}\}$.

4. **Number of elementary outcomes**
   - For one roll: $\lvert \Omega_1 \rvert = 6$.  
   - For two rolls: $\lvert \Omega_2 \rvert = 6^2 = 36$.  
   - For three rolls: $\lvert \Omega_3 \rvert = 6^3 = 216$.

5. **Meaning of an elementary outcome**  
   An **elementary outcome** is one completely specified result of the experiment:
   - For one roll, an elementary outcome is one face (for example $4$).  
   - For two rolls, an elementary outcome is one ordered pair such as $(2,5)$, meaning *2 on the first roll and 5 on the second roll*.  
   - For three rolls, an elementary outcome is one ordered triple such as $(6,1,3)$, meaning *6 on the first roll, 1 on the second roll, and 3 on the third roll*.
