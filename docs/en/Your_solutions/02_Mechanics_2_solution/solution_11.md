# Problem 11 — Dynamics with Time-Dependent Force

## Given

$$m = 3\ \text{kg}, \quad \vec{F}(t) = (15t,\ 3t-12,\ -6t^2)\ \text{N}$$
$$\vec{r}_0 = (5, 2, -3)\ \text{m}, \quad \vec{v}_0 = (2, 0, 1)\ \text{m/s}$$

---

## Step 1 — Acceleration

$$\boxed{\vec{a}(t) = \frac{\vec{F}}{m} = (5t,\ t-4,\ -2t^2)\ \text{m/s}^2}$$

---

## Step 2 — Velocity

$$\boxed{\vec{v}(t) = \left(2 + \frac{5t^2}{2},\quad \frac{t^2}{2} - 4t,\quad 1 - \frac{2t^3}{3}\right)\ \text{m/s}}$$

---

## Step 3 — Position

$$\boxed{\vec{r}(t) = \left(5 + 2t + \frac{5t^3}{6},\quad 2 + \frac{t^3}{6} - 2t^2,\quad -3 + t - \frac{t^4}{6}\right)\ \text{m}}$$

---

## Verification at $t = 0$

| Quantity | Expected | Computed |
|----------|---------|----------|
| $\vec{v}(0)$ | $(2, 0, 1)$ | $(2, 0, 1)$ ✅ |
| $\vec{r}(0)$ | $(5, 2, -3)$ | $(5, 2, -3)$ ✅ |
