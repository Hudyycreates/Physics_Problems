### Question 8: Waves

**Which of the following functions can describe a traveling wave?** *Hint: check if it satisfies the wave equation:*
$$\frac{\partial^2 y}{\partial x^2} = \frac{1}{v^2}\frac{\partial^2 y}{\partial t^2}$$

a) $y(x,t) = A\cos(kx^2 - \omega t)$
b) $y(x,t) = A(x - vt)^2$
c) $y(x,t) = A\log(x + vt)$

---

### The Plain English Concept (No Advanced Math Yet)

Before we touch the scary equation, let's understand how a "traveling wave" works.

Imagine a perfect wave rolling across a pond. The wave moves forward, but its *shape* never changes. In physics, for a math formula to perfectly describe this, the position ($x$) and the time ($t$) must be locked together in a very specific package inside the formula. 

They almost always have to look exactly like this:
**$(x - vt)$** or  **$(x + vt)$**

Notice that neither the $x$ nor the $t$ has an exponent of 2 attached directly to it *inside* the package. They are partners.

**What is the hint asking us to do?**
That big equation with the $\partial$ symbols is a "testing machine." 
Think of it like a balance scale:
* The **left side** tests the formula by looking *only* at the $x$.
* The **right side** tests the formula by looking *only* at the $t$.
* If you run the formula through both sides and they equal each other perfectly, you have a traveling wave!

**What does $\partial^2$ mean?**
It means "take the derivative twice." If you don't know calculus, just think of a derivative as a math operation that extracts what is attached to a variable. If you do it twice, you extract it twice.

---

### Testing The Options (Step-by-Step)

Let's run each option through the testing machine.

<br>

#### **Testing Option (a):** $y = A\cos(kx^2 - \omega t)$

We can fail this one just by looking at it, without doing any hard math!

* Look at the package inside: **$(kx^2 - \omega t)$**
* Notice that the $x$ is squared ($x^2$), but the time ($t$) is just a regular $t$. 
* Because they are not balanced inside the package, they will fail the balance scale. When you run them through the testing machine, the $x$ side will generate different shapes than the $t$ side.
* **Result: FAIL.**

<br><br>

#### **Testing Option (b):** $y = A(x - vt)^2$

This formula has the perfect $(x - vt)$ package. The square is on the *outside*, which is totally fine. Let's run it through the machine.

**1. Test the left side (look only at $x$):**
When we run this through the calculus machine for $x$ twice, it strips away the variables and just leaves the constant numbers in front. 
* The result for the left side is simply: **$2A$**

**2. Test the right side (look only at $t$):**
When we run it through for $t$, the machine extracts whatever is attached to $t$. Here, a **$-v$** is attached to $t$. Because we run it twice ($\partial^2$), the $-v$ comes out twice. $(-v \times -v = v^2)$. 
* The result for the $t$ side is: **$2A \times v^2$**

**3. Put them on the balance scale:**
Now we plug our results back into the original testing equation from the hint:
*(Left Side)* = $\frac{1}{v^2} \times$ *(Right Side)*

**$2A$** = $\frac{1}{v^2} \times$ **($2A \times v^2$)**

Look at the right side of the equals sign. We are dividing by $v^2$ and multiplying by $v^2$. They completely cancel each other out!

**$2A = 2A$**

* Both sides match perfectly!
* **Result: PASS.**

<br><br>

#### **Testing Option (c):** $y = A\log(x + vt)$

This formula also has a perfect $(x + vt)$ package! Let's run it through the machine. Because it's a logarithm, the calculus output looks a little messy, but watch what happens.

**1. Test the left side (look only at $x$):**
The calculus machine turns the logarithm into a fraction. Doing it twice gives us this result:
* **$\frac{-A}{(x + vt)^2}$**

**2. Test the right side (look only at $t$):**
Just like in option (b), whatever is attached to $t$ gets extracted twice. Here, a positive **$v$** is attached to $t$. It comes out twice ($v \times v = v^2$). We get the exact same messy fraction, but multiplied by $v^2$:
* **$\frac{-A \times v^2}{(x + vt)^2}$**

**3. Put them on the balance scale:**
*(Left Side)* = $\frac{1}{v^2} \times$ *(Right Side)*

**$\frac{-A}{(x + vt)^2}$** = $\frac{1}{v^2} \times$ **$\frac{-A \times v^2}{(x + vt)^2}$**

Once again, look at the right side. The $v^2$ on the bottom cancels out the $v^2$ on the top! You are left with the exact same fraction on both sides.

**$\frac{-A}{(x + vt)^2}$** = **$\frac{-A}{(x + vt)^2}$**

* Both sides match perfectly!
* **Result: PASS.**

---

### Final Result

**Both (b) and (c) describe a traveling wave.** *(They both perfectly satisfy the wave equation).*
