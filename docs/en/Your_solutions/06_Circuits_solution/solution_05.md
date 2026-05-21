# Kirchhoff's Laws: Two-Loop Circuit Solution

## Problem Statement
Using Kirchhoff's laws, find the currents **I1**, **I2**, and **I3** going through the resistors **R1**, **R2**, and **R3** respectively in the given two-loop circuit:

* **Left loop:** Source **E1 = 4.5 V** with internal resistance **rw1 = 1 Ω**, top resistor **R1 = 20 Ω**.
* **Right loop:** Source **E2 = 9 V** with internal resistance **rw2 = 1 Ω**.
* **Shared branch:** Resistor **R2 = 10 Ω** connecting the top junction to the bottom node.

---

## Step-by-Step Analytical Solution

Instead of solving complex simultaneous loop equations, we use the **Node Voltage Method** for a cleaner, more precise proof.

### Step 1: Establish the Reference Ground (0 V)
* We define the entire **bottom wire** as our reference node (**Ground = 0 V**).
* We define the unknown voltage at the **top junction** as **VA**.
* Internal resistances (**rw**) are treated as standard resistors connected in series within their respective branches.

---

### Step 2: Define Branch Currents via Ohm's Law
We express the current leaving node **VA** through each of the three branches using the Ohm's Law formula: `I = V / R`

1. **Left Branch Current (I1):** Total resistance is `R1 + rw1 = 20 + 1 = 21 Ω`.
   * `I1 = (VA - 4.5) / 21`

2. **Middle Branch Current (I2):** Total resistance is `R2 = 10 Ω`.
   * `I2 = VA / 10`

3. **Right Branch Current (I3):** Total resistance is `rw2 = 1 Ω`.
   * `I3 = (VA - 9) / 1`

---

### Step 3: Apply Kirchhoff's Current Law (KCL)
According to KCL, the algebraic sum of all currents leaving the top junction must equal zero:

`I1 + I2 + I3 = 0`

Substitute our Ohm's Law expressions into the KCL equation:
`((VA - 4.5) / 21) + (VA / 10) + ((VA - 9) / 1) = 0`

To eliminate the fractions, multiply the entire equation by the common denominator (**210**):
`10(VA - 4.5) + 21(VA) + 210(VA - 9) = 0`

`10VA - 45 + 21VA + 210VA - 1890 = 0`

Combine like terms:
`241VA - 1935 = 0`

`241VA = 1935`  
`VA = 1935 / 241`  
**VA ≈ 8.03 V**

---

### Step 4: Calculate Final Currents
Now, substitute the junction voltage **VA = 8.03 V** back into each individual branch equation:

* **Middle Branch (I2):**
  * `I2 = 8.03 / 10`  
  * **I2 = 0.803 A** (Flowing Downward)

* **Left Branch (I1):**
  * `I1 = (8.03 - 4.5) / 21 = 3.53 / 21`  
  * **I1 = 0.167 A** (Flowing Leftward)

* **Right Branch (I3):**
  * `I3 = (8.03 - 9) / 1`  
  * **I3 = -0.970 A** *(The negative sign denotes that current actually flows **Upward/Into** the node at 0.970 A, driven by the dominant 9 V source).*

---

## Final Verification
* **Currents Entering Junction = Currents Leaving Junction**
* `0.970 A = 0.167 A + 0.803 A`
* `0.970 A = 0.970 A` **[Verified]**
