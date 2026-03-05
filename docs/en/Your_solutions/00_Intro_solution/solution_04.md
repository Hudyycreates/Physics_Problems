```python
import sympy

# Define symbols
T, L, g = sympy.symbols('T L g', positive=True)
pi = sympy.pi

# Define the equation T = 2*pi*sqrt(L/g)
equation = sympy.Eq(T, 2 * pi * sympy.sqrt(L / g))

# Solve for g
solution = sympy.solve(equation, g)

print(f"Solution for g: {solution}")



```

```text
Solution for g: [4*pi**2*L/T**2]


```

To rearrange the formula for the period of a simple pendulum to solve for $g$, follow these algebraic steps:

1. **Start with the original formula:**

$$T = 2\pi \sqrt{\frac{L}{g}}$$


2. **Divide both sides by $2\pi$ to isolate the square root:**

$$\frac{T}{2\pi} = \sqrt{\frac{L}{g}}$$


3. **Square both sides of the equation to remove the square root:**

$$\left(\frac{T}{2\pi}\right)^2 = \frac{L}{g}$$


$$\frac{T^2}{4\pi^2} = \frac{L}{g}$$


4. **Multiply both sides by $g$ and then by $\frac{4\pi^2}{T^2}$ to isolate $g$ (or simply take the reciprocal of both sides and multiply by $L$):**

$$g \cdot \frac{T^2}{4\pi^2} = L$$


$$g = \frac{4\pi^2 L}{T^2}$$



**Final Formula:**


$$g = \frac{4\pi^2 L}{T^2}$$
