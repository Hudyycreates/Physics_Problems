# 4. Force Comparison

### Problem Statement

Calculate the magnitude of the electric force ($F_e$) and the gravitational force ($F_g$) between an electron and a proton in a hydrogen atom, where the average distance is $r \approx 5.3 \times 10^{-11}\text{ m}$. 

Finally, calculate the ratio $F_e/F_g$.

---

### Solution

#### 1. Identify the Given Constants

* **Distance ($r$):** $5.3 \times 10^{-11}\text{ m}$
* **Proton Charge ($q_p$):** $+1.602 \times 10^{-19}\text{ C}$
* **Electron Charge ($q_e$):** $-1.602 \times 10^{-19}\text{ C}$
* **Proton Mass ($m_p$):** $1.67 \times 10^{-27}\text{ kg}$
* **Electron Mass ($m_e$):** $9.11 \times 10^{-31}\text{ kg}$
* **Coulomb Constant ($k$):** $8.99 \times 10^9\text{ N}\cdot\text{m}^2/\text{C}^2$
* **Gravitational Constant ($G$):** $6.67 \times 10^{-11}\text{ N}\cdot\text{m}^2/\text{kg}^2$

---

#### 2. Calculate the Electric Force ($F_e$)

Using **Coulomb's Law**:
$$F_e = k \frac{|q_p \cdot q_e|}{r^2}$$

Substituting the values:
$$F_e = (8.99 \times 10^9) \frac{(1.602 \times 10^{-19})^2}{(5.3 \times 10^{-11})^2}$$

$$F_e = (8.99 \times 10^9) \frac{2.566 \times 10^{-38}}{2.809 \times 10^{-21}}$$

$$F_e \approx 8.21 \times 10^{-8}\text{ N}$$

---

#### 3. Calculate the Gravitational Force ($F_g$)

Using **Newton's Law of Universal Gravitation**:
$$F_g = G \frac{m_p \cdot m_e}{r^2}$$

Substituting the values:
$$F_g = (6.67 \times 10^{-11}) \frac{(1.67 \times 10^{-27}) \cdot (9.11 \times 10^{-31})}{(5.3 \times 10^{-11})^2}$$

$$F_g = (6.67 \times 10^{-11}) \frac{1.521 \times 10^{-57}}{2.809 \times 10^{-21}}$$

$$F_g \approx 3.61 \times 10^{-47}\text{ N}$$



---

#### 4. Calculate the Ratio ($F_e / F_g$)

To find the relative strength, we divide the electric force by the gravitational force. Note that the distance $r^2$ cancels out if you use the formulas directly, meaning this ratio is independent of the distance:

$$\text{Ratio} = \frac{F_e}{F_g} = \frac{k |q_p q_e|}{G m_p m_e}$$

$$\text{Ratio} = \frac{8.21 \times 10^{-8}}{3.61 \times 10^{-47}}$$

$$\text{Ratio} \approx 2.27 \times 10^{39}$$

---

### Final Result

* **Electric Force ($F_e$):** $\approx 8.21 \times 10^{-8}\text{ N}$
* **Gravitational Force ($F_g$):** $\approx 3.61 \times 10^{-47}\text{ N}$
* **Ratio ($F_e/F_g$):** **$\approx 2.27 \times 10^{39}$**

> **Conclusion:** The electric force is approximately **$10^{39}$ times stronger** than the gravitational force. This demonstrates why gravity is considered negligible when dealing with atomic-scale interactions.
