# Problem 9 — Vertical Throw with Drag

## Conceptual Intro

Without drag: symmetric rise and fall, constant deceleration $g$.
With drag: **both** gravity and drag oppose upward motion → lower peak,
faster ascent deceleration. Descent is slower — approaches terminal velocity.

---

## Given

$$m\frac{dv}{dt} = -mg - kv, \quad v(0) = v_0,\ x(0) = 10$$

---

## Part 1 — Analytical Solution

$$\frac{dv}{dt} + \beta v = -g, \quad \beta = \frac{k}{m}$$

$$\boxed{v(t) = \left(v_0 + \frac{g}{\beta}\right)e^{-\beta t} - \frac{g}{\beta}}$$

$$\boxed{x(t) = x_0 + \frac{v_0 + g/\beta}{\beta}\left(1 - e^{-\beta t}\right) - \frac{g}{\beta}t}$$

---

## Part 2 — Maximum Height

Set $v(t_{max}) = 0$:

$$t_{max} = \frac{1}{\beta}\ln\!\left(1 + \frac{\beta v_0}{g}\right)$$

Substitute into $x(t)$ to get $x_{max}$.

---

## Part 3 — Comparison

| | With Drag | Without Drag |
|--|-----------|--------------|
| $t_{max}$ | $\frac{1}{\beta}\ln(1+\beta v_0/g)$ | $v_0/g$ |
| $x_{max}$ | $x(t_{max})$ | $x_0 + v_0^2/(2g)$ |
| Symmetry | ❌ Asymmetric | ✅ Symmetric |

---

## Part 4 — Numerical Simulation (JavaScript)
```javascript
// Euler method for mdv/dt = -mg - kv
const g = 9.8, dt = 0.01;
let v = v0, x = x0;
while (x >= 0) {
  v += (-g - (k/m)*v) * dt;
  x += v * dt;
}
```

> Decrease $dt$ for higher accuracy. RK4 gives better results for stiff drag values.
