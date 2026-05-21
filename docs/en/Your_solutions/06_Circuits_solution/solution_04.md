# Mixed Circuit Resistance Calculation

## Problem Statement

Calculate the equivalent resistance ($R_{eq}$) for the circuit shown in the figure. All individual resistors in the circuit have an identical resistance of **$10\ \Omega$**.

---

## Step-by-Step Solution

To find the total equivalent resistance, we simplify the circuit from the inside out, breaking it down into clear sequential operations.

---

### Step 1: Simplify the Bottom-Right Parallel Pair

At the bottom right of the circuit, two resistors are connected in parallel because they share the same starting and ending nodes.

* **Resistors:** $R_4 = 10\ \Omega$, $R_5 = 10\ \Omega$

* **Formula (Product-over-Sum):**
  $$R_{\parallel} = \frac{R_4 \times R_5}{R_4 + R_5} = \frac{10 \times 10}{10 + 10} = \frac{100}{20} = 5\ \Omega$$

---

### Step 2: Simplify the Bottom Branch (Series)

The first resistor in the bottom branch is in series with the parallel pair we just solved. Because they are in a single continuous path, we simply add their values together.

* **Resistors:** $R_3 = 10\ \Omega$, $R_{\parallel} = 5\ \Omega$

* **Formula:**
  $$R_{\text{bottom}} = R_3 + R_{\parallel} = 10\ \Omega + 5\ \Omega = 15\ \Omega$$

---

### Step 3: Simplify the Top Branch (Series)

The top branch consists of two resistors connected back-to-back along a single path, meaning they are in series.

* **Resistors:** $R_1 = 10\ \Omega$, $R_2 = 10\ \Omega$

* **Formula:**
  $$R_{\text{top}} = R_1 + R_2 = 10\ \Omega + 10\ \Omega = 20\ \Omega$$

---

### Step 4: Combine the Top and Bottom Branches (Parallel)

The total top branch ($20\ \Omega$) and the total bottom branch ($15\ \Omega$) split from the same initial junction and rejoin before the final resistor. Because the current has two alternative paths, they are in parallel.

* **Formula (Reciprocal Method):**
  $$\frac{1}{R_{\text{combined}}} = \frac{1}{R_{\text{top}}} + \frac{1}{R_{\text{bottom}}} = \frac{1}{20} + \frac{1}{15} = \frac{7}{60}$$

* **Solving for $R_{\text{combined}}$:**
  $$R_{\text{combined}} = \frac{60}{7} \approx 8.57\ \Omega$$

---

### Step 5: Add the Final Series Resistor

Now that the entire parallel network is simplified into a single equivalent block ($8.57\ \Omega$), it sits strictly in series with the final $10\ \Omega$ resistor on the far right. There are no more splits in the circuit.

* **Resistors:** $R_{\text{combined}} = 8.57\ \Omega$, $R_{\text{final}} = 10\ \Omega$

* **Formula:**
  $$R_{eq} = R_{\text{combined}} + R_{\text{final}} = 8.57\ \Omega + 10\ \Omega = 18.57\ \Omega$$

---

## Final Answer

The total equivalent resistance of the circuit is **$18.57\ \Omega$** (or exactly **$\frac{130}{7}\ \Omega$**).
