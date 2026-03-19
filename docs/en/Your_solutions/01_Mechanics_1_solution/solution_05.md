# Question 5: Relative Velocity

> **Problem:** A river flows east at $2\ \text{m/s}$. A boat that can travel at $5\ \text{m/s}$ in still water wants to go directly north across the river. In what direction (angle) should it head? How long will it take to cross the river if it is $200\ \text{m}$ wide?

---

## Background

When a boat moves through a flowing river, its actual velocity (called the **resultant velocity**) is the vector sum of two velocities:

1. The boat's velocity **relative to the water** (what the engine produces)
2. The river current's velocity **relative to the ground**

$$\vec{v}_{\text{resultant}} = \vec{v}_{\text{boat}} + \vec{v}_{\text{river}}$$

Since the boat wants to travel **directly north** despite an eastward current, it must aim at an angle **west of north** so the current's eastward push is exactly cancelled.

---

## Setting Up the Vector Diagram

Define the coordinate system:
- Positive $x$-axis: East
- Positive $y$-axis: North

**River current vector:**
$$\vec{v}_{\text{river}} = 2\hat{i} \quad \text{(eastward, 2 m/s)}$$

**Boat velocity vector** — the boat heads at angle $\theta$ west of north, so:
$$\vec{v}_{\text{boat}} = -5\sin\theta\,\hat{i} + 5\cos\theta\,\hat{j}$$

The minus sign on the $\hat{i}$ term reflects that the boat steers westward to counteract the current.

**Resultant velocity:**
$$\vec{v}_{\text{resultant}} = (2 - 5\sin\theta)\hat{i} + (5\cos\theta)\hat{j}$$

---

## Step 1 — Find the Required Heading Angle

For the boat to travel directly north, the eastward (x) component of the resultant must be zero:

$$2 - 5\sin\theta = 0$$

$$\sin\theta = \frac{2}{5}$$

$$\boxed{\theta = \arcsin\!\left(\frac{2}{5}\right) \approx 23.58°\ \text{west of north}}$$

---

## Step 2 — Find the Resultant Northward Speed

With $\sin\theta = \dfrac{2}{5}$, use the Pythagorean identity to find $\cos\theta$:

$$\cos\theta = \sqrt{1 - \sin^2\theta} = \sqrt{1 - \frac{4}{25}} = \sqrt{\frac{21}{25}} = \frac{\sqrt{21}}{5}$$

The northward component of the resultant velocity is:

$$v_N = 5\cos\theta = 5 \cdot \frac{\sqrt{21}}{5} = \sqrt{21} \approx 4.58\ \text{m/s}$$

So the full resultant velocity is:

$$\vec{v}_{\text{resultant}} = 0\,\hat{i} + \sqrt{21}\,\hat{j} \quad \text{(purely northward, as required)}$$

---

## Step 3 — Find the Time to Cross the River

The river is $200\ \text{m}$ wide (north–south distance). The boat covers this distance at the resultant northward speed $\sqrt{21}\ \text{m/s}$:

$$t = \frac{\text{distance}}{\text{speed}} = \frac{200}{\sqrt{21}} = \frac{200\sqrt{21}}{21}$$

$$\boxed{t = \frac{200}{\sqrt{21}} \approx 43.6\ \text{seconds}}$$

---

## Verification

Check that the resultant velocity is purely northward:

| Component | Calculation | Result |
|-----------|-------------|--------|
| East ($\hat{i}$) | $2 - 5\sin(23.58°) = 2 - 5(0.4)$ | $0\ \text{m/s}$ |
| North ($\hat{j}$) | $5\cos(23.58°) = 5 \cdot \dfrac{\sqrt{21}}{5}$ | $\sqrt{21} \approx 4.58\ \text{m/s}$ |

No eastward drift — the boat travels directly north as intended.

---

## Summary of Results

| Quantity | Value |
|----------|-------|
| River current speed | $2\ \text{m/s}$ east |
| Boat speed in still water | $5\ \text{m/s}$ |
| Required heading | $\arcsin\!\left(\dfrac{2}{5}\right) \approx 23.58°$ west of north |
| Resultant northward speed | $\sqrt{21} \approx 4.58\ \text{m/s}$ |
| River width | $200\ \text{m}$ |
| Time to cross | $\dfrac{200}{\sqrt{21}} = \dfrac{200\sqrt{21}}{21} \approx 43.6\ \text{s}$ |

---

## Interpretation

The boat cannot simply point north because the river would carry it eastward off course. By angling upstream (west of north) at $\approx 23.58°$, the westward component of the boat's thrust exactly cancels the eastward river current, producing a net velocity that points straight north. The stronger the current relative to the boat's speed, the more sharply it must angle into the current.

The speed is reduced from the boat's maximum of $5\ \text{m/s}$ down to $\sqrt{21} \approx 4.58\ \text{m/s}$ — some of the engine's output is spent fighting the current rather than crossing the river.

---

*Solved using vector decomposition and the principle of relative velocity.*
