## Problem 4: Phase Difference

###  Conceptual Introduction

A wave repeats itself over one full wavelength $\lambda$. One complete
repetition corresponds to a phase change of $2\pi$ radians (one full cycle).

So the relationship between a **spatial separation** $\Delta x$ and the
**phase difference** $\Delta\phi$ it represents is simply a proportion:

$$\frac{\Delta\phi}{2\pi} = \frac{\Delta x}{\lambda}$$

This tells us: *what fraction of a full wavelength is the separation?*
That same fraction of $2\pi$ is the phase difference.

---

### 📐 Given Information

| Symbol | Meaning | Value |
|--------|---------|-------|
| $\Delta x$ | Spatial separation between two points | $\lambda / 3$ |

---

### 🔺 Step 1 — Write the Phase Difference Formula

Rearranging the proportion above:

$$\Delta\phi = \frac{2\pi}{\lambda} \cdot \Delta x$$

The quantity $\dfrac{2\pi}{\lambda}$ is the **wavenumber** $k$, so this
is equivalently written as:

$$\Delta\phi = k \cdot \Delta x$$

---

### 🔺 Step 2 — Substitute $\Delta x = \lambda/3$

$$\Delta\phi = \frac{2\pi}{\lambda} \times \frac{\lambda}{3}$$

The $\lambda$ cancels:

$$\Delta\phi = \frac{2\pi}{3}$$

$$\boxed{\Delta\phi = \frac{2\pi}{3}\ \text{rad} \approx 2.094\ \text{rad} \approx 120°}$$

---

###  Building Physical Intuition

It helps to see how phase difference scales with separation:

| Separation $\Delta x$ | Phase difference $\Delta\phi$ | In degrees |
|-----------------------|-------------------------------|------------|
| $0$ | $0$ | $0°$ |
| $\lambda/4$ | $\pi/2$ | $90°$ |
| $\lambda/3$ | $2\pi/3$ | $120°$ ← **this problem** |
| $\lambda/2$ | $\pi$ | $180°$ (perfectly out of phase) |
| $\lambda$ | $2\pi$ | $360°$ (perfectly in phase again) |

At $\Delta\phi = \pi$ (separation $= \lambda/2$), the two points are at
**opposite** displacements at all times — if one is at a crest, the other
is at a trough. This is **destructive interference** for two equal-amplitude waves.

---

###  Common Mistakes

- ❌ **Using $\Delta\phi = \Delta x / \lambda$** — this gives a dimensionless
  fraction, not radians. Always multiply by $2\pi$
- ❌ **Confusing $\lambda/3$ separation with $120°$ phase and then second-guessing
  it** — it is exactly correct: one third of a cycle = one third of $360°$

---

###  What If the Separation Were $2\lambda/3$?

$$\Delta\phi = \frac{2\pi}{\lambda} \times \frac{2\lambda}{3} = \frac{4\pi}{3}\ \text{rad} = 240°$$

This is equivalent (by symmetry) to $-\frac{2\pi}{3}$ radians, or a phase
lag of $120°$ — the wave measured at the second point appears to be
$2/3$ of a cycle **behind** the first.
