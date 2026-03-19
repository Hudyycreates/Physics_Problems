# Projectile Motion — Step-by-Step Solution

**Given:**
- Initial velocity: $v_0 = 100$ m/s
- Launch angle: $\theta = 37°$
- No air resistance
- $g = 9.8$ m/s²

---

## Step 1 — Decompose the Initial Velocity

The launch velocity points at 37° above the horizontal. We split it into two components:

$$v_x = v_0 \cos\theta = 100 \times \cos(37°) = 100 \times 0.7986 = 79.9 \text{ m/s}$$

$$v_y = v_0 \sin\theta = 100 \times \sin(37°) = 100 \times 0.6018 = 60.2 \text{ m/s}$$

---

## Step 2 — Derive the Differential Equations of Motion

The only force acting after launch is gravity (downward). Apply Newton's second law $F = ma$ in each direction:

**Horizontal** — no force acts horizontally:

$$m\frac{d^2x}{dt^2} = 0 \implies \frac{d^2x}{dt^2} = 0$$

**Vertical** — gravity acts downward:

$$m\frac{d^2y}{dt^2} = -mg \implies \frac{d^2y}{dt^2} = -g$$

**Integrate once** (acceleration → velocity):

$$\frac{dx}{dt} = v_x = v_0\cos\theta = 79.9 \text{ m/s} \quad \text{(constant)}$$

$$\frac{dy}{dt} = v_y = v_0\sin\theta - gt = 60.2 - 9.8t$$

**Integrate again** (velocity → position), using initial conditions $x(0) = 0$, $y(0) = 0$:

$$\boxed{x(t) = v_0\cos\theta \cdot t = 79.9\,t}$$

$$\boxed{y(t) = v_0\sin\theta \cdot t - \frac{1}{2}gt^2 = 60.2\,t - 4.9\,t^2}$$

---

## Step 3 — Time of Flight

The projectile lands when $y(t) = 0$ (returns to ground level):

$$60.2\,t - 4.9\,t^2 = 0$$

Factor out $t$:

$$t\,(60.2 - 4.9\,t) = 0$$

Two solutions:

$$t = 0 \quad \text{(launch)} \qquad \text{or} \qquad t = \frac{60.2}{4.9}$$

Solve the second:

$$t_{\text{flight}} = \frac{60.2}{4.9} = \frac{2 \times 60.2}{9.8} = \frac{2\,v_0\sin\theta}{g}$$

$$t_{\text{flight}} = \frac{120.4}{9.8}$$

$$\boxed{t_{\text{flight}} = 12.28 \text{ s}}$$

---

## Step 4 — Maximum Height

The projectile reaches its highest point when vertical velocity $= 0$:

$$v_y = 0 \implies 60.2 - 9.8\,t = 0 \implies t_{\text{peak}} = \frac{60.2}{9.8} = 6.14 \text{ s}$$

Substitute $t_{\text{peak}}$ into $y(t)$:

$$H = 60.2\,(6.14) - 4.9\,(6.14)^2$$

$$H = 369.6 - 4.9 \times 37.7$$

$$H = 369.6 - 184.7$$

$$\boxed{H_{\max} = 184.8 \text{ m}}$$

---

## Step 5 — Range

Substitute $t_{\text{flight}}$ into $x(t)$:

$$R = 79.9 \times 12.28$$

$$\boxed{R = 981.2 \text{ m}}$$

---

## Final Answers

| Quantity | Formula | Answer |
|---|---|---|
| Time of flight | $\dfrac{2\,v_0\sin\theta}{g}$ | **12.28 s** |
| Maximum height | $\dfrac{(v_0\sin\theta)^2}{2g}$ | **184.8 m** |
| Range | $\dfrac{v_0^2\sin 2\theta}{g}$ | **981.2 m** |
