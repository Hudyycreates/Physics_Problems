# 9. Vector Lorentz Force

### Problem Statement

A proton moves with a velocity $\vec{v} = (2\hat{i} - 4\hat{j} + \hat{k})\text{ m/s}$ in a region where the magnetic field is $\vec{B} = (\hat{i} + 2\hat{j} - \hat{k})\text{ T}$. 

What is the magnitude of the magnetic force this charge experiences?

---

### Solution

#### 1. Identify the Given Information

* **Charge of a proton ($q$):** $\approx 1.6 \times 10^{-19}\text{ C}$
* **Velocity vector ($\vec{v}$):** $(2, -4, 1)\text{ m/s}$
* **Magnetic field vector ($\vec{B}$):** $(1, 2, -1)\text{ T}$

---

#### 2. The Magnetic Force Formula (Vector Form)

The magnetic part of the Lorentz force is determined by the cross product of the velocity and magnetic field vectors:

$$\vec{F}_m = q(\vec{v} \times \vec{B})$$



To find the **magnitude** of the force, we first need to calculate the cross product vector $\vec{v} \times \vec{B}$.

---

#### 3. Calculate the Cross Product ($\vec{v} \times \vec{B}$)

Using the determinant method:

$$\vec{v} \times \vec{B} = \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ 2 & -4 & 1 \\ 1 & 2 & -1 \end{vmatrix}$$

**Step-by-step expansion:**

* **$\hat{i}$ component:** $(-4)(-1) - (1)(2) = 4 - 2 = 2$
* **$\hat{j}$ component:** $-\left[ (2)(-1) - (1)(1) \right] = -[-2 - 1] = 3$
* **$\hat{k}$ component:** $(2)(2) - (-4)(1) = 4 + 4 = 8$

So, the resulting vector is:
$$\vec{v} \times \vec{B} = (2\hat{i} + 3\hat{j} + 8\hat{k})$$

---

#### 4. Calculate the Magnitude of the Cross Product

Now, we find the magnitude of the vector we just calculated:

$$|\vec{v} \times \vec{B}| = \sqrt{2^2 + 3^2 + 8^2}$$
$$|\vec{v} \times \vec{B}| = \sqrt{4 + 9 + 64}$$
$$|\vec{v} \times \vec{B}| = \sqrt{77} \approx 8.775$$

---

#### 5. Calculate the Final Force Magnitude

Now, multiply the result by the charge of the proton ($q$):

$$F = q \cdot |\vec{v} \times \vec{B}|$$
$$F = (1.6 \times 10^{-19}\text{ C}) \cdot \sqrt{77}$$
$$F \approx 1.6 \times 10^{-19} \cdot 8.775$$
$$F \approx 1.404 \times 10^{-18}\text{ N}$$

---

### Final Result

The magnitude of the magnetic force is:

**$$F \approx 1.40 \times 10^{-18}\text{ N}$$**
