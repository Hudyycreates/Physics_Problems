# 7. Cyclotron Motion

### Problem Statement

An electron is accelerated from rest through a potential difference of $5000\text{ V}$. It then enters a region of uniform magnetic field $B = 0.1\text{ T}$, perpendicular to its velocity. 

What is the radius of the circular path it will follow?

---

### Solution

#### 1. Identify the Given Information

* **Potential Difference ($V$):** $5000\text{ V}$
* **Magnetic Field ($B$):** $0.1\text{ T}$
* **Electron Charge ($e$):** $\approx 1.602 \times 10^{-19}\text{ C}$
* **Electron Mass ($m$):** $\approx 9.11 \times 10^{-31}\text{ kg}$

---

#### 2. Phase 1: Acceleration (Conservation of Energy)

When the electron is accelerated through a potential difference, its electrical potential energy is converted into kinetic energy.

$$qV = \frac{1}{2}mv^2$$

Rearranging to find the velocity ($v$):

$$v = \sqrt{\frac{2eV}{m}}$$

**Calculation:**
$$v = \sqrt{\frac{2 \cdot (1.602 \times 10^{-19}\text{ C}) \cdot (5000\text{ V})}{9.11 \times 10^{-31}\text{ kg}}}$$
$$v \approx \sqrt{1.758 \times 10^{15}}$$
$$v \approx 4.19 \times 10^7\text{ m/s}$$

---

#### 3. Phase 2: Circular Motion (Magnetic Force)

When the electron enters the magnetic field perpendicularly, the magnetic force ($F_B$) provides the centripetal force ($F_c$) required for circular motion.



1.  **Magnetic Force:** $F_B = evB$
2.  **Centripetal Force:** $F_c = \frac{mv^2}{r}$

Setting them equal for equilibrium in the curve:
$$evB = \frac{mv^2}{r}$$

---

#### 4. Solve for Radius ($r$)

Isolating $r$:
$$r = \frac{mv}{eB}$$

Alternatively, we can substitute the expression for $v$ from Phase 1 to get a direct formula:
$$r = \frac{1}{B} \sqrt{\frac{2mV}{e}}$$

**Final Calculation:**
$$r = \frac{(9.11 \times 10^{-31}\text{ kg}) \cdot (4.19 \times 10^7\text{ m/s})}{(1.602 \times 10^{-19}\text{ C}) \cdot (0.1\text{ T})}$$

$$r = \frac{3.817 \times 10^{-23}}{1.602 \times 10^{-20}}$$

$$r \approx 0.00238\text{ m}$$

---

### Final Result

The radius of the circular path is:

**$$r \approx 2.38 \times 10^{-3}\text{ m}$$**
**(or $2.38\text{ mm}$)**

> **Note:** At a velocity of approximately $14\%$ the speed of light, relativistic effects would change the mass slightly (by about $1\%$), but for standard textbook physics, the classical calculation provided above is the expected approach.
