# 8. Lorentz Force

### Problem Statement

A charged particle with charge $q = 2 \times 10^{-19}\text{ C}$ and mass $m = 4 \times 10^{-27}\text{ kg}$ enters a magnetic field of $B = 0.5\text{ T}$ at a speed of $v = 10^6\text{ m/s}$ perpendicular to the field. 

What is the magnitude of the Lorentz force acting on the particle?

---

### Solution

#### 1. Identify the Given Information

* **Charge ($q$):** $2 \times 10^{-19}\text{ C}$
* **Mass ($m$):** $4 \times 10^{-27}\text{ kg}$
* **Magnetic Field ($B$):** $0.5\text{ T}$
* **Velocity ($v$):** $10^6\text{ m/s}$
* **Angle ($\theta$):** $90^\circ$ (since the velocity is perpendicular to the field)

---

#### 2. The Lorentz Force Formula

The full Lorentz force equation describes the force on a charge moving through both an electric field ($\vec{E}$) and a magnetic field ($\vec{B}$):

$$\vec{F} = q(\vec{E} + \vec{v} \times \vec{B})$$

In this specific problem, there is no mention of an electric field ($E = 0$), so the force is purely magnetic. The magnitude of this magnetic force is given by:

$$F = qvB \sin(\theta)$$



---

#### 3. Why the Angle Matters

Because the particle enters **perpendicularly**:
* $\theta = 90^\circ$
* $\sin(90^\circ) = 1$

This simplifies our formula to its maximum possible value:
$$F = qvB$$

---

#### 4. Final Calculation

**Step A: Substitute the known values**
$$F = (2 \times 10^{-19}\text{ C}) \cdot (10^6\text{ m/s}) \cdot (0.5\text{ T})$$

**Step B: Multiply the terms**
$$F = (2 \cdot 0.5) \cdot (10^{-19} \cdot 10^6)$$
$$F = 1.0 \cdot 10^{-13}$$

---

### Final Result

The magnitude of the Lorentz force acting on the particle is:

**$$F = 1 \times 10^{-13}\text{ N}$$**

> **Note:** Even though the mass was provided, it is not required to calculate the **force** itself. The mass would only be necessary if you were asked to find the **acceleration** ($a = F/m$) or the **radius** of the particle's path.
