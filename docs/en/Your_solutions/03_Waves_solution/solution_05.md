## Problem 5: Echo Ranging

###  Conceptual Introduction

When a sound is produced near a reflective surface (a cliff, a wall, a
mountain), the sound wave travels **outward**, reflects off the surface,
and returns to the source. The total time measured is for the **round trip**
— the sound covers the distance to the cliff **twice**.

This is the principle behind sonar, radar, and ultrasound imaging:
by measuring the time delay of a reflected signal and knowing the wave
speed, we can calculate distance.

$$d = \frac{v \cdot t_{total}}{2}$$

The division by 2 is essential — we are measuring the one-way distance to
the cliff, not the total round-trip distance.

---

###  Given Information

| Symbol | Meaning | Value |
|--------|---------|-------|
| $t_{total}$ | Total time until echo is heard | $1\ \text{s}$ |
| $v$ | Speed of sound in air | $343\ \text{m/s}$ |

---

### 🔺 Step 1 — Calculate Total Distance Traveled by the Sound

The sound travels at $343\ \text{m/s}$ for a total of $1$ second:

$$d_{total} = v \times t_{total} = 343\ \text{m/s} \times 1\ \text{s} = 343\ \text{m}$$

---

### 🔺 Step 2 — Find the One-Way Distance to the Cliff

This total distance is the **round trip** (to the cliff and back), so
the actual distance to the cliff is half of that:

$$d_{cliff} = \frac{d_{total}}{2} = \frac{343}{2}$$

$$\boxed{d_{cliff} = 171.5\ \text{m}}$$

---

### 🔍 Sanity Check

If the cliff is $171.5\ \text{m}$ away and sound travels at $343\ \text{m/s}$,
the time for the sound to reach the cliff is:

$$t_{one-way} = \frac{d_{cliff}}{v} = \frac{171.5}{343} = 0.5\ \text{s}$$

Round trip: $2 \times 0.5\ \text{s} = 1\ \text{s}$ ✅

---

###  Common Mistakes

- ❌ **Not dividing by 2** — the most common error. The measured time is for
  the full round trip; the cliff is only halfway along that path.
- ❌ **Forgetting to check units** — speed in m/s, time in seconds, gives
  distance in metres. Stay consistent.

---

###  Real-World Extension — Sonar and Echolocation

Dolphins and bats use this exact principle (echolocation) to detect objects.
Sonar on submarines uses the same method underwater, where $v_{water} \approx 1482\ \text{m/s}$.
If the same echo were heard after $1$ second underwater:

$$d = \frac{1482 \times 1}{2} = 741\ \text{m}$$

The same time delay corresponds to a much greater distance — this is why
sonar works over long ranges in the ocean.
