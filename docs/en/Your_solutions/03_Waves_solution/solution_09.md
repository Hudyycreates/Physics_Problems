# Section 3 — Problem 9: Damped Harmonic Oscillator

##  Conceptual Introduction

The damped harmonic oscillator describes every physical system that oscillates
while losing energy — a spring with friction, an LC circuit with resistance,
a pendulum in air. The equation of motion is:

$$m\ddot{x} + b\dot{x} + kx = 0$$

Three forces act simultaneously:

| Term | Force | Role |
|------|-------|------|
| $-kx$ | Spring (restoring) | Always pulls back toward equilibrium |
| $-b\dot{x}$ | Damping (friction) | Always opposes velocity, removes energy |
| $m\ddot{x}$ | Inertia | Newton's second law |

The central question is: does the system oscillate, or does friction
overwhelm the spring? The answer depends entirely on the **ratio** of the
damping strength to the natural oscillation frequency.

---

## Part 1 — General Solution

### Step 1 — Trial Solution

We look for solutions of the form $x(t) = e^{\lambda t}$. Substituting:

$$m\lambda^2 e^{\lambda t} + b\lambda e^{\lambda t} + ke^{\lambda t} = 0$$

Dividing through by $e^{\lambda t}$ (never zero):

$$m\lambda^2 + b\lambda + k = 0 \quad \text{(characteristic equation)}$$

### Step 2 — Solve the Quadratic

$$\lambda = \frac{-b \pm \sqrt{b^2 - 4mk}}{2m}$$

### Step 3 — Introduce Natural Parameters

Define two quantities that appear throughout the theory:

$$\omega_0 = \sqrt{\frac{k}{m}} \quad \text{(natural angular frequency — no damping)}$$

$$\gamma = \frac{b}{2m} \quad \text{(damping rate)}$$

The roots become:

$$\lambda = -\gamma \pm \sqrt{\gamma^2 - \omega_0^2}$$

The entire classification hangs on the sign of the **discriminant**
$\Delta = \gamma^2 - \omega_0^2$.

---

## Part 2 — Classification of Cases

### Case 1: Underdamped — $b < 2\sqrt{mk}$, equivalently $\gamma < \omega_0$

The discriminant $\Delta < 0$, so the square root is imaginary.
Define the **damped angular frequency**:

$$\omega_d = \sqrt{\omega_0^2 - \gamma^2}$$

The two roots are complex conjugates: $\lambda = -\gamma \pm i\omega_d$

Using Euler's formula $e^{i\theta} = \cos\theta + i\sin\theta$, the
**general solution** is:

$$\boxed{x(t) = e^{-\gamma t}\bigl[C_1\cos(\omega_d t) + C_2\sin(\omega_d t)\bigr]}$$

**Physical interpretation:** The system **oscillates** at frequency $\omega_d$,
but the amplitude decays exponentially with envelope $e^{-\gamma t}$.
The oscillation frequency $\omega_d$ is always *lower* than the natural
frequency $\omega_0$ — damping slows the oscillation.

**Applying initial conditions** $x(0) = x_0$, $\dot{x}(0) = v_0$:

At $t = 0$: $\quad x_0 = e^0 \cdot C_1 \Rightarrow C_1 = x_0$

Differentiating $x(t)$ and evaluating at $t = 0$:

$$\dot{x}(0) = -\gamma C_1 + \omega_d C_2 = v_0 \Rightarrow C_2 = \frac{v_0 + \gamma x_0}{\omega_d}$$

---

### Case 2: Critically Damped — $b = 2\sqrt{mk}$, equivalently $\gamma = \omega_0$

The discriminant $\Delta = 0$: there is exactly **one repeated root**
$\lambda = -\gamma$.

A repeated root in a 2nd-order ODE always requires a special second
independent solution. If both solutions were $e^{-\gamma t}$, they would
be proportional and we could not satisfy two arbitrary initial conditions.
The correct second solution is $te^{-\gamma t}$:

**General solution:**

$$\boxed{x(t) = (C_1 + C_2 t)\,e^{-\gamma t}}$$

**Physical interpretation:** The system returns to equilibrium as fast as
possible **without oscillating**. This is the boundary case between
oscillatory and non-oscillatory behavior. It is used wherever fastest
non-oscillatory return is required — car shock absorbers, door dampers,
galvanometers.

**Applying initial conditions:**

At $t = 0$: $\quad C_1 = x_0$

Differentiating and evaluating at $t = 0$:
$\dot{x}(0) = C_2 - \gamma C_1 = v_0 \Rightarrow C_2 = v_0 + \gamma x_0$

---

### Case 3: Overdamped — $b > 2\sqrt{mk}$, equivalently $\gamma > \omega_0$

The discriminant $\Delta > 0$: both roots are **real and negative**.
Define:

$$\mu = \sqrt{\gamma^2 - \omega_0^2}$$

Then:

$$\lambda_1 = -\gamma + \mu < 0 \qquad \lambda_2 = -\gamma - \mu < 0$$

(Both are negative because $\mu = \sqrt{\gamma^2 - \omega_0^2} < \gamma$.)

**General solution:**

$$\boxed{x(t) = C_1 e^{\lambda_1 t} + C_2 e^{\lambda_2 t}}$$

**Physical interpretation:** The system returns to equilibrium **without
oscillating**, but more slowly than the critically damped case. It is the
sum of two decaying exponentials with different decay rates.

**Applying initial conditions:**

$$C_1 = \frac{v_0 - \lambda_2 x_0}{\lambda_1 - \lambda_2}, \qquad C_2 = x_0 - C_1$$

---

### Summary of All Three Cases

| Parameter | Underdamped | Critical | Overdamped |
|-----------|-------------|----------|------------|
| Condition | $b < 2\sqrt{mk}$ | $b = 2\sqrt{mk}$ | $b > 2\sqrt{mk}$ |
| Roots $\lambda$ | Complex: $-\gamma \pm i\omega_d$ | Real repeated: $-\gamma$ | Real distinct: $\lambda_1, \lambda_2$ |
| Solution form | $e^{-\gamma t}[C_1\cos\omega_d t + C_2\sin\omega_d t]$ | $(C_1 + C_2 t)e^{-\gamma t}$ | $C_1 e^{\lambda_1 t} + C_2 e^{\lambda_2 t}$ |
| Oscillates? | ✅ Yes | ❌ No | ❌ No |
| Return speed | Slow (oscillates past) | **Fastest** | Slow (sluggish) |

The **damping ratio** $\zeta = b/b_c = \gamma/\omega_0$ summarizes all cases:

$$\zeta < 1 \Rightarrow \text{underdamped}, \quad \zeta = 1 \Rightarrow \text{critical}, \quad \zeta > 1 \Rightarrow \text{overdamped}$$

---

## Part 3 — Numerical Solution: RK4 Method

To solve numerically, rewrite the second-order ODE as a
**system of two first-order ODEs**:

Let state vector $\mathbf{y} = (x,\, \dot{x}) = (x,\, v)$. Then:

$$\frac{dx}{dt} = v \qquad \frac{dv}{dt} = \frac{-bv - kx}{m}$$

This defines $\mathbf{f}(x, v) = \bigl(v,\ (-bv - kx)/m\bigr)$.

The **4th-order Runge-Kutta** scheme advances the state by step $\Delta t$:

$$k_1 = \mathbf{f}(\mathbf{y}_n)$$

$$k_2 = \mathbf{f}\!\left(\mathbf{y}_n + \tfrac{\Delta t}{2}\,k_1\right)$$

$$k_3 = \mathbf{f}\!\left(\mathbf{y}_n + \tfrac{\Delta t}{2}\,k_2\right)$$

$$k_4 = \mathbf{f}\!\left(\mathbf{y}_n + \Delta t\,k_3\right)$$

$$\mathbf{y}_{n+1} = \mathbf{y}_n + \frac{\Delta t}{6}(k_1 + 2k_2 + 2k_3 + k_4)$$

RK4 has **4th-order accuracy** — local error $\mathcal{O}(\Delta t^5)$, far
superior to Euler's method ($\mathcal{O}(\Delta t^2)$) for the same step size.
```python
import numpy as np
import matplotlib.pyplot as plt

def rk4_damped(m, b, k, x0, v0, t_end=20, dt=0.01):
    """
    Solves m*x'' + b*x' + k*x = 0 using RK4.
    Returns arrays: t, x, v
    """
    def f(state):
        x, v = state
        return np.array([v, (-b*v - k*x) / m])

    N     = int(t_end / dt)
    t     = np.linspace(0, t_end, N+1)
    state = np.array([x0, v0], dtype=float)
    xs    = np.zeros(N+1)
    vs    = np.zeros(N+1)
    xs[0], vs[0] = x0, v0

    for i in range(N):
        k1 = f(state)
        k2 = f(state + dt/2 * k1)
        k3 = f(state + dt/2 * k2)
        k4 = f(state + dt   * k3)
        state += dt/6 * (k1 + 2*k2 + 2*k3 + k4)
        xs[i+1] = state[0]
        vs[i+1] = state[1]

    return t, xs, vs

# Parameters
m, k = 1.0, 2.0
b_critical = 2 * np.sqrt(m * k)   # ≈ 2.828

# Solve all three cases
cases = {
    'Underdamped ($b=0.5$)':  0.5,
    'Critical ($b=b_c$)':     b_critical,
    'Overdamped ($b=6.0$)':   6.0
}
colors = ['#5ba3d9', '#e8a030', '#a060e0']

fig, axes = plt.subplots(1, 2, figsize=(12, 5))
fig.patch.set_facecolor('#0d0d14')
for ax in axes:
    ax.set_facecolor('#13131f')
    ax.tick_params(colors='#777')
    for sp in ax.spines.values(): sp.set_edgecolor('#2a2a3e')

for (label, b), color in zip(cases.items(), colors):
    t, x, v = rk4_damped(m, b, k, x0=1.0, v0=0.0)

    # x(t) plot
    axes[0].plot(t, x, color=color, lw=1.8, label=label)

    # Phase portrait
    axes[1].plot(x, v, color=color, lw=1.5, label=label)

axes[0].set_xlabel('t (s)', color='#777'); axes[0].set_ylabel('x(t)', color='#777')
axes[0].set_title('Displacement vs Time', color='#ccc', fontsize=12)
axes[0].legend(fontsize=9, facecolor='#1a1a2a', labelcolor='#ccc')
axes[0].axhline(0, color='#333', lw=0.8)

axes[1].set_xlabel('x', color='#777'); axes[1].set_ylabel('ẋ  (velocity)', color='#777')
axes[1].set_title('Phase Portrait', color='#ccc', fontsize=12)
axes[1].legend(fontsize=9, facecolor='#1a1a2a', labelcolor='#ccc')
axes[1].axhline(0, color='#333', lw=0.8); axes[1].axvline(0, color='#333', lw=0.8)

plt.tight_layout()
plt.savefig('damped_oscillator.png', dpi=150, bbox_inches='tight',
            facecolor=fig.get_facecolor())
plt.show()
```

---

## Part 4 — Effect of Parameter $b$

| Range of $b$ | Behavior |
|--------------|----------|
| $b \to 0$ | Ideal oscillator — oscillates at $\omega_0$ forever, no decay |
| $0 < b \ll b_c$ | Many oscillations, slow exponential envelope decay |
| $b \to b_c^-$ | Very few oscillations before dying out |
| $b = b_c = 2\sqrt{mk}$ | Critical: fastest return to equilibrium, no oscillations |
| $b > b_c$ | Overdamped: exponential return, slower as $b$ increases |
| $b \to \infty$ | System barely moves — paralyzed by friction |

The **energy** of the system decays as:

$$E(t) \approx E_0\, e^{-(b/m)\,t}$$

So the energy **half-life** is $t_{1/2} = \frac{m\ln 2}{b}$ — doubling $b$
halves the half-life.

---

## Part 5 — Graph of $x(t)$

The three cases look fundamentally different:

- **Underdamped:** sinusoidal oscillation shrinking inside an exponential
  envelope. Crosses $x = 0$ repeatedly.
- **Critically damped:** smooth monotone curve from $x_0$ back to zero.
  Fastest possible decay without crossing.
- **Overdamped:** smooth monotone curve, but slower than critical — may
  appear to "creep" back toward zero.

---

## Part 6 — Phase Portrait

The phase portrait plots $\dot{x}$ (velocity) on the $y$-axis versus
$x$ (position) on the $x$-axis. Every point represents a complete
instantaneous state of the system.

| Case | Shape in phase space |
|------|----------------------|
| **Underdamped** | Inward **spiral** — each orbit is one oscillation cycle, gradually shrinking toward the origin |
| **Critical** | A curve that curves directly into the origin without looping |
| **Overdamped** | A broad slow curve that approaches the origin from one side only |

All trajectories approach the **fixed point** $(0, 0)$ — the equilibrium.
The spiral is the visual signature of oscillation: the loops confirm that
the system crosses zero multiple times before coming to rest.

---

##  Common Mistakes

- ❌ **Confusing $\omega_0$ and $\omega_d$** — $\omega_0 = \sqrt{k/m}$ is
  the natural frequency with no damping. $\omega_d = \sqrt{\omega_0^2 - \gamma^2}$
  is the actual oscillation frequency in the underdamped case. They are
  only equal when $b = 0$.
- ❌ **Missing the $te^{-\gamma t}$ term in the critical case** — a repeated
  root always requires this extra term. Without it the solution has only
  one independent function and cannot satisfy both initial conditions.
- ❌ **Assuming overdamped returns faster than critical** — it does not.
  Critical damping is the fastest non-oscillatory return. Overdamped is
  actually slower despite having more friction.
