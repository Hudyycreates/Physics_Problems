# Section 3 — Problem 10: Superposition of Wave Sources

##  Conceptual Introduction

A point source located at position $\vec{r}_0$ emits circular (or spherical)
waves that spread outward in all directions. The displacement at any
field point $\vec{r}$ due to that single source is:

$$u(\vec{r}, t) = \frac{A}{|\vec{r} - \vec{r}_0|^\alpha}\sin\!\left(k|\vec{r}-\vec{r}_0| - \omega t\right)$$

| Symbol | Meaning |
|--------|---------|
| $|\vec{r} - \vec{r}_0|$ | Distance from the source to the field point |
| $A$ | Source amplitude |
| $\alpha \in [0, 2]$ | Spatial decay exponent — controls how fast amplitude falls with distance |
| $k = 2\pi/\lambda$ | Wavenumber |
| $\omega$ | Angular frequency |

When $\alpha = 0$: amplitude is constant everywhere (plane wave approximation).
When $\alpha = 1$: amplitude falls as $1/r$ (correct for 2D circular waves, e.g. ripples on water).
When $\alpha = 2$: amplitude falls as $1/r^2$ (3D spherical wave intensity law).

When multiple sources are present, the **superposition principle** gives:

$$u_{total}(\vec{r}, t) = \sum_{i} \frac{A}{|\vec{r} - \vec{r}_i|^\alpha}\sin\!\left(k|\vec{r}-\vec{r}_i| - \omega t\right)$$

The resulting pattern of constructive and destructive interference
depends on the positions of the sources, the wavelength, and $\alpha$.

---

## Mathematical Setup for Simulation

### Step 1 — Discretize the field

Divide the simulation canvas into a grid of pixels. Each pixel at position
$(p_x, p_y)$ is a field point $\vec{r}$.

### Step 2 — Precompute distances

For each source at $(s_x, s_y)$, precompute the distance to every pixel:

$$r_i(p_x, p_y) = \sqrt{(p_x - s_x)^2 + (p_y - s_y)^2}$$

This is done once when a source is added, not every frame. The distance
does not change over time — only the time argument $\omega t$ advances.

### Step 3 — Evaluate field at each frame

At time $t$, the field value at pixel $(p_x, p_y)$ is:

$$u(p_x, p_y, t) = \sum_{i=1}^{N} \frac{A}{r_i^{\,\alpha}} \cdot \sin(k\, r_i - \omega t)$$

### Step 4 — Normalize and colorize

Normalize $u$ by its maximum absolute value so the color scale always
uses the full dynamic range regardless of the number of sources:

$$u_{norm} = \frac{u}{\max|u|}$$

Map $u_{norm} \in [-1, 1]$ to a diverging color map
(e.g. blue for positive / crests, red for negative / troughs, black for zero).

### Step 5 — Performance: sin lookup table

Calling `Math.sin()` per pixel per frame is too slow for real-time rendering.
Instead, precompute a table of $N_{LUT}$ sine values:

$$\text{LUT}[i] = \sin\!\left(\frac{2\pi i}{N_{LUT}}\right), \quad i = 0, 1, \ldots, N_{LUT}-1$$

Then approximate $\sin(\theta)$ as:

$$\sin(\theta) \approx \text{LUT}\!\left[\left\lfloor\frac{\theta \cdot N_{LUT}}{2\pi}\right\rfloor \bmod N_{LUT}\right]$$

With $N_{LUT} = 8192$ this gives excellent accuracy at $\sim 5\times$ the
speed of the native function.

---


---

## Key Physics to Observe

| $\alpha$ value | Amplitude behaviour | Pattern type |
|----------------|---------------------|--------------|
| $\alpha = 0$ | Constant everywhere | Uniform amplitude interference |
| $\alpha = 1$ | Falls as $1/r$ | 2D circular wave (water ripple) |
| $\alpha = 2$ | Falls as $1/r^2$ | 3D spherical wave cross-section |

With two sources, concentric rings of constructive interference (bright bands)
and destructive interference (dark bands) appear — this is the same physics
as Young's double-slit experiment. With more sources arranged in a line,
a **phased array** pattern emerges — the basis of radar, sonar, and 5G antennas.

---

##  Common Mistakes

- ❌ **Dividing by zero at the source position** — always add a small offset
  (e.g. $+0.5$) to distances to avoid `Infinity` values at $r = 0$
- ❌ **Recomputing distances every frame** — distances are fixed by geometry;
  only the phase $\omega t$ changes each frame. Precompute and cache.
- ❌ **Not normalizing the field before colorizing** — without normalization,
  adding more sources makes all previous colors saturate and the pattern
  becomes unreadable
