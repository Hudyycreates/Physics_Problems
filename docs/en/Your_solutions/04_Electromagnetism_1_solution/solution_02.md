# 2. Electric Potential

### Problem Statement

Point charges of $+1\text{ C}$, $-2\text{ C}$, $+3\text{ C}$, and $-4\text{ C}$ are placed at the corners of a square with sides of $1.0\text{ m}$ (in order). 

Calculate the electric potential at the center of the square.

---

### Solution

#### 1. Identify the Given Information

* **Charges:** * $q_1 = +1\text{ C}$
    * $q_2 = -2\text{ C}$
    * $q_3 = +3\text{ C}$
    * $q_4 = -4\text{ C}$
* **Side length ($a$):** $1.0\text{ m}$
* **Coulomb's constant ($k$):** $\approx 8.99 \times 10^9\text{ N}\cdot\text{m}^2/\text{C}^2$

---

#### 2. Determine the Distance to the Center ($r$)

Electric potential ($V$) is a **scalar quantity**. This means we only need the magnitude of the distance from each charge to the center; we do not need to account for angles or directions.

In a square, the distance from any corner to the center is half the length of the diagonal ($d$).

1.  **Calculate the diagonal ($d$):**
    $$d = a\sqrt{2} = 1.0\sqrt{2}\text{ m}$$

2.  **Calculate the distance to center ($r$):**
    $$r = \frac{d}{2} = \frac{1.0\sqrt{2}}{2} = \frac{\sqrt{2}}{2}\text{ m} \approx 0.707\text{ m}$$

3.  **Square of the distance (for reference):**
    $$r^2 = 0.5\text{ m}^2$$

---

#### 3. Formula for Total Electric Potential

The total electric potential at the center is the algebraic sum of the potentials created by each individual charge:

$$V_{total} = V_1 + V_2 + V_3 + V_4$$

Since $V = \frac{kq}{r}$, and $k$ and $r$ are the same for every charge in this specific geometry, we can factor them out:

$$V_{total} = \frac{k}{r} (q_1 + q_2 + q_3 + q_4)$$



---

#### 4. Final Calculation

**Step A: Sum the charges**
$$\sum q = (+1\text{ C}) + (-2\text{ C}) + (+3\text{ C}) + (-4\text{ C}) = -2\text{ C}$$

**Step B: Substitute values into the equation**
$$V_{total} = \frac{8.99 \times 10^9}{0.707} \cdot (-2)$$

**Step C: Solve**
$$V_{total} \approx (1.271 \times 10^{10}) \cdot (-2)$$
$$V_{total} \approx -2.54 \times 10^{10}\text{ V}$$

---

### Final Result

The electric potential at the center of the square is:

**$$V = -2.54 \times 10^{10}\text{ V}$$**

*(This can also be written as $-25.4\text{ GV}$)*
