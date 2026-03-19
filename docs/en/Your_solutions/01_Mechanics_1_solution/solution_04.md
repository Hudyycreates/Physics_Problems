# Question 4: Vector Calculus

> **Problem:** The position of an object is given by $\vec{r}(t) = (3t^2)\hat{i} + (5t - 8t^2)\hat{j}$.  
> Find the object's **velocity** and **acceleration** vectors as a function of time.

---

## Background

In vector calculus, when an object moves through space, its position is described as a vector function of time. The relationships between position, velocity, and acceleration are:

| Quantity | Symbol | How to get it |
|----------|--------|---------------|
| Position | $\vec{r}(t)$ | Given |
| Velocity | $\vec{v}(t)$ | First derivative of $\vec{r}(t)$ |
| Acceleration | $\vec{a}(t)$ | Second derivative of $\vec{r}(t)$, or first derivative of $\vec{v}(t)$ |

The key rule: **differentiate each component independently.** The $\hat{i}$ and $\hat{j}$ unit vectors are constants, so they are unaffected by differentiation.

---

## Given

$$\vec{r}(t) = (3t^2)\hat{i} + (5t - 8t^2)\hat{j}$$

Breaking it into components:

- $x$-component: $\quad r_x(t) = 3t^2$
- $y$-component: $\quad r_y(t) = 5t - 8t^2$

---

## Step 1 — Find the Velocity Vector

Velocity is the first derivative of position with respect to time:

$$\vec{v}(t) = \frac{d\vec{r}}{dt} = \frac{d}{dt}\left[(3t^2)\hat{i} + (5t - 8t^2)\hat{j}\right]$$

Differentiate each component separately:

**$\hat{i}$ component:**
$$\frac{d}{dt}(3t^2) = 6t$$

**$\hat{j}$ component:**
$$\frac{d}{dt}(5t - 8t^2) = 5 - 16t$$

Therefore:

$$\boxed{\vec{v}(t) = (6t)\hat{i} + (5 - 16t)\hat{j}}$$

---

## Step 2 — Find the Acceleration Vector

Acceleration is the first derivative of velocity (equivalently, the second derivative of position):

$$\vec{a}(t) = \frac{d\vec{v}}{dt} = \frac{d}{dt}\left[(6t)\hat{i} + (5 - 16t)\hat{j}\right]$$

Differentiate each component separately:

**$\hat{i}$ component:**
$$\frac{d}{dt}(6t) = 6$$

**$\hat{j}$ component:**
$$\frac{d}{dt}(5 - 16t) = -16$$

Therefore:

$$\boxed{\vec{a}(t) = 6\hat{i} - 16\hat{j}}$$

Note that the acceleration vector is **constant** — it does not depend on $t$. This means the object experiences uniform acceleration throughout its motion, similar to projectile motion under constant gravity.

---

## Step 3 — Verify via Second Derivative of Position

As a check, differentiate $\vec{r}(t)$ twice directly:

**First derivative:**
$$\frac{d\vec{r}}{dt} = 6t\hat{i} + (5 - 16t)\hat{j} = \vec{v}(t) \checkmark$$

**Second derivative:**
$$\frac{d^2\vec{r}}{dt^2} = 6\hat{i} - 16\hat{j} = \vec{a}(t) \checkmark$$

Both routes give the same result.

---

## Summary of Results

| Quantity | Vector |
|----------|--------|
| Position | $\vec{r}(t) = (3t^2)\hat{i} + (5t - 8t^2)\hat{j}$ |
| Velocity | $\vec{v}(t) = (6t)\hat{i} + (5 - 16t)\hat{j}$ |
| Acceleration | $\vec{a}(t) = 6\hat{i} - 16\hat{j}$ |

---

## Interpretation

**Velocity $\vec{v}(t) = 6t\hat{i} + (5 - 16t)\hat{j}$**

- The horizontal velocity ($6t$) starts at zero and increases linearly with time — the object accelerates to the right.
- The vertical velocity ($5 - 16t$) starts at $5$ and decreases linearly — the object initially moves upward, then slows, stops vertically at $t = \dfrac{5}{16}$, and then moves downward.

**Acceleration $\vec{a}(t) = 6\hat{i} - 16\hat{j}$**

- Constant horizontal acceleration of $6$ units in the $+x$ direction.
- Constant downward acceleration of $16$ units in the $-y$ direction.
- Because the acceleration is constant, this is an example of **uniformly accelerated motion** in two dimensions.

---

*Solved using component-wise differentiation of vector functions.*
