# Question 10: Kinematics — Elliptic Helix
 
> **Problem:** Point M moves according to $\vec{r}(t) = (a\cos(\omega t),\ b\sin(\omega t),\ bt)$ where $a, b, \omega > 0$.
> - (a) Find the equation of the trajectory.
> - (b) Compute the path length from $t = 0$ to $t = t_0$.
> - (c) Discuss special cases.
 
---
 
## Background
 
A **parametric curve in 3D** describes a point whose $x$, $y$, $z$ coordinates are each functions of time. Eliminating the parameter $t$ reveals the geometric shape of the path — independent of how fast the point moves along it.
 
---
 
## Part (a) — Equation of the Trajectory
 
The three coordinate functions are:
 
$$x(t) = a\cos(\omega t), \qquad y(t) = b\sin(\omega t), \qquad z(t) = bt$$
 
### Step 1 — Eliminate $t$ from $x$ and $y$
 
$$\frac{x}{a} = \cos(\omega t), \qquad \frac{y}{b} = \sin(\omega t)$$
 
Apply the Pythagorean identity $\cos^2(\omega t) + \sin^2(\omega t) = 1$:
 
$$\boxed{\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1}$$
 
This is the equation of an **elliptic cylinder** with semi-axes $a$ (along $x$) and $b$ (along $y$).
 
### Step 2 — Interpret the $z$ component
 
$$z = bt \implies t = \frac{z}{b}$$
 
The point ascends the cylinder linearly as $t$ increases.
 
### Conclusion
 
The trajectory is an **elliptic helix**: the point winds continuously around the elliptic cylinder $\dfrac{x^2}{a^2} + \dfrac{y^2}{b^2} = 1$ while rising at a constant rate in the $z$-direction.
 
One full revolution in the $xy$-plane requires time $T = \dfrac{2\pi}{\omega}$, during which the point rises by $\Delta z = b \cdot T = \dfrac{2\pi b}{\omega}$ — this is the **pitch** of the helix.
 
---
 
## Part (b) — Path Length from $t = 0$ to $t = t_0$
 
### Step 1 — Compute the velocity vector
 
$$\vec{v}(t) = \frac{d\vec{r}}{dt} = \big(-a\omega\sin(\omega t),\ b\omega\cos(\omega t),\ b\big)$$
 
### Step 2 — Compute the speed $|\vec{v}(t)|$
 
$$|\vec{v}(t)|^2 = a^2\omega^2\sin^2(\omega t) + b^2\omega^2\cos^2(\omega t) + b^2$$
 
Rewrite by separating the $b^2\omega^2$ term:
 
$$= b^2\omega^2\cos^2(\omega t) + a^2\omega^2\sin^2(\omega t) + b^2$$
 
$$= b^2\omega^2 + \omega^2(a^2 - b^2)\sin^2(\omega t) + b^2$$
 
$$|\vec{v}(t)| = \sqrt{b^2(1 + \omega^2) + \omega^2(a^2 - b^2)\sin^2(\omega t)}$$
 
### Step 3 — Integrate to find path length
 
$$\boxed{s = \int_0^{t_0} \sqrt{b^2(1+\omega^2) + \omega^2(a^2-b^2)\sin^2(\omega t)}\; dt}$$
 
For $a \neq b$, this integral does not have a closed form in elementary functions — it is an **elliptic integral of the second kind**. Substituting $u = \omega t$:
 
$$s = \frac{b\sqrt{1+\omega^2}}{\omega} \int_0^{\omega t_0} \sqrt{1 + k^2\sin^2(u)}\; du, \qquad k^2 = \frac{\omega^2(a^2-b^2)}{b^2(1+\omega^2)}$$
 
This equals $\dfrac{b\sqrt{1+\omega^2}}{\omega}\, E\!\left(-k^2,\, \omega t_0\right)$ in standard elliptic integral notation, and must be evaluated numerically for general $a$, $b$, $\omega$.
 
### Special case: $a = b$
 
When the semi-axes are equal the term $(a^2-b^2)$ vanishes:
 
$$|\vec{v}(t)| = \sqrt{b^2(1+\omega^2)} = b\sqrt{1+\omega^2} \quad \text{(constant)}$$
 
The speed is constant, so the path length closes to:
 
$$\boxed{s = b\sqrt{1+\omega^2}\cdot t_0}$$
 
---
 
## Part (c) — Velocity, Acceleration, and Special Cases
 
### Velocity vector
 
$$\vec{v}(t) = -a\omega\sin(\omega t)\;\hat{i} + b\omega\cos(\omega t)\;\hat{j} + b\;\hat{k}$$
 
$$|\vec{v}(t)| = \sqrt{a^2\omega^2\sin^2(\omega t) + b^2\omega^2\cos^2(\omega t) + b^2}$$
 
### Acceleration vector
 
$$\vec{a}(t) = \frac{d\vec{v}}{dt} = -a\omega^2\cos(\omega t)\;\hat{i} - b\omega^2\sin(\omega t)\;\hat{j} + 0\;\hat{k}$$
 
$$|\vec{a}(t)| = \omega^2\sqrt{a^2\cos^2(\omega t) + b^2\sin^2(\omega t)}$$
 
The acceleration lies entirely in the horizontal ($xy$) plane and points inward toward the axis of the cylinder — it is a generalized centripetal acceleration. There is no vertical acceleration component; the point rises at a constant speed $b$ in the $z$-direction.
 
### Special cases
 
| Condition | Geometry | Path length |
|-----------|----------|-------------|
| $a = b$ | **Circular helix** on cylinder $x^2+y^2=a^2$ | $s = a\sqrt{1+\omega^2}\cdot t_0$ |
| $a \neq b$ | **Elliptic helix** on elliptic cylinder $\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$ | Elliptic integral |
| $a = b$, $b \to 0$ | Circular motion in $xy$-plane ($z=0$) | $s = a\omega t_0$ (circumference only) |
| $\omega \to 0$ | Straight line along $z$-axis | $s = bt_0$ |
 
**Special case $a = b$ — acceleration magnitude:**
 
$$|\vec{a}(t)| = a\omega^2 = \text{const}$$
 
This is the classical centripetal acceleration of uniform circular motion, now constant in magnitude. For $a \neq b$ the magnitude oscillates between $b\omega^2$ (minimum, at the narrow end of the ellipse) and $a\omega^2$ (maximum, at the wide end).
 
---
 
## Summary of Results
 
| Quantity | Expression |
|----------|-----------|
| Trajectory | Elliptic helix on cylinder $\dfrac{x^2}{a^2} + \dfrac{y^2}{b^2} = 1$ |
| Velocity | $\vec{v}(t) = (-a\omega\sin\omega t,\ b\omega\cos\omega t,\ b)$ |
| Acceleration | $\vec{a}(t) = (-a\omega^2\cos\omega t,\ -b\omega^2\sin\omega t,\ 0)$ |
| $\|\vec{a}\|$ when $a=b$ | $a\omega^2$ (constant) |
| Path length when $a=b$ | $b\sqrt{1+\omega^2}\cdot t_0$ |
| Path length when $a \neq b$ | Elliptic integral $E\!\left(-k^2, \omega t_0\right)$ |
| Pitch per revolution | $\dfrac{2\pi b}{\omega}$ |
 
---
 
## Python Code
 
```python
import numpy as np
import matplotlib.pyplot as plt
 
def elliptic_helix(a, b, omega, t0, N=1000):
    t = np.linspace(0, t0, N)
    x = a * np.cos(omega * t)
    y = b * np.sin(omega * t)
    z = b * t
    return x, y, z, t
 
def path_length_numeric(a, b, omega, t0, N=10000):
    t = np.linspace(0, t0, N)
    vx = -a * omega * np.sin(omega * t)
    vy =  b * omega * np.cos(omega * t)
    vz =  b * np.ones_like(t)
    speed = np.sqrt(vx**2 + vy**2 + vz**2)
    return np.trapz(speed, t)
 
fig = plt.figure(figsize=(12, 5))
 
params = [
    dict(a=2, b=1, omega=1.5, t0=12, label='Elliptic helix (a=2, b=1)'),
    dict(a=1, b=1, omega=1.5, t0=12, label='Circular helix (a=b=1)'),
]
 
for i, p in enumerate(params):
    ax = fig.add_subplot(1, 2, i+1, projection='3d')
    x, y, z, t = elliptic_helix(**{k:v for k,v in p.items() if k!='label'})
    ax.plot(x, y, z, lw=1.5, color='#534AB7')
    ax.set_title(p['label'], fontsize=11)
    ax.set_xlabel('x'); ax.set_ylabel('y'); ax.set_zlabel('z')
    length = path_length_numeric(**{k:v for k,v in p.items() if k!='label'})
    if abs(p['a'] - p['b']) < 0.01:
        closed = p['b'] * np.sqrt(1 + p['omega']**2) * p['t0']
        ax.set_title(f"{p['label']}\ns = {length:.3f} (closed: {closed:.3f})", fontsize=10)
    else:
        ax.set_title(f"{p['label']}\ns = {length:.3f} (numeric)", fontsize=10)
 
plt.tight_layout()
plt.savefig('elliptic_helix.png', dpi=150)
plt.show()
```
 
---
 
*Solved using parametric differentiation, the Pythagorean trigonometric identity, and arc-length integration.*
