# Section 3 — Problem 11: Young's Two-Slit Interference

##  Conceptual Introduction

Young's double-slit experiment (1801) was the first convincing demonstration
that light behaves as a wave. Two narrow slits act as **coherent point sources**
— they emit waves with a fixed phase relationship (here, in phase).

The total displacement at any field point $\vec{r}$ is the **sum of the two
partial waves**:

$$u(\vec{r}, t) = \frac{A}{|\vec{r}-\vec{r}_1|}\sin\!\left(k|\vec{r}-\vec{r}_1| - \omega t\right) + \frac{A}{|\vec{r}-\vec{r}_2|}\sin\!\left(k|\vec{r}-\vec{r}_2| - \omega t\right)$$

where $\vec{r}_1$ and $\vec{r}_2$ are the positions of the two slits.

| Symbol | Meaning |
|--------|---------|
| $d = |\vec{r}_1 - \vec{r}_2|$ | Slit separation |
| $\lambda = 2\pi/k$ | Wavelength |
| $A$ | Amplitude of each source |
| $r_1, r_2$ | Distances from slits 1 and 2 to field point |

---

## The Interference Condition

At a distant screen, the path difference between the two waves determines
whether interference is constructive or destructive:

**Path difference:** $\Delta r = r_1 - r_2 \approx d\sin\theta$
(for a screen far from the slits, small angle approximation)

**Constructive interference** (bright fringe):

$$\Delta r = n\lambda, \quad n = 0, \pm1, \pm2, \ldots$$

$$\Rightarrow d\sin\theta_n = n\lambda \Rightarrow \theta_n = \arcsin\!\left(\frac{n\lambda}{d}\right)$$

**Destructive interference** (dark fringe):

$$\Delta r = \left(n + \frac{1}{2}\right)\lambda$$

The **fringe spacing** on a screen at distance $L$:

$$\Delta y = \frac{\lambda L}{d}$$

Increasing $\lambda$ (longer wavelength) widens the fringes.
Increasing $d$ (wider slit separation) narrows them.

---

## Mathematical Setup for Simulation

### Step 1 — Slit positions

Place both slits at $x = 0$ (left edge of canvas), symmetrically about the
centre:

$$\vec{r}_1 = (0,\; H/2 - d/2), \qquad \vec{r}_2 = (0,\; H/2 + d/2)$$

where $H$ is the canvas height and $d$ is the slit separation.

### Step 2 — Precompute distances

For every pixel $(p_x, p_y)$:

$$r_1 = \sqrt{p_x^2 + (p_y - y_1)^2} + \varepsilon, \qquad r_2 = \sqrt{p_x^2 + (p_y - y_2)^2} + \varepsilon$$

($\varepsilon = 0.5$ to prevent division by zero at the slit positions.)

These are recomputed only when $d$ changes.

### Step 3 — Field at each frame

$$u(p_x, p_y, t) = \frac{A}{r_1}\sin(kr_1 - \omega t) + \frac{A}{r_2}\sin(kr_2 - \omega t)$$

### Step 4 — Time-averaged intensity

The instantaneous field oscillates too quickly to see the fringe pattern clearly.
The **time-averaged intensity** at each point is:

$$I \propto \langle u^2 \rangle$$

In practice, update a running average using an exponential moving average (EMA):

$$I_{n+1} = (1-\alpha_{\text{EMA}})\,I_n + \alpha_{\text{EMA}}\,u^2$$

With $\alpha_{\text{EMA}} \approx 0.05$, the intensity profile builds up over
roughly 20 frames, showing the steady-state fringe pattern.

---
---

## Key Physics to Observe in the Simulation

| Action | What you see | Why |
|--------|-------------|-----|
| Increase $\lambda$ (larger wavelength) | Fringe spacing **widens** | $\Delta y = \lambda L/d$ — spacing proportional to $\lambda$ |
| Increase $d$ (wider slits) | Fringe spacing **narrows** | More slits per wavelength → tighter pattern |
| Set $d < \lambda$ | Fringes **disappear** | Path difference cannot reach $\lambda$ — constructive condition never met |
| Add more wavelengths | More fringes across screen | Higher-order maxima become visible |

---

## Analytical Fringe Positions

For a screen at distance $L$ from the slits, the $n$-th bright fringe
appears at:

$$y_n = \frac{n\lambda L}{d}, \quad n = 0, \pm1, \pm2, \ldots$$

The central fringe ($n = 0$) always falls on the axis of symmetry regardless
of $\lambda$ or $d$.

The intensity envelope at the screen (ignoring single-slit diffraction) is:

$$I(\theta) = 4A^2\cos^2\!\left(\frac{\pi d \sin\theta}{\lambda}\right)$$

Maximum intensity $4A^2$ occurs at constructive interference — exactly
four times the single-source intensity $A^2$, not twice. This is because
amplitude doubles at a constructive point, and intensity scales as amplitude squared.

---

##  Common Mistakes

- ❌ **Using $I = 2A^2$ for constructive interference** — amplitude doubles
  ($2A$), so intensity is $(2A)^2 = 4A^2$, not $2A^2$
- ❌ **Forgetting the $1/r$ amplitude factor** — each partial wave decays with
  distance; the two sources don't contribute equal amplitudes unless the
  field point is equidistant from both slits
- ❌ **Confusing path difference with phase difference** — path difference
  $\Delta r$ and phase difference $\Delta\phi = k\Delta r = 2\pi\Delta r/\lambda$
  are related by the factor $k$. Constructive interference occurs when
  $\Delta\phi = 2\pi n$, which is equivalent to $\Delta r = n\lambda$
