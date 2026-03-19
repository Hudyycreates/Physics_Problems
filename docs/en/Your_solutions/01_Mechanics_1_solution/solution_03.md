# 🗺️ Path Intersection: Alice & Bob

> **Problem:** Alice moves along $A(t) = (2+t,\ 8-3t)$ and Bob moves along $B(t) = (2t-1,\ 2t+2)$.  
> Determine if their paths intersect. If yes, find when and where they collide. If no, find the minimum distance and when it occurs.

---

## 📌 The Setup

| Person | Position at time $t$ | x-component | y-component |
|--------|----------------------|-------------|-------------|
| Alice  | $A(t) = (2+t,\ 8-3t)$ | $2+t$ | $8-3t$ |
| Bob    | $B(t) = (2t-1,\ 2t+2)$ | $2t-1$ | $2t+2$ |

> ⚠️ **Key distinction:**  
> - **Path intersection** — do the *curves* share a common point? (can be at different times)  
> - **Collision** — are they at the *same point at the same time*?

---

## Part 1 — Do the Paths Cross?

To test if the curves share a point, use **different parameters** $t$ and $s$ (Alice and Bob can pass through the same location at different moments):

$$A(t) = B(s)$$

### Setting Up the System

**x-equation:**
$$2 + t = 2s - 1 \implies t - 2s = -3 \tag{i}$$

**y-equation:**
$$8 - 3t = 2s + 2 \implies 3t + 2s = 6 \tag{ii}$$

### Solving the System

Add equations (i) and (ii):

$$(t - 2s) + (3t + 2s) = -3 + 6$$

$$4t = 3 \implies \boxed{t = \frac{3}{4}}$$

Substitute back into equation (i):

$$\frac{3}{4} - 2s = -3 \implies 2s = \frac{15}{4} \implies \boxed{s = \frac{15}{8}}$$

### Finding the Intersection Point

$$A\!\left(\frac{3}{4}\right) = \left(2 + \frac{3}{4},\ 8 - \frac{9}{4}\right) = \left(\frac{11}{4},\ \frac{23}{4}\right)$$

$$B\!\left(\frac{15}{8}\right) = \left(2\cdot\frac{15}{8} - 1,\ 2\cdot\frac{15}{8} + 2\right) = \left(\frac{11}{4},\ \frac{23}{4}\right) \checkmark$$

### ✅ Conclusion: Paths DO Intersect

The paths cross at $\left(\dfrac{11}{4},\ \dfrac{23}{4}\right) = (2.75,\ 5.75)$.

However:
- Alice passes through this point at $t = \dfrac{3}{4}$
- Bob passes through this point at $t = \dfrac{15}{8}$

Since $\dfrac{3}{4} \neq \dfrac{15}{8}$, **they are never at the same place at the same time — no collision occurs.**

---

## Part 2 — Minimum Distance Between Them

Since they never collide, we find the **closest they come** to each other at the same time $t$.

### Step 1 — Displacement Vector

$$\vec{d}(t) = A(t) - B(t) = \big((2+t)-(2t-1),\ (8-3t)-(2t+2)\big) = (3-t,\ 6-5t)$$

### Step 2 — Squared Distance Function

To avoid dealing with square roots, minimize $D^2(t)$ instead:

$$D^2(t) = (3-t)^2 + (6-5t)^2$$

Expanding:

$$D^2(t) = (9 - 6t + t^2) + (36 - 60t + 25t^2)$$

$$\boxed{D^2(t) = 26t^2 - 66t + 45}$$

### Step 3 — Minimize via Differentiation

$$\frac{d(D^2)}{dt} = 52t - 66$$

Set equal to zero:

$$52t - 66 = 0 \implies \boxed{t^* = \frac{33}{26} \approx 1.269}$$

**Confirm it's a minimum** (second derivative test):

$$\frac{d^2(D^2)}{dt^2} = 52 > 0 \implies \text{minimum confirmed} \checkmark$$

### Step 4 — Compute the Minimum Distance

Substitute $t^* = \dfrac{33}{26}$ into $D^2(t)$:

$$D^2\!\left(\frac{33}{26}\right) = 26\cdot\frac{33^2}{26^2} - 66\cdot\frac{33}{26} + 45 = \frac{1089}{26} - \frac{2178}{26} + \frac{1170}{26} = \frac{81}{26}$$

$$\boxed{D_{\min} = \sqrt{\frac{81}{26}} = \frac{9}{\sqrt{26}} = \frac{9\sqrt{26}}{26} \approx 1.765 \text{ units}}$$

### Step 5 — Positions at Closest Approach

At $t^* = \dfrac{33}{26}$:

$$A\!\left(\frac{33}{26}\right) = \left(\frac{85}{26},\ \frac{109}{26}\right) \approx (3.27,\ 4.19)$$

$$B\!\left(\frac{33}{26}\right) = \left(\frac{40}{26},\ \frac{118}{26}\right) \approx (1.54,\ 4.54)$$

---

## 📊 Summary of Results

| Question | Answer |
|----------|--------|
| Do paths cross? | ✅ Yes, at $\left(\frac{11}{4},\ \frac{23}{4}\right) = (2.75,\ 5.75)$ |
| Does a collision occur? | ❌ No — Alice arrives at $t = \frac{3}{4}$, Bob at $t = \frac{15}{8}$ |
| Time of closest approach | $t^* = \frac{33}{26} \approx 1.269$ |
| Alice's position then | $\left(\frac{85}{26},\ \frac{109}{26}\right) \approx (3.27,\ 4.19)$ |
| Bob's position then | $\left(\frac{40}{26},\ \frac{118}{26}\right) \approx (1.54,\ 4.54)$ |
| Minimum distance | $\frac{9\sqrt{26}}{26} \approx 1.765$ units |

---

## 💡 Intuition

Think of Alice and Bob as two cars on different roads. Their roads **do cross** at a junction — but they arrive at the junction at different times, so they never crash. The minimum distance question asks: at what moment are the two cars **closest together** (even on their separate roads)?

The answer comes from minimizing the distance function $D(t)$, which is a parabola in $t^2$ — its minimum gives the moment of closest approach.

---

*Solved using parametric equations, simultaneous linear systems, and single-variable calculus optimization.*
