# 7: The Fly and the Bicycle

**Problem:** A bicycle is $10\text{ m}$ from a wall and moves toward it at a constant speed of $1\text{ m/s}$. A fly starts from the bicycle's front wheel and flies toward the wall at $2\text{ m/s}$. Each time the fly reaches the wall, it instantly turns around and flies back to the bicycle. It keeps flying back and forth until the bicycle reaches the wall.

**Intuition:** This problem is a classic "math trap." It is tempting to try to calculate every single trip the fly takes back and forth, which would result in an infinite series of smaller and smaller distances. However, the "logical shortcut" is to realize the fly is constrained by the same clock as the bicycle. If we know how long the bicycle takes to reach the wall, we know exactly how long the fly has been in the air.



---

### **Step 1 — Identify What Ends the Motion**

The motion ends the moment the bicycle reaches the wall. Because the fly is moving continuously until this moment, both the bicycle and the fly share the **exact same time interval** for their respective travels.

---

### **Step 2 — Find How Long the Bicycle Takes**

To find the total duration of the trip, we use the bicycle's data:

* **Initial Distance ($d$):** $10\text{ m}$
* **Speed ($v$):** $1\text{ m/s}$

Using the basic motion formula $d = v \cdot t$, we solve for time ($t$):

$$t = \frac{d}{v}$$

$$t = \frac{10\text{ m}}{1\text{ m/s}} = 10\text{ seconds}$$

The bicycle reaches the wall in **$10\text{ seconds}$**.

---

### **Step 3 — Apply the Same Time to the Fly**

Since the fly is in constant motion for the entire $10$ seconds that the bicycle is moving, we can now calculate the fly's total distance regardless of how many turns it makes.

* **Fly's Speed ($v_{fly}$):** $2\text{ m/s}$
* **Total Time ($t$):** $10\text{ s}$

Using the distance formula:

$$d_{fly} = v_{fly} \cdot t$$

$$d_{fly} = 2\text{ m/s} \times 10\text{ s} = 20\text{ meters}$$

---

### **Final Answer**

The fly travels a total distance of **$20\text{ meters}$** before the motion ends.

---

### **Key Concept**


* **The "Time-Constraint" Insight:** By focusing on the total time—a shared variable—we bypass the need to sum an infinite series. This is a common strategy in physics problems where internal movements are complex but the total duration is dictated by a simpler, underlying process.
