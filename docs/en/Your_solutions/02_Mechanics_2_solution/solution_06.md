# Problem 6 — Energy Dissipation

## Conceptual Intro

Each bounce retains 70% of mechanical energy. Since $E \propto h$, height
follows the same geometric decay:

$$h_n = h_0 \cdot \alpha^n$$

> ⚠️ Don't subtract 30% of the *original* height each time — subtract 30%
> of the *current* height. The base changes after every bounce.

---

## Given

| Symbol | Meaning | Value |
|--------|---------|-------|
| $h_0$ | Initial height | $2.0\ \text{m}$ |
| $\alpha$ | Energy retained | $0.70$ |
| $n$ | Bounces | $2$ |

---

## Solution

$$h_1 = 2.0 \times 0.70 = 1.4\ \text{m}$$

$$h_2 = 2.0 \times (0.70)^2 = 2.0 \times 0.49$$

$$\boxed{h_2 = 0.98\ \text{m}}$$

---

## Energy Table

| Bounce | Height | Energy Retained |
|--------|--------|-----------------|
| Drop | $2.00\ \text{m}$ | $100\%$ |
| 1st | $1.40\ \text{m}$ | $70\%$ |
| 2nd | $0.98\ \text{m}$ | $49\%$ |

> After two bounces, **51% of mechanical energy** is lost to heat and sound.
