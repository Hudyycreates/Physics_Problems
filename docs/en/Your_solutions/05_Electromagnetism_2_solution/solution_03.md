# 3. Biot-Savart Law

### Problem Statement

A small segment of a line wire of length $dL = 0.1\text{ m}$ carries a current of $3\text{ A}$. The segment is located at a distance of $r = 0.2\text{ m}$ from a point $P$. 

Calculate the magnetic field at point $P$ due to this current segment (assume the segment is perpendicular to the line connecting it to point $P$).

---

### Solution

#### 1. Identify the Given Information

* **Current ($I$):** $3\text{ A}$
* **Segment length ($dL$):** $0.1\text{ m}$
* **Distance ($r$):** $0.2\text{ m}$
* **Angle ($\theta$):** $90^\circ$ (perpendicular)
* **Constant ($\frac{\mu_0}{4\pi}$):** $10^{-7}\text{ T}\cdot\text{m/A}$

---

#### 2. The Biot-Savart Formula

The magnetic field ($dB$) produced by a small current element is given by:

$$dB = \frac{\mu_0}{4\pi} \frac{I \cdot dL \sin(\theta)}{r^2}$$



---

#### 3. Final Calculation

**Step A: Substitute the known values**
$$dB = (10^{-7}) \frac{3 \cdot 0.1 \cdot \sin(90^\circ)}{(0.2)^2}$$

**Step B: Simplify the terms**
* $\sin(90^\circ) = 1$
* $I \cdot dL = 3 \cdot 0.1 = 0.3$
* $r^2 = (0.2)^2 = 0.04$

**Step C: Solve**
$$dB = 10^{-7} \cdot \frac{0.3}{0.04}$$
$$dB = 10^{-7} \cdot 7.5$$
$$dB = 7.5 \times 10^{-7}\text{ T}$$

---

### Final Result

The magnetic field at point $P$ is:

**$$B = 7.5 \times 10^{-7}\text{ T}$$**
**(or $0.75\text{ }\mu\text{T}$)**
