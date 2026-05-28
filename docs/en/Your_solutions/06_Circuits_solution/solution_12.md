# Problem 12: Transformer Currents

**Question:** A transformer has a primary coil with 1000 turns and a secondary coil with 200 turns. If the primary voltage is 120 V (AC), what is the secondary voltage? If the current in the secondary is 3 A, what is the current in the primary?

---

### The Intuition
A transformer is like a gearbox on a bicycle. You can trade speed for pedaling force, but you can't magically create more total pedaling power. In electrical terms, you can step down the **Voltage** (like shifting to an easier gear), but doing so allows you to step up the **Current**. The total Power on both sides remains roughly equal. 

### Metrics
* **Turns ($N_p, N_s$):** The number of wire loops on the primary (input) and secondary (output) sides.
* **Voltage ($V_p, V_s$):** The electrical pressure on the primary and secondary sides, measured in Volts (V).
* **Current ($I_p, I_s$):** The flow rate on the primary and secondary sides, measured in Amperes (A).

### Solution

**1. Find Secondary Voltage**
The ratio of voltages is strictly equal to the ratio of turns:
$$\frac{V_s}{V_p} = \frac{N_s}{N_p}$$

Rearrange to solve for $V_s$:
$$V_s = V_p \times \left(\frac{N_s}{N_p}\right)$$
$$V_s = 120 \times \left(\frac{200}{1000}\right)$$
$$V_s = 120 \times 0.2$$
$$V_s = 24 \text{ V}$$

**2. Find Primary Current**
Assuming an ideal transformer, the power in equals the power out ($P_p = P_s$). Since $P = V \times I$, we can write:
$$V_p \times I_p = V_s \times I_s$$

Plug in the known values:
$$120 \times I_p = 24 \times 3$$
$$120 \times I_p = 72$$
$$I_p = \frac{72}{120}$$
$$I_p = 0.6 \text{ A}$$

**Final Answers:**
* The secondary voltage is **24 V**.
* The primary current is **0.6 A**.
