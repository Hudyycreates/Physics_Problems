# 3. Electrostatic Equilibrium

### Problem Statement

Find the equilibrium position for a charge $q_3 = +1\text{ C}$ placed on the line between a charge $q_1 = +4\text{ C}$ and a charge $q_2 = +9\text{ C}$, which are separated by a distance of $2.0\text{ m}$.

---

### Solution

#### 1. Identify the Given Information

* **Charge 1 ($q_1$):** $+4\text{ C}$ (Source charge at $x = 0$)
* **Charge 2 ($q_2$):** $+9\text{ C}$ (Source charge at $x = L$)
* **Test Charge ($q_3$):** $+1\text{ C}$ (The charge we are positioning)
* **Separation distance ($L$):** $2.0\text{ m}$
* **Distance from $q_1$ to $q_3$:** $x$
* **Distance from $q_3$ to $q_2$:** $L - x = (2.0 - x)$

---

#### 2. The Condition for Equilibrium

For the charge $q_3$ to be in **electrostatic equilibrium**, the net force acting on it must be zero ($\sum F = 0$).

Because $q_3$ is placed *between* two positive charges:
1.  $q_1$ repels $q_3$ to the **right**.
2.  $q_2$ repels $q_3$ to the **left**.

Equilibrium occurs when the magnitude of the force from $q_1$ equals the magnitude of the force from $q_2$:

$$F_{13} = F_{23}$$



---

#### 3. Mathematical Set-up

Using **Coulomb's Law**:

$$\frac{k |q_1 q_3|}{x^2} = \frac{k |q_2 q_3|}{(L - x)^2}$$

We can simplify this equation immediately:
* The constant $k$ cancels out.
* The charge $q_3$ cancels out (meaning the equilibrium position is independent of the magnitude or sign of the third charge).

This leaves us with:
$$\frac{q_1}{x^2} = \frac{q_2}{(L - x)^2}$$

---

#### 4. Solving for $x$

Substitute the known values ($q_1 = 4$, $q_2 = 9$, $L = 2$):

$$\frac{4}{x^2} = \frac{9}{(2 - x)^2}$$

**Step A: Take the square root of both sides**
Taking the square root is the easiest way to solve this without dealing with a complex quadratic equation:

$$\sqrt{\frac{4}{x^2}} = \sqrt{\frac{9}{(2 - x)^2}}$$

$$\frac{2}{x} = \frac{3}{2 - x}$$

**Step B: Cross-multiply**
$$2(2 - x) = 3x$$

**Step C: Expand and solve**
$$4 - 2x = 3x$$
$$4 = 5x$$
$$x = \frac{4}{5}$$
$$x = 0.8\text{ m}$$

---

### Final Result

The equilibrium position for $q_3$ is:

**$$x = 0.8\text{ m} \text{ from the } +4\text{ C charge}$$**

*(Or $1.2\text{ m}$ from the $+9\text{ C}$ charge)*
