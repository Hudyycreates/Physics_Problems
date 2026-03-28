# Problem 7 — Dynamics with Friction

## Conceptual Intro

The 10 kg block has **two friction surfaces acting simultaneously**:
- **Top surface** (against stationary 5 kg block tied to wall)
- **Bottom surface** (against the ground)

Both friction forces point backward. The 5 kg block cannot move — but
it still contributes friction to the 10 kg block beneath it.

---

## Given

| Symbol | Meaning | Value |
|--------|---------|-------|
| $m_1$ | Top block (tied, stationary) | $5\ \text{kg}$ |
| $m_2$ | Bottom block (moving) | $10\ \text{kg}$ |
| $F$ | Applied force | $45\ \text{N}$ |
| $\mu_k$ | Kinetic friction (all surfaces) | $0.2$ |

---

## Step 1 — Normal Forces

**Surface A** (between blocks — only $m_1$ presses down):

$$N_A = m_1 g = 5 \times 9.8 = 49\ \text{N}$$

**Surface B** (ground — supports both blocks):

$$N_B = (m_1 + m_2)g = 15 \times 9.8 = 147\ \text{N}$$

> ⚠️ The ground holds up **both** blocks — don't use only $m_2 g$ here.

---

## Step 2 — Friction Forces on $m_2$

$$f_A = \mu_k N_A = 0.2 \times 49 = 9.8\ \text{N} \quad (\text{backward})$$

$$f_B = \mu_k N_B = 0.2 \times 147 = 29.4\ \text{N} \quad (\text{backward})$$

$$f_{total} = 9.8 + 29.4 = 39.2\ \text{N}$$

---

## Step 3 — Newton's Second Law on $m_2$

$$F_{net} = F - f_A - f_B = 45 - 9.8 - 29.4 = 5.8\ \text{N}$$

$$a = \frac{F_{net}}{m_2} = \frac{5.8}{10}$$

$$\boxed{a = 0.58\ \text{m/s}^2}$$

---

## Step 4 — Verify Wall Tension

Forces on $m_1$ horizontally: $f_A$ forward, $T$ backward.
Since $m_1$ doesn't accelerate: $T = f_A = 9.8\ \text{N}$ ✅

---

## Force Summary

| Force | Direction | Magnitude |
|-------|-----------|-----------|
| Applied $F$ | Forward | $45.0\ \text{N}$ |
| $f_A$ (top block) | Backward | $9.8\ \text{N}$ |
| $f_B$ (ground) | Backward | $29.4\ \text{N}$ |
| **Net** | **Forward** | **$5.8\ \text{N}$** |
| **Acceleration** | **Forward** | **$0.58\ \text{m/s}^2$** |

---

## Common Mistakes

- ❌ Using $N_B = m_2 g$ — the ground supports both blocks
- ❌ Forgetting $f_A$ — the tied block still applies backward friction
- ❌ Including the 5 kg block in Newton's law — it doesn't accelerate
