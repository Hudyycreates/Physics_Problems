## Problem 7: Standing Wave Modes

###  Conceptual Introduction

A string fixed at both ends supports standing waves only when the
boundary conditions are satisfied: both endpoints must be **nodes**
(zero displacement at all times).

For a string of length $L$, the general rule for the $n$-th harmonic is:

$$L = n \cdot \frac{\lambda}{2}, \qquad n = 1, 2, 3, 4, \ldots$$

Each harmonic $n$ has exactly $n$ **antinodes** (points of maximum
displacement). So a standing wave with **four antinodes** is the
**fourth harmonic** ($n = 4$).

The key insight is that more antinodes = more half-wavelengths fitting
into the string = **shorter wavelength**.

---

### 📐 Given Information

| Symbol | Meaning | Value |
|--------|---------|-------|
| $L$ | Length of string | $80\ \text{cm} = 0.80\ \text{m}$ |
| Number of antinodes | Identifies harmonic | $4$ antinodes $\Rightarrow n = 4$ |

---

### 🔺 Step 1 — Write the General Harmonic Condition

For the $n$-th harmonic, $n$ half-wavelengths fit into the string length:

$$L = n \cdot \frac{\lambda_n}{2}$$

Solving for $\lambda_n$:

$$\lambda_n = \frac{2L}{n}$$

---

### 🔺 Step 2 — Identify the Harmonic Number

Four antinodes means the fourth harmonic: $n = 4$.

---

### 🔺 Step 3 — Calculate the Wavelength

$$\lambda_4 = \frac{2L}{n} = \frac{2 \times 0.80\ \text{m}}{4}$$

$$\lambda_4 = \frac{1.60}{4}$$

$$\boxed{\lambda_4 = 0.40\ \text{m} = 40\ \text{cm}}$$

---

###  Sanity Check — Does It Fit?

If $\lambda_4 = 0.40\ \text{m}$, then four half-wavelengths span:

$$4 \times \frac{0.40}{2} = 4 \times 0.20 = 0.80\ \text{m} = L \quad \checkmark$$

Exactly four half-wavelengths fit into the string. ✅

---

###  Full Harmonic Comparison for This String

| Harmonic $n$ | Antinodes | Wavelength $\lambda_n = 2L/n$ | Relative to $\lambda_1$ |
|:---:|:---:|:---:|:---:|
| $n = 1$ | 1 | $1.60\ \text{m}$ | $\lambda_1$ |
| $n = 2$ | 2 | $0.80\ \text{m}$ | $\lambda_1 / 2$ |
| $n = 3$ | 3 | $0.533\ \text{m}$ | $\lambda_1 / 3$ |
| $n = 4$ | 4 | $0.40\ \text{m}$ | $\lambda_1 / 4$ ← **this problem** |
| $n = 5$ | 5 | $0.32\ \text{m}$ | $\lambda_1 / 5$ |

Notice: as $n$ increases (more antinodes), the wavelength **decreases**
proportionally. The $n$-th harmonic has a wavelength exactly $1/n$ of the
fundamental wavelength.

---

###  Common Mistakes

- ❌ **Using $L = n\lambda$ instead of $L = n\lambda/2$** — each harmonic
  fits $n$ **half**-wavelengths, not $n$ full wavelengths
- ❌ **Confusing nodes and antinodes** — nodes are zero-displacement points
  (always at the fixed ends); antinodes are maximum-displacement points.
  The problem specifies **antinodes** to identify $n$
- ❌ **Forgetting to convert cm to m** — $80\ \text{cm} = 0.80\ \text{m}$

---

### What If the Same String Had a Wave Speed of 200 m/s?

We could find the frequency of the fourth harmonic:

$$f_4 = \frac{v}{\lambda_4} = \frac{200\ \text{m/s}}{0.40\ \text{m}} = 500\ \text{Hz}$$

And verify using the harmonic rule $f_n = nf_1$:

$$f_1 = \frac{v}{\lambda_1} = \frac{200}{1.60} = 125\ \text{Hz}$$

$$f_4 = 4 \times 125 = 500\ \text{Hz} \quad \checkmark$$
