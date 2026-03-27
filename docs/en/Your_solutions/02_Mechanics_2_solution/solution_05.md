# Problem 5 — Inelastic Collision

## Conceptual Intro — What Makes a Collision "Inelastic"?

| Collision Type | Objects | Kinetic Energy |
|---------------|---------|----------------|
| **Elastic** | Bounce apart | ✅ Conserved |
| **Inelastic** | Some deformation | ❌ Partially lost |
| **Perfectly Inelastic** | Stick together | ❌ Maximum loss |

> 🎯 "Jumps onto" = they stick together = perfectly inelastic by definition.

---

## Given Information

| Symbol | Meaning | Value |
|--------|---------|-------|
| $m_r$ | Runner mass | $70\ \text{kg}$ |
| $v_r$ | Runner's initial speed | $3\ \text{m/s}$ |
| $m_c$ | Cart mass | $140\ \text{kg}$ |
| $v_c$ | Cart's initial speed | $0\ \text{m/s}$ |

---

## Step 1 — Conservation of Momentum

$$m_r v_r + m_c v_c = (m_r + m_c)v_f$$

$$v_f = \frac{m_r v_r}{m_r + m_c} = \frac{70 \times 3}{70 + 140} = \frac{210}{210}$$

$$\boxed{v_f = 1.0\ \text{m/s}}$$

---

## Step 2 — Is Kinetic Energy Conserved?

$$KE_{before} = \frac{1}{2}(70)(3)^2 = 315\ \text{J}$$

$$KE_{after} = \frac{1}{2}(210)(1.0)^2 = 105\ \text{J}$$

$$\Delta KE = 210\ \text{J lost} \approx \boxed{66.7\%\ \text{of KE lost}}$$

> ❌ Kinetic energy is **not** conserved — lost to heat, sound, and deformation.

---

## Full Picture Summary

| Quantity | Before | After |
|---------|--------|-------|
| Runner speed | $3.0\ \text{m/s}$ | $1.0\ \text{m/s}$ |
| Cart speed | $0\ \text{m/s}$ | $1.0\ \text{m/s}$ |
| Total momentum | $210\ \text{kg·m/s}$ | $210\ \text{kg·m/s}$ ✅ |
| Total KE | $315\ \text{J}$ | $105\ \text{J}$ ❌ |

---

## Common Mistakes

- ❌ Averaging the speeds — mass weighs into the result, not just velocity
- ❌ Expecting energy to be conserved — energy loss is the answer, not an error
- ❌ Forgetting the cart has zero initial momentum

---

## What If the Cart Were Moving Too?

If the cart rolled **toward** the runner at $1\ \text{m/s}$ (negative direction):

$$v_f = \frac{(70)(3) + (140)(-1)}{210} = \frac{70}{210} \approx 0.33\ \text{m/s}$$

> Direction matters — always assign signs to velocities before solving!
