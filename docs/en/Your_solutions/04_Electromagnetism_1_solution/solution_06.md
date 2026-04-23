### Question 6: Field at a point from a system of charges

**Two point charges are given:**
* $+q$ at point $(-a, 0)$
* $+2q$ at point $(a, 0)$

**Tasks:**
1. Determine the field vector $\vec{E}(0,y)$, $\vec{E}(x,0)$ and generally $\vec{E}(x,y)$.
2. Determine the condition for which the components $E_x=0$, $E_y=0$ and the zero field $\vec{E}=0$.
3. Calculate the field for: $a = 0.2$ m, $y = 0.3$ m, $q = 2 \mu C$.
4. Investigate the limit $y \gg a$.

---

### 1. Intuition & The "Far-Field" Limit (The Best Part)

Before diving into the heavy vector math, let's look at the final task: the limit where $y \gg a$. This is the most physically interesting part of the problem and shows a deep understanding of how the universe works.

**The Concept:** Imagine you are standing incredibly far away along the y-axis. From a massive distance, the small physical separation ($2a$) between the two charges becomes completely negligible. 

Your instruments can no longer resolve two distinct charges; they blur together into a single point. 

Because electric fields obey the **principle of superposition**, the individual fields simply add together. Therefore, from far away, a $+q$ and a $+2q$ charge sitting close together will act exactly like a single, unified $+3q$ point charge sitting right at the origin. 

Mathematically, as $y \to \infty$, the complex electric field equation should simply collapse into Coulomb's standard law for a single $3q$ charge: 

$$E \approx \frac{k(3q)}{y^2}$$

*(We will prove this mathematically in Step 4!)*

<br>

---

### 2. Finding the Zero Field ($\vec{E} = 0$)

Where do the electric fields from these two charges perfectly cancel each other out? 

**The Physical "Tug-of-War":**
* Because both charges are positive, their electric fields push away from each other along the x-axis. 
* Therefore, the "zero point" *must* be located somewhere on the x-axis ($y=0$) directly between them. 
* Because the $+2q$ charge on the right is twice as strong, it pushes harder. This means the zero point must be shoved closer to the weaker $+q$ charge on the left.

**The Math:**
Let's set the opposing fields equal to each other for the region between the charges ($-a < x < a$):

$$\frac{kq}{(x+a)^2} = \frac{k(2q)}{(a-x)^2}$$

*(Note: We use $(a-x)^2$ for the second term to represent the distance pointing leftward from the $+2q$ charge).*

1. Cancel $kq$ from both sides and cross-multiply:
$$(a-x)^2 = 2(x+a)^2$$

2. Take the square root of both sides (choosing the physical root inside our bounds):
$$a - x = \sqrt{2}(x + a)$$

3. Expand and solve for $x$:
$$a - x = \sqrt{2}x + \sqrt{2}a$$
$$a - \sqrt{2}a = x + \sqrt{2}x$$
$$a(1 - \sqrt{2}) = x(1 + \sqrt{2})$$

$$x = a\left(\frac{1-\sqrt{2}}{1+\sqrt{2}}\right)$$

*(Notice that $\frac{1-\sqrt{2}}{1+\sqrt{2}}$ yields a negative number. This perfectly proves our intuition: the zero point is at a negative x-coordinate, meaning it sits closer to the weaker $+q$ charge on the left!)*

<br>

---

### 3. The General Math: Vectors & Superposition

To find the General Electric Field ($\vec{E}$) at any random point $(x,y)$, we must add the field from charge 1 ($\vec{E}_1$) and charge 2 ($\vec{E}_2$) using vector components. 

The general formula for an electric field vector at a distance $\vec{r}$ is:

$$\vec{E} = \frac{kq}{r^3} \vec{r}$$

*(Pro-Tip: Using $\vec{r}/r^3$ instead of the standard unit vector $\hat{r}/r^2$ makes splitting things into $x$ and $y$ components much easier for calculus!)*

**For Charge 1 ($+q$ at $-a, 0$):**
* Distance vector $\vec{r}_1$: from $(-a, 0)$ to $(x,y)$ is $(x+a)\hat{i} + y\hat{j}$
* Magnitude cubed $r_1^3$: $\left((x+a)^2 + y^2\right)^{3/2}$

**For Charge 2 ($+2q$ at $a, 0$):**
* Distance vector $\vec{r}_2$: from $(a, 0)$ to $(x,y)$ is $(x-a)\hat{i} + y\hat{j}$
* Magnitude cubed $r_2^3$: $\left((x-a)^2 + y^2\right)^{3/2}$

**The General Field $\vec{E}(x,y)$:**

$$E_x(x,y) = kq\left[ \frac{x+a}{\left((x+a)^2 + y^2\right)^{3/2}} + \frac{2(x-a)}{\left((x-a)^2 + y^2\right)^{3/2}} \right]$$

$$E_y(x,y) = kq\left[ \frac{y}{\left((x+a)^2 + y^2\right)^{3/2}} + \frac{2y}{\left((x-a)^2 + y^2\right)^{3/2}} \right]$$

*(To answer the first part of the prompt: to find $\vec{E}(0,y)$ or $\vec{E}(x,0)$, you simply plug 0 in for $x$ or $y$ in these master equations).*

<br>

---

### 4. Proving the Far-Field Limit ($y \gg a$)

Let's return to our intuition from Step 1 and prove it using the equations we just built. 

We will look at a point straight up the y-axis ($x=0$) and push it toward infinity. 
From our general equation, setting $x=0$ gives:

$$E_y(0,y) = kq\left[ \frac{y}{\left(a^2 + y^2\right)^{3/2}} + \frac{2y}{\left((-a)^2 + y^2\right)^{3/2}} \right]$$

If $y$ is massive compared to $a$ ($y \gg a$), the $a^2$ term essentially becomes zero relative to $y^2$. We can ignore it. 
The denominator simplifies heavily: $(y^2)^{3/2} = y^3$.

$$E_y \approx kq\left[ \frac{y}{y^3} + \frac{2y}{y^3} \right]$$

$$E_y \approx kq\left[ \frac{1}{y^2} + \frac{2}{y^2} \right]$$

$$E_y \approx \frac{k(3q)}{y^2}$$

**Conclusion:** The math perfectly matches our physical intuition! From far away, the field acts exactly like a single $+3q$ point charge at the origin.

<br>

---

### 5. Numerical Calculation

**Given values:** * $a = 0.2$ m
* $y = 0.3$ m
* $q = 2 \times 10^{-6}$ C
* Coulomb's constant $k \approx 8.99 \times 10^9$ $\text{N}\cdot\text{m}^2/\text{C}^2$

We are finding $\vec{E}(0, 0.3)$. 

**1. Calculate the shared denominator:**
Since $x=0$, both denominators are the same: 
$$r^3 = (0.2^2 + 0.3^2)^{3/2} = (0.04 + 0.09)^{3/2} = (0.13)^{3/2} \approx 0.0468$$

**2. Calculate $E_x$:**
$$E_x = (8.99 \times 10^9)(2 \times 10^{-6}) \left[ \frac{0.2}{0.0468} + \frac{2(-0.2)}{0.0468} \right]$$

$$E_x \approx 17980 \times [ 4.27 - 8.55 ]$$

$$E_x \approx 17980 \times (-4.28) \approx -7.69 \times 10^4 \text{ N/C}$$
*(Notice that $E_x$ is negative! This makes sense: the stronger $+2q$ charge on the right pushes the test charge harder to the left than the weaker $+q$ pushes it to the right).*

**3. Calculate $E_y$:**
$$E_y = (8.99 \times 10^9)(2 \times 10^{-6}) \left[ \frac{0.3}{0.0468} + \frac{2(0.3)}{0.0468} \right]$$

$$E_y \approx 17980 \times [ 6.41 + 12.82 ]$$

$$E_y \approx 17980 \times (19.23) \approx 3.45 \times 10^5 \text{ N/C}$$

<br>

### Final Result Vector

**$\vec{E} = (-7.69 \times 10^4 \hat{i} + 3.45 \times 10^5 \hat{j}) \text{ N/C}$**
