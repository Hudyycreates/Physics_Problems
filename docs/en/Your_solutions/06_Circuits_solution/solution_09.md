# Problem 9: Current

**Question:** Charge flowing through the wire is given by $Q(t) = 5t^2 + 5$. What is the current at $t = 3$ s?

---

### The Intuition: What's Actually Happening?

Think of **Charge ($Q$)** like water filling up a bucket, and **Current ($I$)** like the speed of the water blasting out of the hose. 

* **The Function:** The equation $Q(t) = 5t^2 + 5$ tells us the total amount of "water" (charge) that has passed through the wire. Because there is a $t^2$ in there, the charge isn't just flowing at a steady drip—it’s actively speeding up as time goes on.
* **The Derivative:** When we take the derivative, we are asking: *"Exactly how fast is that water flowing right at this specific split second?"* Taking the derivative of charge gives us that exact flow rate, which we call Current. 

---

### Solution

**1. Formula for Current**
Current is the rate of change of charge over time:
$$I(t) = \frac{dQ(t)}{dt}$$

**2. Differentiate Charge Function**
We take our charge function and find its derivative:
$$Q(t) = 5t^2 + 5$$
$$I(t) = \frac{d}{dt}(5t^2 + 5)$$
$$I(t) = 10t$$
*(This means the flow rate increases by 10 Amperes every second).*

**3. Evaluate at $t = 3$ s**
To find the exact flow rate at the 3-second mark, plug in $3$:
$$I(3) = 10(3)$$
$$I(3) = 30$$

<br>

### Final Answer
At exactly 3 seconds, the current is flowing at **30 A** (Amperes).
