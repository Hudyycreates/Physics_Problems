## Problem 6: Wave Equation

###  Conceptual Introduction

When a wave is written in the standard form:

$$y(x,t) = A\sin(kx - \omega t)$$

every wave property can be read off **directly from the coefficients**:

| Coefficient | Symbol | What it tells you |
|-------------|--------|-------------------|
| Coefficient in front | $A$ | Amplitude |
| Coefficient of $x$ | $k$ | Wavenumber $= 2\pi/\lambda$ |
| Coefficient of $t$ | $\omega$ | Angular frequency $= 2\pi f$ |
| Ratio $\omega/k$ | — | Wave speed $v$ |

The key is to identify these coefficients correctly before applying any formula.

---

###  Given Equation

$$y(x,t) = 0.05\sin(2\pi x - 50\pi t)$$

where $x$ and $y$ are in **metres** and $t$ is in **seconds**.

Matching to the standard form $y = A\sin(kx - \omega t)$, we can immediately read:

$$A = 0.05\ \text{m}, \qquad k = 2\pi\ \text{rad/m}, \qquad \omega = 50\pi\ \text{rad/s}$$

---

### 🧮 Part a — Amplitude $A$

The amplitude is the coefficient in front of the sine function.
It is the maximum displacement from equilibrium:

$$\boxed{A = 0.05\ \text{m} = 5\ \text{cm}}$$

---

### 🧮 Part b — Wavelength $\lambda$

The wavenumber $k$ is related to wavelength by:

$$k = \frac{2\pi}{\lambda} \implies \lambda = \frac{2\pi}{k}$$

Substituting $k = 2\pi$:

$$\lambda = \frac{2\pi}{2\pi}$$

$$\boxed{\lambda = 1\ \text{m}}$$

---

### 🧮 Part c — Frequency $f$

The angular frequency $\omega$ is related to ordinary frequency $f$ by:

$$\omega = 2\pi f \implies f = \frac{\omega}{2\pi}$$

Substituting $\omega = 50\pi$:

$$f = \frac{50\pi}{2\pi}$$

$$\boxed{f = 25\ \text{Hz}}$$

---

### 🧮 Part d — Wave Speed $v$

Wave speed can be found two ways — both must give the same answer.

**Method 1:** Using the fundamental wave relationship:

$$v = f\lambda = 25\ \text{Hz} \times 1\ \text{m}$$

**Method 2:** Using the ratio of angular frequency to wavenumber:

$$v = \frac{\omega}{k} = \frac{50\pi}{2\pi}$$

Both give:

$$\boxed{v = 25\ \text{m/s}}$$

---

###  Full Results Summary

| Property | Symbol | Formula used | Value |
|----------|--------|-------------|-------|
| Amplitude | $A$ | Read directly | $0.05\ \text{m}$ |
| Wavelength | $\lambda$ | $\lambda = 2\pi/k$ | $1\ \text{m}$ |
| Frequency | $f$ | $f = \omega/2\pi$ | $25\ \text{Hz}$ |
| Wave speed | $v$ | $v = f\lambda = \omega/k$ | $25\ \text{m/s}$ |
| Period | $T$ | $T = 1/f$ | $0.04\ \text{s}$ |

---

###  Common Mistakes

- ❌ **Reading $A = \sin(...)$** — the amplitude is only the number in front,
  never the entire sine term
- ❌ **Confusing $k$ (wavenumber) with $K$ (spring constant)** — in wave
  equations, $k = 2\pi/\lambda$ always
- ❌ **Forgetting the $2\pi$ when finding $f$ from $\omega$** — $\omega \neq f$.
  Always divide $\omega$ by $2\pi$ to get $f$
- ❌ **Not checking units** — confirm that $k$ is in $\text{rad/m}$ and
  $\omega$ is in $\text{rad/s}$ before applying formulas

---

###  What Does the Wave Look Like at $t = 0$?

At $t = 0$, the equation reduces to:

$$y(x,\ 0) = 0.05\sin(2\pi x)$$

This is a sine wave with wavelength $1\ \text{m}$ and amplitude $5\ \text{cm}$,
starting at $y = 0$ when $x = 0$, reaching a crest of $5\ \text{cm}$ at
$x = 0.25\ \text{m}$, returning to zero at $x = 0.5\ \text{m}$, reaching a
trough at $x = 0.75\ \text{m}$, and completing the cycle at $x = 1\ \text{m}$.
