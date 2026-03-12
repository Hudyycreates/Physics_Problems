# 8. Definite Integrals

**Problem:** Calculate the area under the curve of the function $f(x) = \sin(x)$ from $x = 0$ to $x = \pi$.

---

### **1. Identify the Goal**

The area under a curve is found by calculating the **definite integral** of the function over the given interval. We are solving for:

$$\text{Area} = \int_{0}^{\pi} \sin(x) \, dx$$

---

### **2. Find the Antiderivative**

First, we find the function whose derivative is $\sin(x)$. 

* The derivative of $\cos(x)$ is $-\sin(x)$.
* Therefore, the antiderivative of $\sin(x)$ is **$-\cos(x)$**.

---

### **3. Apply the Fundamental Theorem of Calculus**

We evaluate the antiderivative at the upper limit ($\pi$) and subtract the value at the lower limit ($0$):

$$\text{Area} = \left[ -\cos(x) \right]_{0}^{\pi}$$

---

### **4. Calculate the Final Value**

Substitute the trigonometric values from the unit circle where $\cos(\pi) = -1$ and $\cos(0) = 1$:

$$\text{Area} = (-\cos(\pi)) - (-\cos(0))$$

$$\text{Area} = (-(-1)) - (-1)$$

$$\text{Area} = 1 + 1$$

**$$\text{Area} = 2$$**



---

### **Extra Notes for Context**

* **Positive Area:** Since the sine curve is above the x-axis between $0$ and $\pi$, the area is positive.
* **Net Change:** If you integrated from $0$ to $2\pi$, the result would be $0$ because the area below the axis would cancel out the area above it.
* **Symmetry:** Because of the curve's symmetry, the area from $0$ to $\frac{\pi}{2}$ is exactly $1$.
