# 6. Function Analysis

**Problem:** Identify any local maxima or minima for the function $f(x) = 3x^2 - 12x + 7$.

---

### **1. State the Original Function**
We begin with the quadratic function:
$$f(x) = 3x^2 - 12x + 7$$

---

### **2. Differentiate the Function**
To find the slope, we apply the power rule ($nx^{n-1}$) to each term. We differentiate the original function to find the rate of change:
$$f'(x) = \frac{d}{dx}(3x^2) - \frac{d}{dx}(12x) + \frac{d}{dx}(7)$$

$$f'(x) = 6x - 12$$

> **Note:** The derivative $f'(x)$ represents the slope of the graph at any point $x$.

---

### **3. Find the Critical Point**
The graph reaches a "stationary point" (a local maximum or minimum) when it stops climbing or falling. We set the slope to zero to find this exact moment:
$$6x - 12 = 0$$

$$6x = 12$$

**$$x = 2$$**

---

### **4. Calculate the Y-Coordinate**
Now that we have the $x$-value of the critical point, we substitute it back into the **original** function $f(x)$ to find the height of the graph at that point:
$$f(2) = 3(2)^2 - 12(2) + 7$$

$$f(2) = 3(4) - 24 + 7$$

$$f(2) = 12 - 24 + 7$$

**$$f(2) = -5$$**



---

### **5. Classify the Critical Point**
We need to know if $(2, -5)$ is a peak or a valley. Since the coefficient of $x^2$ is positive ($3$), the parabola opens upward, which indicates a minimum.

* **Second Derivative Test:** $f''(x) = 6$.
* Because the second derivative is **positive ($6 > 0$)**, the graph is concave up, confirming that $(2, -5)$ is a **local minimum**.

---

### **[GeoGebra Visualization](https://www.geogebra.org/calculator/vcq79med)**


1. **Input:** `f(x) = 3x^2 - 12x + 7`
2. **Vertex:** Use the `Extremum(f)` command to confirm the minimum is at $(2, -5)$.
3. **Slope:** Input `f'(x)` to verify the derivative line crosses the x-axis exactly at $x=2$.
