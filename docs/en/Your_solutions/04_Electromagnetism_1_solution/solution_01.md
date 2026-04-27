# 1. Coulomb's Law

### Problem Statement
Four point charges of $+1.0\text{ C}$ each are placed at the corners of a square with sides of $1.0\text{ m}$. Calculate the magnitude and direction of the electric force on a charge of $-2.0\text{ C}$ placed at the center of the square.

---

### Solution

#### 1. Identify the Given Information
* **Corner charges ($q$):** $+1.0\text{ C}$ each.
* **Center charge ($q_0$):** $-2.0\text{ C}$.
* **Side length of the square ($a$):** $1.0\text{ m}$.
* **Coulomb's constant ($k$):** $\approx 8.99 \times 10^9\text{ N}\cdot\text{m}^2/\text{C}^2$.

#### 2. Determine the Distance to the Center
The distance $r$ from a corner to the center of the square is half the length of the diagonal.
The diagonal $d$ is:
$$d = a\sqrt{2} = 1.0\sqrt{2}\text{ m}$$

The distance $r$ is:
$$r = \frac{d}{2} = \frac{\sqrt{2}}{2}\text{ m}$$

The square of the distance is:
$$r^2 = \left(\frac{\sqrt{2}}{2}\right)^2 = \frac{2}{4} = 0.5\text{ m}^2$$



#### 3. Calculate Force Magnitude
The magnitude of the force exerted by any single corner charge on the center charge is:
$$F = k \frac{|q \cdot q_0|}{r^2}$$
$$F = (8.99 \times 10^9) \frac{|1.0 \cdot (-2.0)|}{0.5}$$
$$F = (8.99 \times 10^9) \cdot 4$$
$$F = 3.596 \times 10^{10}\text{ N}$$

#### 4. Vector Analysis and Symmetry
The center charge is negative, and the corner charges are positive. This means the forces are **attractive**, pulling the center charge toward each corner.

* The force from the **top-left** corner pulls toward the top-left.
* The force from the **bottom-right** corner pulls toward the bottom-right.
* The force from the **top-right** corner pulls toward the top-right.
* The force from the **bottom-left** corner pulls toward the bottom-left.

Because the magnitudes of the charges and the distances are all identical:
1.  The force vector from the top-left corner is cancelled by the force vector from the bottom-right corner.
2.  The force vector from the top-right corner is cancelled by the force vector from the bottom-left corner.

#### Final Result
The net electric force is the vector sum of these four forces. Due to the perfect symmetry:
$$\vec{F}_{net} = 0\text{ N}$$

* **Magnitude:** $0\text{ N}$
* **Direction:** Undefined (The charge is in static equilibrium).
