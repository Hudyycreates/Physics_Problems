# Work and Energy: Calculus-Based Solution

## 1. Initial Parameters

* **Mass ($m$):** $2$ kg
* **Constant Force ($\vec{F}$):** $[6, 2]$ N
* **Initial Velocity ($\vec{v}_0$):** $[1, -1]$ m/s
* **Initial Position ($\vec{r}_0$):** $[0, 0]$ m

---

## 2. Deriving Kinematics through Integration

### Step 1: Acceleration Vector $\vec{a}(t)$

Using Newton's Second Law:
$$\vec{a} = \frac{\vec{F}}{m}$$

$$\vec{a}(t) = \left[ \frac{6}{2}, \frac{2}{2} \right]$$

**Result:**
$$\vec{a}(t) = [3, 1] \text{ m/s}^2$$

---

### Step 2: Velocity Vector $\vec{v}(t)$

Velocity is the integral of acceleration with respect to time:
$$\vec{v}(t) = \int \vec{a} \, dt = \int [3, 1] \, dt$$

$$\vec{v}(t) = [3t + C_x, t + C_y]$$

Using the initial condition $\vec{v}(0) = [1, -1]$:
* $3(0) + C_x = 1 \implies C_x = 1$
* $0 + C_y = -1 \implies C_y = -1$

**Result:**
$$\vec{v}(t) = [3t + 1, t - 1] \text{ m/s}$$

---

### Step 3: Position Vector $\vec{r}(t)$

Position is the integral of velocity with respect to time:
$$\vec{r}(t) = \int \vec{v}(t) \, dt = \int [3t + 1, t - 1] \, dt$$

$$\vec{r}(t) = \left[ \frac{3}{2}t^2 + t + K_x, \frac{1}{2}t^2 - t + K_y \right]$$

Using the initial condition $\vec{r}(0) = [0, 0]$:
* $K_x = 0$
* $K_y = 0$

**Result:**
$$\vec{r}(t) = [1.5t^2 + t, 0.5t^2 - t] \text{ m}$$

---

## 3. Trajectory Analysis

### Step 4: Path of Motion (Trajectory)

To understand the path, we look at the parametric equations for $x$ and $y$:
1. $x(t) = 1.5t^2 + t$
2. $y(t) = 0.5t^2 - t$

**Description:**
Since the acceleration vector $[3, 1]$ is constant and the initial velocity is not parallel to the force, the body follows a **parabolic path**. 

As $t \to \infty$, the quadratic terms dominate, and the trajectory aligns more closely with the direction of the force vector.

---

## 4. Work Calculation ($t = 3$ s)

To find the work done, we use the line integral of power over time:
$$W = \int_{0}^{3} \vec{F} \cdot \vec{v}(t) \, dt$$

### Step 5: Dot Product Calculation

$$\vec{F} \cdot \vec{v}(t) = [6, 2] \cdot [3t + 1, t - 1]$$
$$= 6(3t + 1) + 2(t - 1)$$
$$= 18t + 6 + 2t - 2$$
$$\vec{F} \cdot \vec{v}(t) = 20t + 4$$

---

### Step 6: Integration for Work

$$W = \int_{0}^{3} (20t + 4) \, dt$$
$$W = \left[ 10t^2 + 4t \right]_{0}^{3}$$
$$W = (10(3)^2 + 4(3)) - 0$$

**Total Work Done:**
$$W = 102 \text{ J}$$

---

## 5. Work-Energy Theorem Verification

### Step 7: Change in Kinetic Energy ($\Delta KE$)

Kinetic Energy formula: $KE = \frac{1}{2}m|\vec{v}|^2$. Since $m=2$, $KE = |\vec{v}|^2$.

**At $t = 0$ s:**
$$\vec{v}(0) = [1, -1]$$
$$KE_i = (1)^2 + (-1)^2 = 2 \text{ J}$$

**At $t = 3$ s:**
$$\vec{v}(3) = [3(3)+1, (3)-1] = [10, 2]$$
$$KE_f = (10)^2 + (2)^2 = 104 \text{ J}$$

**Change in Energy:**
$$\Delta KE = 104 - 2 = 102 \text{ J}$$

---

### Final Conclusion

The work done calculated via integration ($102$ J) is identical to the change in kinetic energy ($102$ J). 

**The Work-Energy Theorem is verified.**
