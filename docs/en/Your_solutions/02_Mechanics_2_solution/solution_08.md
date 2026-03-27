# Problem 8 — Work of a Variable Force

## Conceptual Intro

$F(x) = -kx$ is Hooke's Law — the restoring force always points back to origin.
This problem chains four ideas: equation of motion → solution → work → potential energy.

---

## Part 1 — Equation of Motion

$$m\ddot{x} = -kx \implies \ddot{x} + \omega^2 x = 0, \quad \omega = \sqrt{\frac{k}{m}}$$

**General solution:**

$$\boxed{x(t) = A\cos(\omega t + \varphi)}$$

---

## Part 2 — Work from 0 to $x_0$

$$W = \int_0^{x_0} (-kx)\, dx = \left[-\frac{kx^2}{2}\right]_0^{x_0}$$

$$\boxed{W = -\frac{1}{2}kx_0^2}$$

> Negative work: spring force opposes displacement direction.

---

## Part 3 — Potential Energy

Using $W = -\Delta U$ with $U(0) = 0$:

$$\boxed{U(x) = \frac{1}{2}kx^2}$$

---

## Part 4 — Verify $F = -dU/dx$

$$-\frac{dU}{dx} = -\frac{d}{dx}\left(\frac{1}{2}kx^2\right) = -kx = F(x) \quad \checkmark$$

---

## Part 5 — Graphs

**F(x):** Straight line through origin, negative slope $-k$

**U(x):** Upward parabola, minimum at $x = 0$

Key insight: $F$ is the *negative slope* of $U$.
Where U is steepest → force is strongest.
Where U is flat (x = 0) → force is zero.
