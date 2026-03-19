# 🎯 Projectile Motion: Range Optimization

> **Problem:** Show analytically that the range formula $R(\theta) = \dfrac{v_0^2 \sin(2\theta)}{g}$ is maximized at a launch angle of **θ = 45°**.

---

## 📚 Background

When a projectile is launched with initial speed $v_0$ at angle $\theta$ above the horizontal, it follows a parabolic path under constant gravitational acceleration $g$. We want to find the angle that sends it the **farthest horizontal distance**.

---

## 🧱 Step 1 — Derive the Range Formula

Decompose the initial velocity into components:

| Component | Expression |
|-----------|------------|
| Horizontal | $v_x = v_0 \cos\theta$ |
| Vertical   | $v_y = v_0 \sin\theta$ |

**Time of Flight** — the projectile returns to ground when vertical displacement = 0:

$$y(t) = v_0 \sin\theta \cdot t - \frac{1}{2}gt^2 = 0$$

$$t\left(v_0 \sin\theta - \frac{1}{2}gt\right) = 0 \implies T = \frac{2v_0 \sin\theta}{g}$$

**Horizontal Range** — distance = horizontal speed × time:

$$R = v_0 \cos\theta \cdot T = v_0 \cos\theta \cdot \frac{2v_0 \sin\theta}{g} = \frac{2v_0^2 \sin\theta\cos\theta}{g}$$

Applying the **double-angle identity** $2\sin\theta\cos\theta = \sin(2\theta)$:

$$\boxed{R(\theta) = \frac{v_0^2 \sin(2\theta)}{g}}$$

---

## 🔍 Step 2 — Set Up the Optimization

Since $\dfrac{v_0^2}{g}$ is a **positive constant**, maximizing $R(\theta)$ is equivalent to maximizing:

$$\sin(2\theta)$$

The sine function achieves its **maximum value of 1** when its argument equals 90°.

---

## 📐 Step 3 — First Derivative Test

Differentiate $R(\theta)$ with respect to $\theta$:

$$\frac{dR}{d\theta} = \frac{v_0^2}{g} \cdot \frac{d}{d\theta}\left[\sin(2\theta)\right]$$

By the **chain rule**, $\dfrac{d}{d\theta}[\sin(2\theta)] = 2\cos(2\theta)$, so:

$$\frac{dR}{d\theta} = \frac{2v_0^2}{g}\cos(2\theta)$$

Set the derivative equal to zero to find critical points:

$$\frac{2v_0^2}{g}\cos(2\theta) = 0$$

Since $\dfrac{2v_0^2}{g} \neq 0$, we require:

$$\cos(2\theta) = 0$$

---

## ✅ Step 4 — Solve for the Critical Angle

The cosine function equals zero at $90° + n \cdot 180°$ for integer $n$. For the physically meaningful range $\theta \in (0°, 90°)$:

$$2\theta = 90° \implies \boxed{\theta = 45°}$$

---

## 🔬 Step 5 — Confirm Maximum via Second Derivative Test

Take the second derivative:

$$\frac{d^2R}{d\theta^2} = \frac{-4v_0^2}{g}\sin(2\theta)$$

Evaluate at $\theta = 45°$:

$$\frac{d^2R}{d\theta^2}\Bigg|_{\theta = 45°} = \frac{-4v_0^2}{g}\sin(90°) = \frac{-4v_0^2}{g} < 0$$

Since the second derivative is **strictly negative**, the critical point at $\theta = 45°$ is a **maximum**. ✅

---

## 🏁 Result: Maximum Range

Substituting $\theta = 45°$ into the range formula:

$$R_{\max} = \frac{v_0^2 \sin(90°)}{g} = \frac{v_0^2 \cdot 1}{g}$$

$$\boxed{R_{\max} = \frac{v_0^2}{g}}$$

---

## 📊 Summary Table

| Quantity | Expression |
|----------|------------|
| Range formula | $R(\theta) = \dfrac{v_0^2 \sin(2\theta)}{g}$ |
| Optimal angle | $\theta^* = 45°$ |
| Maximum range | $R_{\max} = \dfrac{v_0^2}{g}$ |
| Condition verified by | Second derivative test: $R''(45°) < 0$ |

---

## 💡 Intuition

At **θ = 45°**, the launch splits velocity **equally** between horizontal and vertical components. Launching flatter (θ < 45°) covers more horizontal ground per second but falls too quickly. Launching steeper (θ > 45°) stays airborne longer but wastes speed going straight up. The 45° angle is the perfect balance between **time of flight** and **horizontal speed**.

---

*Derived using single-variable calculus and trigonometric identities.*
