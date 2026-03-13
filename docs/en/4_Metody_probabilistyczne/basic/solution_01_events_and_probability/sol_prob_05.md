# Solution

## Task 5 — Buffon's Needle Experiment

We throw a needle of length $L$ onto a floor with equally spaced parallel lines at distance $d$ apart.

1. **Description of the sample space $\Omega$**  
   An elementary outcome of the experiment is one particular position and orientation of the needle relative to the system of parallel lines.  
   Thus, the sample space $\Omega$ consists of **all possible positions and orientations** that the needle can take when it lands on the floor.

2. **Parameters determining the outcome of a single throw**  
   We can describe each outcome by:
   - the **distance** from the center of the needle to the nearest line,  
   - the **orientation angle** of the needle relative to the direction of the lines.

3. **Variables describing an elementary outcome**  
   Let
   - $x$ be the distance from the **center of the needle** to the nearest line,  
   - $\theta$ be the **acute angle** between the needle and the direction of the parallel lines.  
   Then one elementary outcome can be represented as the pair $(x, \theta)$.

4. **Sample space in terms of $(x, \theta)$**  
   By using symmetry, we may restrict to
   - $x \in [0, \tfrac{d}{2}]$ (the center is at most $\tfrac{d}{2}$ from the nearest line),  
   - $\theta \in [0, \tfrac{\pi}{2}]$ (angles larger than $\tfrac{\pi}{2}$ are symmetric).  
   With these variables, the sample space can be written as
   \[
   \Omega = \{(x, \theta) : 0 \le x \le \tfrac{d}{2},\ 0 \le \theta \le \tfrac{\pi}{2}\}.
   \]

5. **Why the sample space is continuous**  
   The distance $x$ and the angle $\theta$ can take **any real values** in their respective intervals (not just finitely many discrete values).  
   Therefore, the sample space is a **continuous set** of points in the $(x,\theta)$–plane, unlike the earlier tasks where the sample spaces consisted of finitely many discrete outcomes (coin tosses, die rolls, card draws, weather states).

