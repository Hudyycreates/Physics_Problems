### Question 10: Animation: Wave Sources

**Write an animation in which it is possible to place dots that will serve as sources of waves described by the equation:**
$$u(\vec{r},t) = \frac{A}{|\vec{r} - \vec{r}_0|^\alpha} \sin(k|\vec{r} - \vec{r}_0| - \omega t)$$
*where $\vec{r}_0$ is the position of the dot, and $\alpha$ is a parameter that can be set within the range $[0,2]$. The animation should show the superposition of waves from all dots.*

---

### 1. Intuitive Context: Dropping Pebbles in a Pond

If Question 8 was about a wave traveling on a single 1D string, this question is about throwing multiple pebbles into a 2D pond or placing multiple speakers in a 3D room. 

When a pebble hits a pond (at position $\vec{r}_0$), a circular ripple expands outward. The equation provided is the exact mathematical anatomy of that expanding ripple, with a built-in "dimmer switch" ($\alpha$) that dictates how fast the wave fades away as it travels outward.

When multiple pebbles are thrown at once, their ripples crash into each other. They don't bounce off one another; they simply add together. This adding together is called **superposition**, and it creates beautiful, complex patterns of "constructive" (amplified) and "destructive" (canceled) interference.

---

### 2. Deconstructing the Math

Let's break down the equation into two easy-to-understand chunks. 

To make it easier to read, let's define the distance from the wave source to our observation point as **$d$**. 
Mathematically, $d = |\vec{r} - \vec{r}_0|$.

Now the equation looks like this:
$$u(\vec{r},t) = \left( \frac{A}{d^\alpha} \right) \cdot \sin(kd - \omega t)$$

#### Chunk 1: The Traveling Wave $\sin(kd - \omega t)$
This is the "engine" of the wave. It guarantees that the shape oscillates up and down over time ($\omega t$) and moves outward through space ($kd$). Because $d$ represents a radius pointing outward from the source, this guarantees the wave is circular (or spherical), spreading outward in all directions equally.

#### Chunk 2: The Attenuation Factor $\left( \frac{A}{d^\alpha} \right)$
As a wave expands, it has to stretch its initial energy over a larger and larger area. Therefore, the amplitude (the height of the wave) must shrink the further away you get. $A$ is the starting amplitude, $d$ is the distance, and the exponent **$\alpha$** decides the *rules of the space* the wave is traveling through.

---

### 3. The Magic of Parameter $\alpha$ (The Physics of Space)

This is the most critical physics concept to highlight to your professor. The parameter $\alpha$ isn't just an arbitrary dial; it literally changes the geometry of the universe the wave exists in!

* **When $\alpha = 0$ (No fading):** * The attenuation factor becomes $1$. The amplitude never shrinks. 
    * **Physics meaning:** This physically represents an idealized 1D wave (like a perfect laser beam or a frictionless string) where the energy doesn't have space to spread out laterally, so it maintains its height forever.
* **When $\alpha = 0.5$ (The 2D Pond):**
    * The amplitude falls off by the square root of the distance ($1/\sqrt{d}$). 
    * **Physics meaning:** *Energy* is proportional to amplitude squared. So if amplitude drops by $1/\sqrt{d}$, the *energy* drops by exactly $1/d$. This perfectly perfectly models a 2D ripple on a pond! As the circle expands, its circumference grows proportionally to $d$, so the energy is perfectly conserved but stretched over that growing boundary.
* **When $\alpha = 1.0$ (The 3D Room):**
    * The amplitude falls off by $1/d$.
    * **Physics meaning:** Energy drops by $1/d^2$. This is the famous **Inverse Square Law**. This perfectly models a 3D spherical wave, like a lightbulb shining in a room or a star in space. The energy is conserved but stretched over the surface area of a sphere, which grows at $r^2$.
* **When $\alpha > 1.0$ (Absorptive/Damped Medium):**
    * **Physics meaning:** The wave loses energy faster than geometry alone dictates. This represents a wave traveling through a "lossy" medium (like sound trying to travel through thick foam, or light traveling through dense fog). The medium itself is absorbing the energy and turning it into heat.

---

### 4. Superposition: How the Waves Combine

The principle of superposition states that the total displacement of the medium at any given point is simply the algebraic sum of the displacements caused by each individual wave.

If you have three dots (sources), the math is simply:
$$u_{total} = u_{dot1} + u_{dot2} + u_{dot3}$$

* **Constructive Interference:** When the peaks of two separate waves happen to arrive at the same spot at the exact same time, they add together to create a massive peak.
* **Destructive Interference:** When the peak of one wave arrives at the exact same time as the trough (valley) of another wave, they equal exactly zero. The water (or medium) goes perfectly flat in that specific spot. 

---

### 5. Presentation Guide 

If you are demonstrating this visually, here are the key phenomena to point out:

1.  **Place just ONE dot and slide $\alpha$:** * Show how at $\alpha = 0$, the screen fills with high-contrast stripes (constant energy). 
    * Slide it to $\alpha = 1$ and point out how the wave quickly becomes "ghostly" and fades to gray (equilibrium) at the edges of the screen due to the Inverse Square Law.
2.  **Place TWO dots close together:**
    * Point out the distinct lines of completely flat gray radiating outward. Explain that these are **"nodal lines"**—areas of permanent destructive interference where the waves from the two sources perfectly cancel each other out continuously.
3.  **Place a line of dots close together (Phased Array):**
    * If you place several dots in a straight, tight line, point out how the individual circular ripples merge together to form one giant, flat "wall" of a wave (a plane wave) moving perpendicular to the line. Explain that this is **Huygens' Principle** in action!
