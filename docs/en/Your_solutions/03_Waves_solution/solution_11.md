### Question 11: Animation: Two-Slit Interference

**Write an animation simulating Young's experiment, in which two slits act as point sources of coherent waves. The displacement of the resultant wave is the sum of partial waves described by the formula:**

$$
u(\vec{r},t) = \frac{A}{|\vec{r} - \vec{r}_1|} \sin(k|\vec{r} - \vec{r}_1| - \omega t) + \frac{A}{|\vec{r} - \vec{r}_2|} \sin(k|\vec{r} - \vec{r}_2| - \omega t)
$$

*where 
r
1
→
 and 
r
2
→
 are the position vectors of the slits. The user should be able to change the distance between the slits 
d
=
|
r
1
→
−
r
2
→
|
 and the wavelength 
λ
. The animation should visualize the resulting interference pattern in real time.*

---

### 1. Intuitive Context: The Double-Slit Experiment

If you want to prove something is a wave and not just a stream of particles, you use **Young's Double-Slit Experiment**. 

Imagine shining a flashlight at a wall with two vertical slits cut into it. If light were purely made of bullet-like particles, you would expect to see exactly two bright lines on the screen behind the slits. But that's not what happens. Instead, the light coming out of the two slits behaves like two overlapping water ripples, creating a complex barcode-like pattern of multiple bright and dark bands on the screen. 

The equation provided is the mathematical representation of **superposition**, locked strictly to two sources that are perfectly "coherent" (meaning they are pulsing at the exact same frequency and time, maintaining a constant phase difference).

---

### 2. The Physics of the Math: Path Length Difference

The core of this phenomenon comes down to one simple geometric concept: **Path Length Difference ($\Delta r$)**. 

Pick any random spot on the screen ($\vec{r}$). 
* The distance from Slit 1 to that spot is $|\vec{r} - \vec{r}_1|$.
* The distance from Slit 2 to that spot is $|\vec{r} - \vec{r}_2|$.

Because the two slits are in different locations, the waves have to travel different distances to reach that specific spot on the screen.

* **Constructive Interference (Bright Spots):** If the difference in distance is exactly 1 full wavelength ($\lambda$), 2 wavelengths, 3 wavelengths, etc., the wave peaks perfectly line up. They add together to create a massive peak.
* **Destructive Interference (Dark Spots / Nodal Lines):** If the difference is 0.5 wavelengths, 1.5 wavelengths, etc., the peak of wave 1 arrives at the exact same time as the valley of wave 2. They perfectly cancel out, leaving a dark spot where nothing moves.

---

### 3. Parameter Effects (Wavelength and Slit Distance)

The visual interference pattern changes drastically depending on the geometric parameters of the system.

* **The Central Maximum:**
The exact middle line between the two slits is *always* an antinode (maximum brightness). This is because the distance from Slit 1 and Slit 2 to the center of the screen is exactly equal ($\Delta r = 0$). The waves will always arrive in perfect sync at this location.

* **Increasing the Wavelength ($\lambda$):**
Increasing the wavelength causes the interference pattern to spread out and get wider. By making the waves physically longer, it takes more physical distance across the screen to achieve that "0.5 wavelength" offset required to create a dark spot. This is mathematically why red light (which has a longer $\lambda$) creates wider interference fringes than blue light.

* **Increasing the Slit Distance ($d$):**
Moving the slits further apart causes the interference pattern to tighten up, packing the fringes much closer together. When the slits are further apart, the geometric baseline is wider. Because of this, you only have to move a tiny distance along the screen to drastically change the path length difference. Therefore, the cycle of constructive and destructive interference happens much more rapidly across the space.
