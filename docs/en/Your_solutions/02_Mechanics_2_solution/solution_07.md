# Problem 7 — Dynamics with Friction

## Conceptual Intro

Two friction surfaces act simultaneously on the 10 kg block:
- The stationary 5 kg block (tied to wall) drags from **above**
- The ground drags from **below**

> ⚠️ The 5 kg block doesn't move — but it still applies friction to
> the moving block. The wall constraint makes the problem solvable in one step.

---

## Given

| Symbol | Meaning | Value |
|--------|---------|-------|
| $m_1$ | Top block (tied) | $5\ \text{kg}$ |
| $m_2$ | Bottom block (moving) | $10\ \text{kg}$ |
| $F$ | Applied force | $45\ \text{N}$ |
| $\mu_k$ | Kinetic friction | $0.2$ |

---

## Step 1 — Normal Forces

$$N_1 = m_1 g = 5 \times 9.8 = 49\ \text{N}$$

$$N_2 = (m_1 + m_2)g = 15 \times 9.8 = 147\ \text{N}$$

---

## Step 2 — Friction Forces

$$f_1 = \mu_k N_1 = 0.2 \times 49 = 9.8\ \text{N}$$

$$f_2 = \mu_k N_2 = 0.2 \times 147 = 29.4\ \text{N}$$

---

## Step 3 — Newton's Second Law on $m_2$

$$F_{net} = 45 - 9.8 - 29.4 = 5.8\ \text{N}$$

$$a = \frac{F_{net}}{m_2} = \frac{5.8}{10}$$

$$\boxed{a = 0.58\ \text{m/s}^2}$$

---

## Force Breakdown

| Force | Direction | Magnitude |
|-------|-----------|-----------|
| Applied $F$ | Forward | $45.0\ \text{N}$ |
| $f_1$ (top block) | Backward | $9.8\ \text{N}$ |
| $f_2$ (ground) | Backward | $29.4\ \text{N}$ |
| **Net** | **Forward** | **$5.8\ \text{N}$** |

## Common Mistakes

- ❌ Forgetting friction from the tied top block
- ❌ Using only $m_2 g$ for ground normal force — ground supports both blocks
- ❌ Treating the 5 kg block as moving — it's fixed to the wall
