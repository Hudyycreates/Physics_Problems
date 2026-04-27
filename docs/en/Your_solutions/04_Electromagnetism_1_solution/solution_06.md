# 6. Field at a point from a system of charges

### Problem Statement

Two point charges are given:
* $+q$ at point $(-a, 0)$
* $+2q$ at point $(a, 0)$

1.  Determine the field vector $\vec{E}(0, y)$, $\vec{E}(x, 0)$, and generally $\vec{E}(x, y)$.
2.  Determine the conditions for which $E_x = 0$, $E_y = 0$, and the zero field point $\vec{E} = 0$.
3.  Calculate the field for: $a = 0.2\text{ m}$, $y = 0.3\text{ m}$, $q = 2\text{ }\mu\text{C}$ at point $(0, y)$.
4.  Investigate the limit $y \gg a$.

---

### Solution

#### 1. General Field Vector $\vec{E}(x, y)$

Let $\vec{r}_1 = (-a, 0)$ and $\vec{r}_2 = (a, 0)$. For any point $P(x, y)$, the displacement vectors from the charges are:
* $\vec{r}_{P1} = (x + a)\hat{i} + y\hat{j}$ with magnitude $r_1 = \sqrt{(x+a)^2 + y^2}$
* $\vec{r}_{P2} = (x - a)\hat{i} + y\hat{j}$ with magnitude $r_2 = \sqrt{(x-a)^2 + y^2}$

The total electric field is $\vec{E} = \vec{E}_1 + \vec{E}_2$:

$$\vec{E}(x, y) = kq \left[ \frac{(x+a)\hat{i} + y\hat{j}}{((x+a)^2 + y^2)^{3/2}} + \frac{2((x-a)\hat{i} + y\hat{j})}{((x-a)^2 + y^2)^{3/2}} \right]$$



---

#### 2. Specific Field Vectors

**Case A: On the y-axis, $\vec{E}(0, y)$**
At $x = 0$, the distances are equal: $r_1 = r_2 = \sqrt{a^2 + y^2}$.
* $E_x(0, y) = kq \left[ \frac{a}{(a^2+y^2)^{3/2}} + \frac{2(-a)}{(a^2+y^2)^{3/2}} \right] = -\frac{kqa}{(a^2+y^2)^{3/2}}$
* $E_y(0, y) = kq \left[ \frac{y}{(a^2+y^2)^{3/2}} + \frac{2y}{(a^2+y^2)^{3/2}} \right] = \frac{3kqy}{(a^2+y^2)^{3/2}}$

$$\vec{E}(0, y) = \frac{kq}{(a^2 + y^2)^{3/2}} (-a\hat{i} + 3y\hat{j})$$

**Case B: On the x-axis, $\vec{E}(x, 0)$**
At $y = 0$, the vertical component $E_y$ is $0$. The horizontal component depends on the region:
$$\vec{E}(x, 0) = kq \left[ \frac{\text{sgn}(x+a)}{(x+a)^2} + \frac{2\text{sgn}(x-a)}{(x-a)^2} \right] \hat{i}$$

---

#### 3. Conditions for Zero Components

* **For $E_y = 0$:**
    From the general formula, $E_y = kqy \left( \frac{1}{r_1^3} + \frac{2}{r_2^3} \right)$. Since both charges are positive, the term in parentheses is always positive. Therefore, **$E_y = 0$ only when $y = 0$** (anywhere on the x-axis).

* **For $E_x = 0$:**
    On the y-axis ($x=0$), $E_x$ is never zero for finite $y$.
    On the x-axis ($y=0$), the field can cancel between the charges where they push in opposite directions. This occurs at a point $x$ where:
    $$\frac{1}{(x+a)^2} = \frac{2}{(a-x)^2}$$
    Taking the square root: $\frac{1}{x+a} = \frac{\sqrt{2}}{a-x} \implies a-x = \sqrt{2}x + \sqrt{2}a$
    Solving for $x$: $x = a \frac{1-\sqrt{2}}{1+\sqrt{2}} \approx -0.171a$.

* **For $\vec{E} = 0$:**
    Both components must be zero. This happens at:
    **$y = 0$ and $x \approx -0.171a$**.

---

#### 4. Numerical Calculation at $(0, 0.3)$

**Given:** $a = 0.2\text{ m}$, $y = 0.3\text{ m}$, $q = 2 \times 10^{-6}\text{ C}$.
1.  **Calculate $r$:** $r = \sqrt{0.2^2 + 0.3^2} = \sqrt{0.13} \approx 0.3606\text{ m}$
2.  **Calculate $kq$:** $kq \approx (8.99 \times 10^9)(2 \times 10^{-6}) = 17,980\text{ N}\cdot\text{m}^2/\text{C}$
3.  **Components:**
    * $E_x = -\frac{17980 \cdot 0.2}{(0.13)^{3/2}} \approx -76,717\text{ N/C}$
    * $E_y = \frac{3 \cdot 17980 \cdot 0.3}{(0.13)^{3/2}} \approx 345,228\text{ N/C}$

**Result:** $\vec{E} \approx (-7.67 \times 10^4 \hat{i} + 3.45 \times 10^5 \hat{j})\text{ N/C}$

---

#### 5. Limit $y \gg a$

When the observation point is very far away, the distance $r \approx y$.
* $E_x \approx -\frac{kqa}{y^3}$ (Falls off very rapidly)
* $E_y \approx \frac{3kqy}{y^3} = \frac{k(3q)}{y^2}$

**Conclusion:** At great distances, the system behaves like a single point charge of magnitude **$Q = 3q$** located at the origin.
