# Harmonic Motion — Full Step-by-Step Solution

**Given:**
- Mass: $m = 10$ kg
- Position equation: $x(t) = 0.2\cos(10\pi t)$ meters

**Find:**
- Spring constant $k$
- Total mechanical energy $E$

---

## Step 1 — Identify the Components of x(t)

The position equation is given as:

$$x(t) = 0.2\cos(10\pi t)$$

We identify two parts:

| Symbol | Name | Value | Meaning |
|--------|------|-------|---------|
| $A$ | Amplitude | $0.2$ m | Maximum displacement from centre |
| $\omega$ | Angular frequency | $10\pi$ rad/s | How fast it oscillates |

---

## Step 2 — Differentiate x(t) Once to Get Velocity

Using the chain rule — the derivative of $\cos(\text{something})$ is $-\sin(\text{something})$ multiplied by the derivative of what is inside:

$$v(t) = \frac{dx}{dt} = \frac{d}{dt}\Big[0.2\cos(10\pi t)\Big]$$

**Step 2a** — $\cos$ becomes $-\sin$:

$$= -0.2\sin(10\pi t)$$

**Step 2b** — multiply by the derivative of the inside $(10\pi t)$:

$$\frac{d}{dt}(10\pi t) = 10\pi$$

**Step 2c** — combine:

$$\boxed{v(t) = -0.2 \times 10\pi \times \sin(10\pi t) = -2\pi\sin(10\pi t)}$$

---

## Step 3 — Differentiate v(t) Again to Get Acceleration

Now differentiate $v(t) = -2\pi\sin(10\pi t)$

Using the chain rule — the derivative of $\sin(\text{something})$ is $\cos(\text{something})$:

**Step 3a** — $-\sin$ becomes $-\cos$:

$$= -2\pi\cos(10\pi t)$$

**Step 3b** — multiply by the derivative of the inside $(10\pi t)$:

$$\frac{d}{dt}(10\pi t) = 10\pi$$

**Step 3c** — combine:

$$\boxed{a(t) = -2\pi \times 10\pi \times \cos(10\pi t) = -20\pi^2\cos(10\pi t)}$$

> **Why the minus sign?** The minus means acceleration always points **opposite** to displacement. When the spring is stretched right, it pulls back left. This is the defining property of a spring.

---

## Step 4 — Apply Newton's Second Law to Find k

For a spring, the restoring force is:

$$F = -kx$$

Newton's second law says $F = ma$, so:

$$ma = -kx$$

Substitute $a(t)$ and $x(t)$:

$$m \times \Big(-20\pi^2\cos(10\pi t)\Big) = -k \times \Big(0.2\cos(10\pi t)\Big)$$

**The $\cos(10\pi t)$ cancels on both sides:**

$$m \times 20\pi^2 = k \times 0.2$$

**Solve for k:**

$$k = \frac{m \times 20\pi^2}{0.2} = \frac{10 \times 20\pi^2}{0.2}$$

$$k = \frac{200\pi^2}{0.2} = 1000\pi^2$$

$$\boxed{k = 1000\pi^2 \approx 9869.6 \text{ N/m}}$$

---

## Step 5 — Calculate Total Mechanical Energy

The total mechanical energy of a spring system is stored entirely in the amplitude:

$$E = \frac{1}{2}kA^2$$

Where:
- $k = 1000\pi^2 \approx 9869.6$ N/m
- $A = 0.2$ m (the number in front of $\cos$ in $x(t)$)

Substituting:

$$E = \frac{1}{2} \times 1000\pi^2 \times (0.2)^2$$

$$E = \frac{1}{2} \times 1000\pi^2 \times 0.04$$

$$E = \frac{1}{2} \times 40\pi^2$$

$$\boxed{E = 20\pi^2 \approx 197.4 \text{ J}}$$

---

## Full Calculus Chain — Summary

$$x(t) = 0.2\cos(10\pi t)$$

$$\downarrow \frac{d}{dt}$$

$$v(t) = -2\pi\sin(10\pi t)$$

$$\downarrow \frac{d}{dt}$$

$$a(t) = -20\pi^2\cos(10\pi t)$$

$$\downarrow \quad ma = -kx$$

$$10 \times (-20\pi^2\cos(10\pi t)) = -k \times (0.2\cos(10\pi t))$$

$$\downarrow \quad \cos(10\pi t) \text{ cancels}$$

$$k = 1000\pi^2 \approx 9869.6 \text{ N/m}$$

$$\downarrow \quad E = \frac{1}{2}kA^2$$

$$E = 20\pi^2 \approx 197.4 \text{ J}$$

---

## Final Answers

| Quantity | Formula | Answer |
|----------|---------|--------|
| Spring constant | $k = \dfrac{m \times \omega^2 \times A}{A} = m\omega^2$ | $k = 1000\pi^2 \approx 9869.6$ N/m |
| Total mechanical energy | $E = \dfrac{1}{2}kA^2$ | $E = 20\pi^2 \approx 197.4$ J |

---

## Key Physical Principles

1. **Position → velocity → acceleration** by differentiating twice using the chain rule
2. **Newton's second law** $F = ma$ combined with the spring force $F = -kx$ gives $ma = -kx$
3. The $\cos(10\pi t)$ term cancels — because both sides have it — leaving a clean equation for $k$
4. **Total energy** lives entirely in the amplitude $A$ at the moment of maximum stretch where all energy is potential

---

*Note: $\omega = 10\pi$ rad/s is the angular frequency read directly from $x(t)$. An equivalent shortcut is $k = m\omega^2 = 10 \times (10\pi)^2 = 1000\pi^2$ N/m*
