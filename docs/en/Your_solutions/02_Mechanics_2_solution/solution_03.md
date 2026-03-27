# Problem 3 — Conservation of Energy

## The Setup

When released from angle $\theta$, the bob sits **higher** than the bottom.
Potential energy converts entirely into kinetic energy as it swings down.

**Given:**
| Symbol | Meaning | Value |
|--------|---------|-------|
| $L$ | Pendulum length | $1.0\ \text{m}$ |
| $\theta$ | Release angle | $15°$ |
| $g$ | Gravity | $9.8\ \text{m/s}^2$ |

---

## Step 1 — Find the Height h

$$h = L(1 - \cos\theta) = 1.0 \times (1 - \cos 15°)$$

$$\boxed{h \approx 0.0341\ \text{m}}$$

> The bob only rises about 3.4 cm — small angle means small height!

---

## Step 2 — Apply Conservation of Energy

$$mgh = \frac{1}{2}mv^2$$

Mass $m$ cancels:

$$v = \sqrt{2gh}$$

---

## Step 3 — Solve for v

$$v = \sqrt{2 \times 9.8 \times 0.0341} = \sqrt{0.6684}$$

$$\boxed{v \approx 0.817\ \text{m/s}}$$

> At the bottom of the swing, the bob moves at roughly 0.82 m/s!

---

## Energy Flow Summary

| Position | Height | Potential Energy | Kinetic Energy |
|----------|--------|-----------------|----------------|
| Release point ($\theta = 15°$) | $0.0341\ \text{m}$ | $mgh$ | $0$ |
| Bottom ($\theta = 0°$) | $0$ | $0$ | $\frac{1}{2}mv^2$ |

$$\Delta PE = \Delta KE \quad \checkmark$$
