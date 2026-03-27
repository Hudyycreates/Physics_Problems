# Problem 4 — Energy & Momentum

## Conceptual Intro — Two Laws, One Problem

This problem is a **two-act story**:

- **Act 1 — The Slide:** Frictionless, no collision. Energy is conserved → height becomes speed.
- **Act 2 — The Collision:** Blocks stick together (perfectly inelastic). Momentum is conserved — energy is **not**.

> ⚠️ You cannot use energy conservation across the collision, only momentum.
> Each law applies to its own phase.

---

## Given Information

| Symbol | Meaning | Value |
|--------|---------|-------|
| $m_1$ | Sliding block mass | $0.5\ \text{kg}$ |
| $m_2$ | Stationary block mass | $1.5\ \text{kg}$ |
| $h$ | Starting height | $3.0\ \text{m}$ |
| $g$ | Gravity | $9.8\ \text{m/s}^2$ |

---

## Act 1 — The Slide (Conservation of Energy)

$$mgh = \frac{1}{2}mv^2$$

Mass cancels — speed at the bottom doesn't depend on mass:

$$v_1 = \sqrt{2gh} = \sqrt{2 \times 9.8 \times 3.0} = \sqrt{58.8}$$

$$\boxed{v_1 \approx 7.67\ \text{m/s}}$$

---

## Act 2 — The Collision (Conservation of Momentum)

$$m_1 v_1 + m_2 \times 0 = (m_1 + m_2)v_f$$

$$v_f = \frac{m_1 v_1}{m_1 + m_2} = \frac{0.5 \times 7.67}{2.0}$$

$$\boxed{v_f \approx 1.92\ \text{m/s}}$$

---

## Sanity Check — Where Did the Energy Go?

$$KE_{before} = \frac{1}{2}(0.5)(7.67)^2 \approx 14.7\ \text{J}$$

$$KE_{after} = \frac{1}{2}(2.0)(1.92)^2 \approx 3.69\ \text{J}$$

$$\Delta KE \approx 11.0\ \text{J lost} \quad (\approx 75\%\ \text{of energy lost})$$

> ✅ Momentum conserved. ✅ Energy lost in collision — expected for perfectly inelastic collisions!

---

## Common Mistakes

- ❌ Using energy conservation through the collision — energy is lost when they stick
- ❌ Forgetting $m_2$ is at rest — its initial momentum is zero
- ❌ Using wrong mass after collision — it's $m_1 + m_2$, not just $m_1$

---

## What If the Track Had Friction?

$v_1$ at the bottom would be **lower** → less momentum into the collision → smaller $v_f$.
The collision math works the same way — just start Act 2 with a smaller number.
