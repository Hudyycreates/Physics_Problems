# 6. EM Wave Analysis

### Problem Statement

An electromagnetic wave has its electric field component described by:
$$E_y(x,t) = 100 \sin(10^7 x - \omega t)\text{ V/m}$$

**Determine:**
1.  Direction of propagation.
2.  Wavelength $\lambda$.
3.  Angular frequency $\omega$.
4.  The equation for the magnetic field component $B_z(x,t)$.

---

### Solution

#### 1. Direction of Propagation
The argument of the sine function is $(kx - \omega t)$. 
* Because the variable is $x$, the wave travels along the **x-axis**.
* Because the signs of $kx$ and $\omega t$ are opposite (one positive, one negative), the wave travels in the **positive x-direction ($+x$)**.

---

#### 2. Calculate Wavelength ($\lambda$)
From the wave equation, the wave number $k = 10^7\text{ rad/m}$.
The relationship between $k$ and $\lambda$ is:
$$\lambda = \frac{2\pi}{k}$$

$$\lambda = \frac{2\pi}{10^7} \approx 6.28 \times 10^{-7}\text{ m}$$
**(or $628\text{ nm}$)**

---

#### 3. Calculate Angular Frequency ($\omega$)
In a vacuum, the speed of light $c = \frac{\omega}{k}$. Therefore:
$$\omega = c \cdot k$$

$$\omega = (3.0 \times 10^8\text{ m/s}) \cdot (10^7\text{ rad/m})$$
**$$\omega = 3.0 \times 10^{15}\text{ rad/s}$$**



---

#### 4. Equation for Magnetic Field ($B_z$)
The magnetic field amplitude is related to the electric field amplitude by $B_0 = \frac{E_0}{c}$:
$$B_0 = \frac{100}{3.0 \times 10^8} \approx 3.33 \times 10^{-7}\text{ T}$$

In an EM wave, $\vec{E}$ and $\vec{B}$ are perpendicular to each other and to the direction of propagation. Since $\vec{E}$ is in the $y$-direction and propagation is in the $x$-direction, $\vec{B}$ must be in the **z-direction**.

The phase remains the same as the electric field:
**$$B_z(x,t) = 3.33 \times 10^{-7} \sin(10^7 x - 3.0 \times 10^{15} t)\text{ T}$$**
