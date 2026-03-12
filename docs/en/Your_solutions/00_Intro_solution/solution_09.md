# 9. Maximum Area Rectangle

To find the dimensions of the rectangle with the maximum area under the curve $y = 3 - x^2$ in the first quadrant, we follow these steps:

### 1. Define the Variables
In the first quadrant, a rectangle anchored at the origin $(0,0)$ with a vertex on the curve $(x, y)$ has:
* **Width:** $x$
* **Height:** $y = 3 - x^2$



### 2. Formulate the Area Function
The Area $A$ of the rectangle is the product of its width and height:

$$A(x) = x \cdot y = x(3 - x^2)$$
$$A(x) = 3x - x^3$$


### 3. Find the Critical Points
To maximize the area, we take the derivative of $A(x)$ with respect to $x$ and set it to zero:

$$A'(x) = \frac{d}{dx}(3x - x^3) = 3 - 3x^2$$

Set $A'(x) = 0$:

$$3 - 3x^2 = 0$$
$$3x^2 = 3$$
$$x^2 = 1$$
$$x = 1 \quad (\text{since } x \text{ must be positive})$$


### 4. Verify the Maximum
We use the second derivative test to ensure this critical point is a maximum:

$$A''(x) = -6x$$

At $x = 1$:

$$A''(1) = -6(1) = -6$$

Since $A''(1) < 0$, the function is concave down at this point, confirming a local maximum.



### 5. Determine the Dimensions
Now, we find the corresponding height $y$ and the maximum area:

* **Width ($x$):** $1$
* **Height ($y$):** $y = 3 - (1)^2 = 2$
* **Maximum Area:** $A = 1 \times 2 = 2$

### Final Answer
The dimensions of the rectangle with the maximum area are:
* **Width:** $1$
* **Height:** $2$

