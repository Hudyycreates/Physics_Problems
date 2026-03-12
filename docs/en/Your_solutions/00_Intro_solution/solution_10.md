# 10. Infinite Series: The Ant’s Path

**Problem:** An ant starts at $(0,0)$ and moves in a spiral: $1\text{ m}$ East, $1/2\text{ m}$ North, $1/3\text{ m}$ West, $1/4\text{ m}$ South, $1/5\text{ m}$ East, and so on. Determine the final resting position $(x, y)$.

---

### **Step 1: Decompose the Movement**

Because the movement occurs on an $xy$-plane, we can track the horizontal (East-West) and vertical (North-South) movements as two independent "tug-of-war" lines.

* **X-axis (East-West):** Moves are $1$ (East), $-1/3$ (West), $+1/5$ (East), $-1/7$ (West)...
* **Y-axis (North-South):** Moves are $1/2$ (North), $-1/4$ (South), $+1/6$ (North), $-1/8$ (South)...



---

### **Step 2: The "Shrinking Step" Logic**

When explaining this, the key is realizing the ant is **trapped** by its own momentum:

* **Shrinking Steps:** Since each step is shorter than the previous one, the total distance doesn't explode into infinity. 
* **The "Bounce":** Because it is an alternating series (forward/back), the ant doesn't just stop at zero. It overshoots, then undershoots, with each "bounce" getting smaller. 
* **Convergence:** Eventually, the "bounces" become so microscopic that the ant effectively locks into one specific spot—this is called **convergence**.



---

### **Step 3: Calculating the Limit**

We don't need to track the ant for an eternity because these patterns follow known mathematical "shortcuts" (Taylor Series).

* **X-Coordinate:** The series $1 - 1/3 + 1/5 - 1/7 \dots$ is the Taylor expansion for $\arctan(x)$ evaluated at $x = 1$, which equals $\frac{\pi}{4}$.
* **Y-Coordinate:** The series $1/2 - 1/4 + 1/6 - 1/8 \dots$ is equivalent to $\frac{1}{2}(1 - 1/2 + 1/3 - 1/4 \dots)$, which is the expansion for $\frac{1}{2} \ln(2)$.

---

### **Final Answer**

The ant's final position, after an infinite number of moves, is:

$$(x, y) = \left( \frac{\pi}{4}, \frac{\ln(2)}{2} \right)$$

---

### **Why this isn't a guess**

If you calculate the first few moves (e.g., $1 - 1/3 + 1/5 \dots$), you get a "snapshot" of where the ant is (like $0.8349$). 

The value $\frac{\pi}{4} \approx 0.785$ is the **limit**—the theoretical "finish line" where the ant settles after infinite steps. Your calculation is the runner mid-stride; the limit is where the runner finally stops.
