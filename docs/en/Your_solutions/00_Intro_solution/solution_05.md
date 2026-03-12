# 5. Trigonometry: Resolving Vectors

**Problem:** A vector $\vec{A}$ has a magnitude of $15$ and makes an angle of $\theta = 60^{\circ}$ with the horizontal axis. Calculate its horizontal ($A_x$) and vertical ($A_y$) components.

**Context:** Any vector acting at an angle can be broken down into two perpendicular components. 



---

### **1. Geometric Setup**

To resolve the vector, we treat it as a triangle where:

* **Hypotenuse**: The total magnitude of the vector ($15$).
* **Horizontal side ($A_x$)**: The adjacent side to the angle.
* **Vertical side ($A_y$)**: The opposite side to the angle.



We use the **SOH CAH TOA** mnemonic to relate the angle to the sides:
* **CAH**: $\cos(\theta) = \frac{\text{Adjacent}}{\text{Hypotenuse}} \rightarrow A_x = A \cos(\theta)$
* **SOH**: $\sin(\theta) = \frac{\text{Opposite}}{\text{Hypotenuse}} \rightarrow A_y = A \sin(\theta)$

---

### **2. Calculation**

**Step 1: Calculate the horizontal component ($A_x$)**

$$A_x = 15 \cdot \cos(60^{\circ})$$

$$A_x = 15 \cdot 0.5$$

**$$A_x = 7.5$$**

---

**Step 2: Calculate the vertical component ($A_y$)**

$$A_y = 15 \cdot \sin(60^{\circ})$$

$$A_y = 15 \cdot 0.866$$

**$$A_y \approx 12.99$$**

---

### **3. Verification & Analysis**

* **Why $A_y > A_x$:** Because the angle ($60^{\circ}$) is greater than $45^{\circ}$, the vector is steeper. This means the magnitude is skewed more toward the vertical axis than the horizontal.

* **Pythagorean Check:** We can verify our components using the theorem $\sqrt{A_x^2 + A_y^2} = A$:

    $$\sqrt{7.5^2 + 12.99^2} \approx \sqrt{56.25 + 168.74} \approx \sqrt{224.99} \approx 15$$

    The result matches our original magnitude, confirming the resolution is accurate.
