# Question 8: Circular Motion

> **Problem:** Calculate the centripetal acceleration of a person standing on the Earth's equator. The Earth's radius is approximately $R = 6378\ \text{km}$.

---

## Background

Any object moving in a circle must be continuously accelerating toward the center of that circle — even if its speed does not change. This is called **centripetal acceleration**. Without it, the object would fly off in a straight line.

A person standing on the Earth's equator travels in a full circle once every 24 hours as the Earth rotates. Even though they feel stationary, they are in circular motion and therefore experience centripetal acceleration directed toward the Earth's center.

The key formulas are:

$$a_c = \frac{v^2}{R} = \omega^2 R$$

where:
- $v$ is the linear (tangential) speed of the person
- $\omega$ is the Earth's angular velocity
- $R$ is the radius of the circular path (Earth's radius at the equator)

---

## Given Information

| Quantity | Symbol | Value |
|----------|--------|-------|
| Earth's radius | $R$ | $6378\ \text{km} = 6{,}378{,}000\ \text{m}$ |
| Period of rotation | $T$ | $24\ \text{hours} = 86{,}400\ \text{s}$ |

---

## Step 1 — Find the Angular Velocity $\omega$

The Earth completes one full rotation ($2\pi$ radians) in one day:

$$\omega = \frac{2\pi}{T} = \frac{2\pi}{86{,}400\ \text{s}}$$

$$\boxed{\omega = 7.272 \times 10^{-5}\ \text{rad/s}}$$

---

## Step 2 — Find the Linear Speed $v$

The person at the equator travels the full circumference of the Earth in one day:

$$v = \omega R = 7.272 \times 10^{-5} \times 6{,}378{,}000$$

$$\boxed{v \approx 464.0\ \text{m/s} \approx 1670\ \text{km/h}}$$

This is roughly the cruising speed of a commercial aircraft, even though the person feels completely stationary.

---

## Step 3 — Calculate the Centripetal Acceleration

Using both forms of the formula as a cross-check:

**Method 1 — using $\omega^2 R$:**

$$a_c = \omega^2 R = \left(7.272 \times 10^{-5}\right)^2 \times 6{,}378{,}000$$

$$a_c = 5.288 \times 10^{-9} \times 6{,}378{,}000$$

$$\boxed{a_c \approx 0.03374\ \text{m/s}^2}$$

**Method 2 — using $v^2 / R$:**

$$a_c = \frac{v^2}{R} = \frac{(464.0)^2}{6{,}378{,}000} = \frac{215{,}296}{6{,}378{,}000}$$

$$\boxed{a_c \approx 0.03375\ \text{m/s}^2} \checkmark$$

Both methods agree. The centripetal acceleration at the equator is:

$$\boxed{a_c \approx 0.0337\ \text{m/s}^2}$$

---

## Step 4 — Compare with Gravitational Acceleration

It is useful to express $a_c$ as a fraction of $g = 9.81\ \text{m/s}^2$:

$$\frac{a_c}{g} = \frac{0.0337}{9.81} \approx 0.00344 \approx 0.34\%$$

This means the centripetal acceleration at the equator is only about **$\frac{1}{291}$** of the gravitational acceleration — small, but measurable.

---

## Physical Interpretation

The centripetal acceleration is directed **inward toward the Earth's center**. Gravity provides this centripetal force. As a consequence, the effective gravitational pull felt by someone at the equator is slightly reduced compared to someone at the poles:

$$g_{\text{effective}} = g - a_c = 9.81 - 0.0337 \approx 9.776\ \text{m/s}^2$$

This is one reason why the measured value of $g$ is slightly smaller at the equator (~$9.78\ \text{m/s}^2$) than at the poles (~$9.83\ \text{m/s}^2$). The other contributing factor is the equatorial bulge of the Earth, which places the equatorial surface farther from the Earth's center.

---

## Summary of Results

| Quantity | Value |
|----------|-------|
| Angular velocity $\omega$ | $7.272 \times 10^{-5}\ \text{rad/s}$ |
| Linear speed $v$ | $\approx 464.0\ \text{m/s}\ (1670\ \text{km/h})$ |
| Centripetal acceleration $a_c$ | $\approx 0.0337\ \text{m/s}^2$ |
| As a fraction of $g$ | $\approx 0.34\%$ of $g$ |
| Direction | Toward Earth's center (inward) |

---

*Solved using the definitions of angular velocity and centripetal acceleration for uniform circular motion.*
