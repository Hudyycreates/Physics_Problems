# Problem 4: Relative Uncertainty

**Question:** A car's speedometer has a 5% of uncertainty. If it reads 60 km/h, what is the range of the car's actual speed?

---

### Metrics
* **Measured Speed ($V$):** 60 km/h
* **Relative Uncertainty ($\%\Delta V$):** 5%
* **Absolute Uncertainty ($\Delta V$):** The error margin in km/h.

### Solution

**1. Calculate Absolute Uncertainty ($\Delta V$)**
Convert the percentage to a decimal and multiply by the measured speed to find the exact error margin.
$$\Delta V = V \times \left(\frac{\%\Delta V}{100}\right)$$
$$\Delta V = 60 \times 0.05$$
$$\Delta V = 3 \text{ km/h}$$

**2. Calculate the Range**
Apply the margin of error ($\pm 3 \text{ km/h}$) to the measured speed.
* **Minimum Speed:** $60 - 3 = 57 \text{ km/h}$
* **Maximum Speed:** $60 + 3 = 63 \text{ km/h}$

**Final Answer:**
The range of the actual speed is **57 km/h to 63 km/h** ($60 \pm 3 \text{ km/h}$).
