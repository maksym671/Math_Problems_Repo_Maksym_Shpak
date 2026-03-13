# Solution

## Task 10 — Events and Probabilities in Buffon's Needle Experiment

We consider the Buffon's needle model from **Task 5**.  
A needle of length $L \le d$ is thrown onto a plane with equally spaced parallel lines at distance $d$.  
Let:
- $X \in [0, d/2]$ be the distance from the needle's center to the nearest line,
- $\theta \in [0, \pi/2]$ be the angle between the needle and the lines.

Assume $X$ and $\theta$ are independent and **uniformly distributed** on their intervals.

The joint density is therefore constant on the rectangle
\[
0 \le X \le \tfrac{d}{2}, \quad 0 \le \theta \le \tfrac{\pi}{2}.
\]
We can work with **areas** and then divide by the total area
\[
\text{Area}_{\text{total}} = \tfrac{d}{2} \cdot \tfrac{\pi}{2}
                           = \tfrac{d \pi}{4}.
\]

### Geometric condition for intersection

The needle intersects a line if and only if the projection of half the needle onto the direction perpendicular to the lines is at least $X$.  
The standard condition is
\[
X \le \tfrac{L}{2} \sin \theta.
\]

---

### Event $A$ — the needle intersects one of the lines

We integrate the uniform density over the region
\[
0 \le X \le \tfrac{L}{2} \sin \theta,
\quad 0 \le \theta \le \tfrac{\pi}{2}.
\]
The corresponding area is
\[
\text{Area}_A
 = \int_{0}^{\pi/2} \left( \int_{0}^{(L/2)\sin\theta} dX \right) d\theta
 = \int_{0}^{\pi/2} \tfrac{L}{2} \sin\theta \, d\theta
 = \tfrac{L}{2} \left[-\cos\theta\right]_{0}^{\pi/2}
 = \tfrac{L}{2} (1 - 0)
 = \tfrac{L}{2}.
\]

Thus
\[
\mathbb{P}(A)
 = \frac{\text{Area}_A}{\text{Area}_{\text{total}}}
 = \frac{(L/2)}{d\pi/4}
 = \frac{2L}{d\pi}.
\]

---

### Event $B$ — the needle does not intersect any line

This is the complement of $A$, so
\[
\mathbb{P}(B) = 1 - \mathbb{P}(A)
              = 1 - \frac{2L}{d\pi}.
\]

---

### Event $C$ — the angle between the needle and the lines is smaller than $\frac{\pi}{6}$

This event depends only on $\theta$.  
Since $\theta$ is uniform on $[0,\pi/2]$,
\[
\mathbb{P}(C)
 = \frac{\text{length of }[0,\pi/6]}{\text{length of }[0,\pi/2]}
 = \frac{\pi/6}{\pi/2}
 = \tfrac{1}{3}.
\]

---

### Event $D$ — the center of the needle falls at a distance less than $\frac{d}{4}$ from the nearest line

This event depends only on $X$.  
Since $X$ is uniform on $[0,d/2]$,
\[
\mathbb{P}(D)
 = \frac{\text{length of }[0,d/4]}{\text{length of }[0,d/2]}
 = \frac{d/4}{d/2}
 = \tfrac{1}{2}.
\]

---

### Event $E$ — the needle intersects a line and the angle is greater than $\frac{\pi}{4}$

We combine the intersection condition $X \le \tfrac{L}{2}\sin\theta$ with the angle constraint $\theta \in [\pi/4, \pi/2]$.

The area of this region is
\[
\text{Area}_E
 = \int_{\theta=\pi/4}^{\pi/2}
     \left( \int_{X=0}^{(L/2)\sin\theta} dX \right) d\theta
 = \int_{\pi/4}^{\pi/2} \tfrac{L}{2} \sin\theta \, d\theta
 = \tfrac{L}{2} \left[-\cos\theta\right]_{\pi/4}^{\pi/2}
 = \tfrac{L}{2} \left( -\cos\tfrac{\pi}{2} + \cos\tfrac{\pi}{4} \right)
 = \tfrac{L}{2} \cdot \tfrac{\sqrt{2}}{2}
 = \tfrac{L\sqrt{2}}{4}.
\]

Thus
\[
\mathbb{P}(E)
 = \frac{\text{Area}_E}{\text{Area}_{\text{total}}}
 = \frac{L\sqrt{2}/4}{d\pi/4}
 = \frac{L\sqrt{2}}{d\pi}.
\]

Note that $E \subset A$, so indeed $\mathbb{P}(E) \le \mathbb{P}(A)$ when $L \le d$.

---

### Additional event

As an example, define the event
$$
F = \left\{\theta \in \left[\tfrac{\pi}{6}, \tfrac{\pi}{3}\right]\right\},
$$
meaning that the angle between the needle and the lines lies between $\tfrac{\pi}{6}$ and $\tfrac{\pi}{3}$.
Since $\theta$ is uniform on $[0,\pi/2]$,
\[
\mathbb{P}(F)
 = \frac{\tfrac{\pi}{3} - \tfrac{\pi}{6}}{\tfrac{\pi}{2}}
 = \frac{\tfrac{\pi}{6}}{\tfrac{\pi}{2}}
 = \tfrac{1}{3}.
\]

