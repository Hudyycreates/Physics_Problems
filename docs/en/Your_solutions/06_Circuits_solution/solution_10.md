# Problem 10: Average Current

**Question:** A lightning bolt transfers a charge of 30 Coulombs to the ground in a time of 2 milliseconds. What is the average current of the lightning bolt?

---

### The Intuition
Think of a lightning bolt as a bucket of water tipping over. Even if the total amount of water (charge) isn't impossibly huge, the fact that it all dumps out in a fraction of a second means the *flow rate* (current) is incredibly violent. Average current just takes the total amount dumped and divides it by how long the event lasted.

### Metrics
* **Total Charge ($Q$):** The total electrical energy transferred, measured in Coulombs (C).
* **Time Interval ($\Delta t$):** How long the event takes, measured in seconds (s). 
* **Average Current ($I_{avg}$):** The average rate of charge flow over that time period, measured in Amperes (A).

### Solution

**1. Formula for Average Current**
$$I_{avg} = \frac{Q}{\Delta t}$$

**2. Convert Time to Standard Units**
Time must be in seconds, not milliseconds (ms). 
$$2 \text{ ms} = 0.002 \text{ s}$$

**3. Evaluate**
$$I_{avg} = \frac{30}{0.002}$$
$$I_{avg} = 15,000$$

**Final Answer:** The average current of the lightning bolt is **15,000 A** (Amperes).
