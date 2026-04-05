# Section 3 — Problem 8: Which Functions Describe a Traveling Wave?

##  Conceptual Introduction

A function $y(x,t)$ is a valid traveling wave **if and only if** it satisfies
the **wave equation**:

$$\frac{\partial^2 y}{\partial x^2} = \frac{1}{v^2}\frac{\partial^2 y}{\partial t^2}$$

The method is always the same:

1. Compute the **LHS**: differentiate $y$ twice with respect to $x$
2. Compute the **RHS**: differentiate $y$ twice with respect to $t$, divide by $v^2$
3. **Compare**: if LHS $=$ RHS for all $x$ and $t$ — valid wave. If not — invalid.

There is also a powerful shortcut worth knowing before we begin:

> **D'Alembert's Principle:** Any function of the form $f(x \pm vt)$
> automatically satisfies the wave equation, provided $f$ is twice
> differentiable. This is because the chain rule gives identical second
> derivatives on both sides. A function that **cannot** be written purely
> as $f(x \pm vt)$ will generally fail.

We will verify each case by direct calculation.

---

## Part a) — $y(x,t) = A\cos(kx^2 - \omega t)$

### Is it of the form $f(x \pm vt)$?

The argument is $kx^2 - \omega t$. This is **not** linear in $x$ — the $x^2$
term prevents it from being written as $f(x - vt)$. We already expect failure,
but let us prove it rigorously.

### Computing LHS: $\partial^2 y / \partial x^2$

**First derivative** — chain rule, since the argument is $u = kx^2 - \omega t$:

$$\frac{\partial y}{\partial x} = -A\sin(kx^2 - \omega t) \cdot \frac{\partial}{\partial x}(kx^2) = -2Akx\sin(kx^2 - \omega t)$$

**Second derivative** — product rule on $2Akx \cdot \sin(kx^2 - \omega t)$:

$$\frac{\partial^2 y}{\partial x^2} = -2Ak\sin(kx^2 - \omega t) - 2Akx \cdot \cos(kx^2 - \omega t) \cdot 2kx$$

$$\text{LHS} = -2Ak\sin(kx^2 - \omega t) - 4Ak^2x^2\cos(kx^2 - \omega t)$$

### Computing RHS: $\frac{1}{v^2}\partial^2 y / \partial t^2$

**First derivative** with respect to $t$:

$$\frac{\partial y}{\partial t} = -A\sin(kx^2 - \omega t) \cdot (-\omega) = A\omega\sin(kx^2 - \omega t)$$

**Second derivative** with respect to $t$:

$$\frac{\partial^2 y}{\partial t^2} = A\omega\cos(kx^2 - \omega t)\cdot(-\omega) = -A\omega^2\cos(kx^2 - \omega t)$$

$$\text{RHS} = \frac{1}{v^2}\cdot\left(-A\omega^2\cos(kx^2 - \omega t)\right) = -\frac{A\omega^2}{v^2}\cos(kx^2 - \omega t)$$

### Comparison

$$\text{LHS} = \underbrace{-2Ak\sin(kx^2-\omega t)}_{\text{sine term}} - \underbrace{4Ak^2x^2\cos(kx^2 - \omega t)}_{x^2\text{-dependent cosine term}}$$

$$\text{RHS} = -\frac{A\omega^2}{v^2}\cos(kx^2-\omega t)$$

The LHS has a **sine term** and an **$x^2$-dependent cosine** that the RHS
does not. These cannot be equal for all values of $x$ and $t$.

> ❌ **$y = A\cos(kx^2 - \omega t)$ does NOT satisfy the wave equation.**
> The argument $kx^2$ is not linear in $x$. Squaring $x$ breaks the
> structure that makes $f(x \pm vt)$ work.

---

## Part b) — $y(x,t) = A(x - vt)^2$

### Is it of the form $f(x \pm vt)$?

Yes — this is $f(u) = Au^2$ where $u = x - vt$. By D'Alembert's principle
we expect it to work. Let us verify.

### Computing LHS: $\partial^2 y / \partial x^2$

**First derivative** with respect to $x$:

$$\frac{\partial y}{\partial x} = A \cdot 2(x - vt) \cdot 1 = 2A(x - vt)$$

**Second derivative** with respect to $x$:

$$\frac{\partial^2 y}{\partial x^2} = 2A$$

### Computing RHS: $\frac{1}{v^2}\partial^2 y / \partial t^2$

**First derivative** with respect to $t$
(chain rule: $\partial(x-vt)/\partial t = -v$):

$$\frac{\partial y}{\partial t} = A \cdot 2(x - vt) \cdot (-v) = -2Av(x - vt)$$

**Second derivative** with respect to $t$:

$$\frac{\partial^2 y}{\partial t^2} = -2Av \cdot (-v) = 2Av^2$$

$$\text{RHS} = \frac{1}{v^2} \cdot 2Av^2 = 2A$$

### Comparison

$$\text{LHS} = 2A = \text{RHS} = 2A \quad \checkmark$$

Equal for **all** values of $x$ and $t$.

> ✅ **$y = A(x - vt)^2$ DOES satisfy the wave equation.**
>
> It represents a parabolic pulse traveling in the $+x$ direction at speed $v$.
> Note: while mathematically valid, this solution is not physically realistic —
> the displacement grows without bound as $|x| \to \infty$. Physical waves
> require additional conditions (e.g. finite energy) to be realistic.

---

## Part c) — $y(x,t) = A\log(x + vt)$

### Is it of the form $f(x \pm vt)$?

Yes — this is $f(u) = A\log(u)$ where $u = x + vt$. It travels in the
$-x$ direction (positive $vt$ shifts the profile leftward over time).

### Computing LHS: $\partial^2 y / \partial x^2$

**First derivative** with respect to $x$:

$$\frac{\partial y}{\partial x} = \frac{A}{x + vt}$$

**Second derivative** with respect to $x$:

$$\frac{\partial^2 y}{\partial x^2} = -\frac{A}{(x + vt)^2}$$

### Computing RHS: $\frac{1}{v^2}\partial^2 y / \partial t^2$

**First derivative** with respect to $t$
(chain rule: $\partial(x+vt)/\partial t = v$):

$$\frac{\partial y}{\partial t} = \frac{A}{x + vt} \cdot v = \frac{Av}{x + vt}$$

**Second derivative** with respect to $t$:

$$\frac{\partial^2 y}{\partial t^2} = Av \cdot \left(\frac{-v}{(x+vt)^2}\right) = -\frac{Av^2}{(x+vt)^2}$$

$$\text{RHS} = \frac{1}{v^2} \cdot \left(-\frac{Av^2}{(x+vt)^2}\right) = -\frac{A}{(x+vt)^2}$$

### Comparison

$$\text{LHS} = -\frac{A}{(x+vt)^2} = \text{RHS} = -\frac{A}{(x+vt)^2} \quad \checkmark$$

Equal for all $x$ and $t$ where the function is defined (i.e. $x + vt > 0$).

> ✅ **$y = A\log(x + vt)$ DOES satisfy the wave equation.**
>
> It represents a logarithmic wave profile traveling in the $-x$ direction.
> Like the parabolic case it is mathematically valid but physically limited —
> it diverges at $x + vt = 0$ and is undefined for $x + vt \leq 0$.

---

## Summary Table

| Function | Valid wave? | Reason |
|----------|:-----------:|--------|
| $A\cos(kx^2 - \omega t)$ | ❌ No | Argument $kx^2$ is not linear in $x$ — extra $x$-dependent terms appear and destroy equality |
| $A(x-vt)^2$ | ✅ Yes | Pure $f(x-vt)$ — both sides reduce to $2A$ |
| $A\log(x+vt)$ | ✅ Yes | Pure $f(x+vt)$ — both sides reduce to $-A/(x+vt)^2$ |

## The General Proof (D'Alembert's Solution)

For any twice-differentiable $f$, define $u = x \pm vt$. Then by the chain rule:

$$\frac{\partial^2}{\partial x^2}f(u) = f''(u) \cdot \left(\frac{\partial u}{\partial x}\right)^2 = f''(u) \cdot 1^2 = f''(u)$$

$$\frac{1}{v^2}\frac{\partial^2}{\partial t^2}f(u) = \frac{1}{v^2} \cdot f''(u) \cdot \left(\frac{\partial u}{\partial t}\right)^2 = \frac{1}{v^2} \cdot f''(u) \cdot (\pm v)^2 = f''(u)$$

Both sides equal $f''(u)$ — so any function of $x \pm vt$ is automatically
a solution. Function (a) fails not because of its shape, but because $kx^2$
prevents it from being written purely as a function of $x \pm vt$.
