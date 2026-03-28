# Problem 10 — Force Field and Power

## Given

$$m = 0.5\ \text{kg}$$
$$x = 5t^2 - t, \quad y = 2t^3, \quad z = -3t + 2$$

---

## Velocity

$$\boxed{\vec{v}(t) = (10t-1,\ 6t^2,\ -3)\ \text{m/s}}$$

## Momentum

$$\boxed{\vec{p}(t) = m\vec{v} = (5t-0.5,\ 3t^2,\ -1.5)\ \text{kg·m/s}}$$

## Acceleration

$$\boxed{\vec{a}(t) = (10,\ 12t,\ 0)\ \text{m/s}^2}$$

> No $z$ acceleration — $z$-motion is uniform (constant velocity).

## Force

$$\boxed{\vec{F}(t) = m\vec{a} = (5,\ 6t,\ 0)\ \text{N}}$$

## Power

$$P = \vec{F} \cdot \vec{v} = 5(10t-1) + 6t(6t^2) + 0$$

$$\boxed{P(t) = 36t^3 + 50t - 5\ \text{W}}$$

---

## Check at $t = 0$

| Quantity | Value |
|----------|-------|
| $\vec{v}$ | $(-1, 0, -3)\ \text{m/s}$ |
| $\vec{F}$ | $(5, 0, 0)\ \text{N}$ |
| $P$ | $-5\ \text{W}$ (force opposes motion → negative power) |
