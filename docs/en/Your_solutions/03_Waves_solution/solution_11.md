### Question 11: Animation: Two-Slit Interference

**Write an animation simulating Young's experiment, in which two slits act as point sources of coherent waves. The displacement of the resultant wave is the sum of partial waves described by the formula:**
$$u(\vec{r},t) = \frac{A}{|\vec{r} - \vec{r}_1|} \sin(k|\vec{r} - \vec{r}_1| - \omega t) + \frac{A}{|\vec{r} - \vec{r}_2|} \sin(k|\vec{r} - \vec{r}_2| - \omega t)$$
*where $\vec{r}_1$ and $\vec{r}_2$ are the position vectors of the slits. The user should be able to change the distance between the slits $d = |\vec{r}_1 - \vec{r}_2|$ and the wavelength $\lambda$.*

---

### 1. Intuitive Context: The Most Famous Experiment in Physics

If you want to prove something is a wave and not just a stream of particles, you use **Young's Double-Slit Experiment**. 

Imagine shining a flashlight at a wall with two vertical slits cut into it. If light were purely made of bullet-like particles, you would expect to see exactly two bright lines on the screen behind the slits. But that's not what happens. Instead, the light coming out of the two slits behaves like two overlapping water ripples, creating a complex barcode-like pattern of multiple bright and dark bands on the screen. 

The equation provided is exactly what we explored in the previous question (Superposition), but locked strictly to **two sources** that are perfectly "coherent" (meaning they are pulsing at the exact same frequency and time, like identical twins jumping in a pool).

---

### 2. The Physics of the Math: Path Length Difference

The entire magic of this animation comes down to one simple geometric concept: **Path Length Difference ($\Delta r$)**. 

Pick any random spot on the screen ($\vec{r}$). 
* The distance from Slit 1 to that spot is $|\vec{r} - \vec{r}_1|$.
* The distance from Slit 2 to that spot is $|\vec{r} - \vec{r}_2|$.

Because the two slits are in different locations, the waves have to travel different distances to reach that specific spot.
* **Constructive Interference (Bright Spots):** If the difference in distance is exactly 1 full wavelength ($\lambda$), 2 wavelengths, 3 wavelengths, etc., the wave peaks perfectly line up. They add together to create a massive peak.
* **Destructive Interference (Dark Spots / Nodal Lines):** If the difference is 0.5 wavelengths, 1.5 wavelengths, etc., the peak of wave 1 arrives at the exact same time as the valley of wave 2. They perfectly cancel out, leaving a dark spot where nothing moves.

---

### 3. Presentation Guide (Explaining the Sliders)

When showing this to your professor, use the sliders to demonstrate that you understand how the geometry dictates the physics. 

**Point out the Central Maximum (Before touching sliders):**
Draw attention to the exact middle line between the two slits. Explain that this line is *always* an antinode (maximum brightness) because the distance from Slit 1 and Slit 2 is exactly equal ($\Delta r = 0$). The waves always arrive in perfect sync here.

**Demonstration 1: Adjust the Wavelength ($\lambda$) Slider**
* **Action:** Increase the wavelength.
* **What happens:** The interference pattern spreads out and gets wider.
* **The Physics:** By making the waves physically longer, it takes more physical distance across the screen to achieve that "0.5 wavelength" offset required to create a dark spot. (You can note that this is why red light, which has a longer $\lambda$, creates wider interference fringes than blue light!)

**Demonstration 2: Adjust the Slit Distance ($d$) Slider**
* **Action:** Move the slits further apart (Increase $d$).
* **What happens:** The interference pattern tightens up; the "beams" pack closer together.
* **The Physics:** When the slits are further apart, the geometric angle between them from the perspective of the screen is wider. Because of this wider baseline, you don't have to move as far along the screen to drastically change the path length difference. Therefore, the cycle of constructive and destructive interference happens much more rapidly across the space.
