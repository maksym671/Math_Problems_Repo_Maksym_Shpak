# Solution

## Task 4 — Weekly Weather Observation

We classify the weather on a day into exactly one of the three states:
Sunny ($S$), Cloudy ($C$), or Rainy ($R$). We observe the weather once per day for consecutive days.

1. **Sample space for one day**  
   The possible weather states are  
   $\Omega_1 = \{S, C, R\}$.  
   Thus $\lvert \Omega_1 \rvert = 3$.

2. **Sample space for two consecutive days**  
   For two days, an elementary outcome is an ordered pair $(w_1, w_2)$ where each $w_i \in \{S,C,R\}$.  
   The sample space is  
   $\Omega_2 = \{(w_1, w_2) : w_1, w_2 \in \{S, C, R\}\}$.  
   There are  
   $\lvert \Omega_2 \rvert = 3^2 = 9$  
   elementary outcomes.

3. **Sample space for seven consecutive days**  
   For a full week, an elementary outcome is an ordered 7-tuple  
   $(w_1, w_2, \dots, w_7)$, where each $w_i \in \{S,C,R\}$.  
   The sample space is  
   $\Omega_7 = \{(w_1,\dots,w_7) : w_i \in \{S, C, R\} \text{ for } i = 1,\dots,7\}$.  
   The number of elementary outcomes is  
   $\lvert \Omega_7 \rvert = 3^7$.

4. **Meaning of an elementary outcome for a weekly observation**  
   An **elementary outcome** in $\Omega_7$ is one completely specified sequence of weather states over the seven days, for example  
   $(S, S, C, R, S, C, R)$,  
   which means: sunny on day 1, sunny on day 2, cloudy on day 3, rainy on day 4, sunny on day 5, cloudy on day 6, and rainy on day 7.

