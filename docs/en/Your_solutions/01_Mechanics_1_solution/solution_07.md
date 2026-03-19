# Question 7: Elimination of Time and Interpretation of Acceleration

> **Problem:** The path of an object is given parametrically as $x(t) = 2t^2$, $y(t) = 3t^3$.  
> Eliminate the parameter $t$, draw the trajectory, calculate $\vec{v}(t)$, $|\vec{v}(t)|$, $\vec{a}(t)$, $|\vec{a}(t)|$, and determine whether the acceleration is constant.

---

## Background

A parametric path expresses both coordinates as separate functions of a shared parameter $t$ (usually time). To understand the actual shape of the path — independent of when the object passes through each point — we eliminate $t$ and write $y$ directly as a function of $x$.

| Quantity | Relationship |
|----------|-------------|
| Position | $\vec{r}(t) = x(t)\hat{i} + y(t)\hat{j}$ |
| Velocity | $\vec{v}(t) = \dfrac{d\vec{r}}{dt}$ |
| Acceleration | $\vec{a}(t) = \dfrac{d\vec{v}}{dt}$ |

---

## Part 1 — Eliminate the Parameter $t$

### Step 1 — Solve for $t$ from $x(t)$

$$x = 2t^2 \implies t^2 = \frac{x}{2} \implies t = \sqrt{\frac{x}{2}} \quad (t \geq 0)$$

### Step 2 — Substitute into $y(t)$

$$y = 3t^3 = 3t \cdot t^2 = 3\sqrt{\frac{x}{2}} \cdot \frac{x}{2} = \frac{3x}{2} \cdot \frac{\sqrt{x}}{\sqrt{2}} = \frac{3x^{3/2}}{2\sqrt{2}}$$

### Step 3 — Rationalize

Multiply numerator and denominator by $\sqrt{2}$:

$$\boxed{y = \frac{3\sqrt{2}}{4}\,x^{3/2}}$$

This is the Cartesian equation of the path — a **power curve** of the form $y \propto x^{3/2}$, valid for $x \geq 0$.

---

## Part 2 — Trajectory

The curve $y = \dfrac{3\sqrt{2}}{4}\,x^{3/2}$ passes through the origin and curves upward with increasing steepness. Key points along the trajectory:

| $t$ | $x = 2t^2$ | $y = 3t^3$ |
|-----|-----------|-----------|
| 0 | 0 | 0 |
| 0.5 | 0.5 | 0.375 |
| 1.0 | 2 | 3 |
| 1.5 | 4.5 | 10.125 |

The object starts at the origin and moves to the right and upward, with the vertical displacement growing faster than the horizontal because $y \sim t^3$ while $x \sim t^2$.

---

## Part 3 — Velocity Vector $\vec{v}(t)$

### Differentiate each component

$$v_x(t) = \frac{dx}{dt} = \frac{d}{dt}(2t^2) = 4t$$

$$v_y(t) = \frac{dy}{dt} = \frac{d}{dt}(3t^3) = 9t^2$$

### Velocity vector

$$\boxed{\vec{v}(t) = 4t\,\hat{i} + 9t^2\,\hat{j}}$$

### Magnitude of velocity $|\vec{v}(t)|$

$$|\vec{v}(t)| = \sqrt{v_x^2 + v_y^2} = \sqrt{(4t)^2 + (9t^2)^2} = \sqrt{16t^2 + 81t^4}$$

Factor out $t^2$:

$$\boxed{|\vec{v}(t)| = t\sqrt{16 + 81t^2}} \quad (t \geq 0)$$

At $t = 0$ the object is momentarily at rest. The speed increases continuously for $t > 0$.

---

## Part 4 — Acceleration Vector $\vec{a}(t)$

### Differentiate the velocity components

$$a_x(t) = \frac{dv_x}{dt} = \frac{d}{dt}(4t) = 4$$

$$a_y(t) = \frac{dv_y}{dt} = \frac{d}{dt}(9t^2) = 18t$$

### Acceleration vector

$$\boxed{\vec{a}(t) = 4\,\hat{i} + 18t\,\hat{j}}$$

### Magnitude of acceleration $|\vec{a}(t)|$

$$|\vec{a}(t)| = \sqrt{a_x^2 + a_y^2} = \sqrt{(4)^2 + (18t)^2}$$

$$\boxed{|\vec{a}(t)| = \sqrt{16 + 324t^2}}$$

---

## Part 5 — Is the Acceleration Constant?

**No.** To be constant, both components of $\vec{a}(t)$ must be independent of $t$:

| Component | Expression | Depends on $t$? |
|-----------|-----------|-----------------|
| $a_x$ | $4$ | No — constant |
| $a_y$ | $18t$ | Yes — grows linearly with $t$ |

Since $a_y = 18t$ changes with time, the acceleration vector **changes in both direction and magnitude** as $t$ increases.

$$\vec{a}(0) = 4\hat{i} + 0\hat{j}, \quad \vec{a}(1) = 4\hat{i} + 18\hat{j}, \quad \vec{a}(2) = 4\hat{i} + 36\hat{j}$$

The horizontal component is fixed at $4$ units, but the vertical component grows without bound. Therefore, the acceleration is **not constant**.

---

## Summary of Results

| Quantity | Expression |
|----------|-----------|
| Cartesian path equation | $y = \dfrac{3\sqrt{2}}{4}\,x^{3/2}$ |
| Velocity vector | $\vec{v}(t) = 4t\,\hat{i} + 9t^2\,\hat{j}$ |
| Speed | $\|\vec{v}(t)\| = t\sqrt{16 + 81t^2}$ |
| Acceleration vector | $\vec{a}(t) = 4\,\hat{i} + 18t\,\hat{j}$ |
| Magnitude of acceleration | $\|\vec{a}(t)\| = \sqrt{16 + 324t^2}$ |
| Acceleration constant? | No — the $\hat{j}$ component $18t$ depends on $t$ |

---

## Interpretation

The horizontal acceleration $a_x = 4$ is constant — the object is being pushed to the right at a steady rate. The vertical acceleration $a_y = 18t$ starts at zero and grows with time — the upward push becomes stronger the longer the object has been in motion. This means the path curves more and more steeply upward as $t$ increases, which is consistent with the shape of $y \propto x^{3/2}$.

---

*Solved using parametric differentiation, integration of power functions, and component-wise vector analysis.*
