# Problem 12: Work and Energy with a Constant Force

---

## 1. Given Data

* **Mass ($m$):** $2 \text{ kg}$
* **Constant Force ($\vec{F}$):** $(6, 2) \text{ N}$
* **Initial Velocity ($\vec{v}_0$):** $(1, -1) \text{ m/s}$
* **Initial Position ($\vec{r}_0$):** $(0, 0) \text{ m}$

---

## 2. Kinematic Analysis

### Part 1: Acceleration
Using Newton’s Second Law, the acceleration is constant:

$$\vec{a} = \frac{\vec{F}}{m} = \left( \frac{6}{2}, \frac{2}{2} \right) = \mathbf{(3, 1) \text{ m/s}^2}$$


### Part 2: Velocity as a Function of Time
Using the kinematic equation for constant acceleration:

$$\vec{v}(t) = \vec{v}_0 + \vec{a}t$$

$$\vec{v}(t) = (1, -1) + (3, 1)t = \mathbf{(1 + 3t, -1 + t) \text{ m/s}}$$


### Part 3: Position as a Function of Time
Applying the displacement formula:

$$\vec{r}(t) = \vec{r}_0 + \vec{v}_0t + \frac{1}{2}\vec{a}t^2$$

$$\vec{r}(t) = (0, 0) + (1, -1)t + \frac{1}{2}(3, 1)t^2 = \mathbf{\left( t + \frac{3}{2}t^2, -t + \frac{1}{2}t^2 \right) \text{ m}}$$

---

## 3. Trajectory and Work

### Part 4: Trajectory (Path of Motion)
The parametric equations for the path are:

* $x(t) = t + 1.5t^2$
* $y(t) = -t + 0.5t^2$

Since acceleration is constant and directed at $(3, 1)$, the trajectory is a **parabola** that curves toward the direction of the applied force.


### Part 5: Work Done by the Force at $t = 3 \text{ s}$
First, calculate the displacement vector $\Delta \vec{r}$ at $t = 3$:

$$\vec{r}(3) = \left( 3 + \frac{3}{2}(9), -3 + \frac{1}{2}(9) \right) = (16.5, 1.5) \text{ m}$$

Since $\vec{r}_0 = (0,0)$, then $\Delta \vec{r} = (16.5, 1.5) \text{ m}$.

**Work Calculation ($W = \vec{F} \cdot \Delta \vec{r}$):**

$$W = (6 \times 16.5) + (2 \times 1.5) = 99 + 3 = \mathbf{102 \text{ J}}$$

---

## 4. Verification: Work–Energy Theorem
The theorem states that the net work equals the change in kinetic energy: $W = \Delta KE$.


### Initial Kinetic Energy ($t = 0$)

$$KE_0 = \frac{1}{2} m v_0^2 = \frac{1}{2} \times 2 \times (1^2 + (-1)^2) = \mathbf{2 \text{ J}}$$


### Final Kinetic Energy ($t = 3$)
Find the velocity at $t = 3 \text{ s}$:

$$\vec{v}(3) = (1 + 9, -1 + 3) = (10, 2) \text{ m/s}$$

$$KE_f = \frac{1}{2} \times 2 \times (10^2 + 2^2) = \mathbf{104 \text{ J}}$$


### Comparison

$$\Delta KE = 104\text{ J} - 2\text{ J} = \mathbf{102 \text{ J}}$$

**Conclusion:** The change in kinetic energy matches the work calculated ($102\text{ J}$), confirming the **Work–Energy Theorem**.
