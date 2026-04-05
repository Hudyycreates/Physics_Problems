## Problem 3: Superposition Principle

###  Conceptual Introduction

When two waves exist in the same medium at the same time, the
**superposition principle** states that the total displacement at every
point is the **sum** of the individual displacements. The waves pass
through each other completely unchanged.

Here we have two waves with identical amplitude $A$, wavenumber $k$,
and angular frequency $\omega$, but traveling in **opposite directions**:

- $y_1(x,t) = A\sin(kx - \omega t)$ — traveling in the $+x$ direction
- $y_2(x,t) = A\sin(kx + \omega t)$ — traveling in the $-x$ direction

When these two meet, they produce a **standing wave** — a pattern that
oscillates in time but has fixed positions of zero displacement (**nodes**)
and fixed positions of maximum displacement (**antinodes**).

---

###  Step 1 — Write the Superposition

Add the two wave equations together:

$$y(x,t) = y_1 + y_2 = A\sin(kx - \omega t) + A\sin(kx + \omega t)$$

Factor out $A$:

$$y(x,t) = A\bigl[\sin(kx - \omega t) + \sin(kx + \omega t)\bigr]$$

---

### 📐 Step 2 — Apply the Sum-to-Product Identity

We use the standard trigonometric identity:

$$\sin P + \sin Q = 2\sin\!\left(\frac{P + Q}{2}\right)\cos\!\left(\frac{P - Q}{2}\right)$$

Let $P = kx - \omega t$ and $Q = kx + \omega t$. Then:

$$\frac{P + Q}{2} = \frac{(kx - \omega t) + (kx + \omega t)}{2} = \frac{2kx}{2} = kx$$

$$\frac{P - Q}{2} = \frac{(kx - \omega t) - (kx + \omega t)}{2} = \frac{-2\omega t}{2} = -\omega t$$

Substituting back:

$$y(x,t) = A \cdot 2\sin(kx)\cos(-\omega t)$$

Since cosine is an even function, $\cos(-\omega t) = \cos(\omega t)$:

$$\boxed{y(x,t) = 2A\sin(kx)\cos(\omega t)}$$

---

###  Interpreting the Standing Wave

The equation $y(x,t) = 2A\sin(kx)\cos(\omega t)$ separates cleanly
into two independent factors:

| Factor | Expression | Role |
|--------|------------|------|
| Spatial | $\sin(kx)$ | Determines **where** nodes and antinodes are — fixed in space |
| Temporal | $\cos(\omega t)$ | Makes the entire pattern **oscillate** in time |

Every point on the string oscillates at angular frequency $\omega$, but its
**local amplitude** depends on position:

$$\text{local amplitude} = 2A\sin(kx)$$

This is why the wave is called "standing" — the **shape** is fixed in space
and only the size oscillates in time, unlike a traveling wave where the
entire pattern moves.

---

###  Step 3 — Finding the Nodes

Nodes are positions where the displacement is **always zero**, regardless
of time. Since $\cos(\omega t)$ is not always zero, we need:

$$\sin(kx) = 0$$

This occurs whenever:

$$kx = n\pi, \quad n = 0, 1, 2, 3, \ldots$$

Since $k = \dfrac{2\pi}{\lambda}$:

$$\frac{2\pi}{\lambda} \cdot x = n\pi$$

$$\boxed{x_{node} = \frac{n\lambda}{2}, \quad n = 0, 1, 2, 3, \ldots}$$

Nodes are spaced exactly **half a wavelength** apart.

---

###  Step 4 — Finding the Antinodes

Antinodes are positions where the amplitude is **maximum** ($= 2A$):

$$\sin(kx) = \pm 1$$

$$kx = \frac{(2n-1)\pi}{2}, \quad n = 1, 2, 3, \ldots$$

$$\boxed{x_{antinode} = \frac{(2n-1)\lambda}{4}, \quad n = 1, 2, 3, \ldots}$$

That is: $x = \dfrac{\lambda}{4},\ \dfrac{3\lambda}{4},\ \dfrac{5\lambda}{4}, \ldots$

Antinodes also sit **halfway between** consecutive nodes.

---

###  Summary Table

| Feature | Expression | First few positions |
|---------|-----------|---------------------|
| Nodes | $x = n\lambda/2$ | $0,\ \lambda/2,\ \lambda,\ 3\lambda/2, \ldots$ |
| Antinodes | $x = (2n-1)\lambda/4$ | $\lambda/4,\ 3\lambda/4,\ 5\lambda/4, \ldots$ |
| Node spacing | $\lambda/2$ | — |
| Antinode spacing | $\lambda/2$ | — |

---

###  Common Mistakes

- ❌ **Expecting a traveling wave** — two opposite-traveling waves of equal
  amplitude always produce a **standing** wave, not a traveling one
- ❌ **Forgetting $\cos(-\omega t) = \cos(\omega t)$** — cosine is even;
  missing this step leaves an unnecessary negative sign
- ❌ **Applying the identity incorrectly** — make sure to identify $P$ and $Q$
  carefully before substituting into the sum-to-product formula

---

###  What If the Amplitudes Were Different?

If $y_1 = A\sin(kx - \omega t)$ and $y_2 = B\sin(kx + \omega t)$ with $A \neq B$,
the result is **not** a pure standing wave. It becomes a combination of a
standing wave and a traveling wave — the nodes no longer have zero displacement.
Pure standing waves only arise when the two amplitudes are exactly equal.
