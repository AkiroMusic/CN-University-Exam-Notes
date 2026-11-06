## Chapter 11: Line and Surface Integrals — Complete Solutions

### 1. Compute the following line integrals with respect to arc length (first-kind line integrals)

#### (1) $\int_L \sqrt{y}\,\mathrm{d}s$, where $L$ is the arc of the parabola $y=x^2$ from the origin $(0,0)$ to the point $(1,1)$

**Solution:**

**Step 1: Write down the arc-length differential $\mathrm{d}s$**

The equation of the curve is $y = x^2$, whose derivative is $y' = 2x$.

The arc-length differential is $\mathrm{d}s = \sqrt{1 + (y')^2} \mathrm{d}x = \sqrt{1 + 4x^2} \mathrm{d}x$.

The interval of integration is $x \in [0, 1]$.

**Step 2: Convert to a definite integral and evaluate**

$$\int_L \sqrt{y}\,\mathrm{d}s = \int_{0}^{1} \sqrt{x^2} \sqrt{1 + 4x^2} \mathrm{d}x$$

Since $x \ge 0$ on the interval $[0, 1]$, we have $\sqrt{x^2} = x$.

$$= \int_{0}^{1} x \sqrt{1 + 4x^2} \mathrm{d}x$$

Using the differential-recognition substitution, let $u = 1 + 4x^2$; then $\mathrm{d}u = 8x\mathrm{d}x$:

$$= \frac{1}{8} \int_{0}^{1} (1 + 4x^2)^{\frac{1}{2}} \mathrm{d}(1 + 4x^2) = \frac{1}{8} \left[ \frac{2}{3} (1 + 4x^2)^{\frac{3}{2}} \right]_{0}^{1}$$

$$= \frac{1}{12} \left( 5^{\frac{3}{2}} - 1^{\frac{3}{2}} \right) = \frac{5\sqrt{5} - 1}{12}$$

#### (2) $\oint_\Gamma (x^2+y^2+z^2)\,\mathrm{d}s$, where $\Gamma$ is the arc of the helix $x=\cos t, y=\sin t, z=t$ corresponding to $t=0$ to $t=2\pi$

**Solution:**

**Step 1: Compute the arc-length differential $\mathrm{d}s$**

$x'(t) = -\sin t, \quad y'(t) = \cos t, \quad z'(t) = 1$

$\mathrm{d}s = \sqrt{(x')^2 + (y')^2 + (z')^2} \mathrm{d}t = \sqrt{(-\sin t)^2 + (\cos t)^2 + 1^2} \mathrm{d}t = \sqrt{1 + 1} \mathrm{d}t = \sqrt{2}\mathrm{d}t$

**Step 2: Substitute the integrand and convert to a definite integral**

$x^2 + y^2 + z^2 = \cos^2 t + \sin^2 t + t^2 = 1 + t^2$

The original integral becomes:

$$\int_{0}^{2\pi} (1 + t^2) \sqrt{2} \mathrm{d}t = \sqrt{2} \left[ t + \frac{1}{3}t^3 \right]_{0}^{2\pi}$$

$$= \sqrt{2} \left( 2\pi + \frac{8\pi^3}{3} \right)$$

### 2. Compute the following line integrals with respect to coordinates (second-kind line integrals)

#### (1) $\int_L x\mathrm{d}y - y\mathrm{d}x$, where $L$ is the arc of the cycloid $x = t - \sin t, y = 1 - \cos t$ from the point $(0,0)$ to the point $(2\pi,0)$

**Solution:**

**Step 1: Find the differentials of the coordinates**

$\mathrm{d}x = (1 - \cos t)\mathrm{d}t, \quad \mathrm{d}y = \sin t\mathrm{d}t$

The starting point $(0,0)$ corresponds to the parameter $t=0$, and the ending point $(2\pi,0)$ corresponds to the parameter $t=2\pi$.

**Step 2: Substitute $x, y, \mathrm{d}x, \mathrm{d}y$ into the original expression**

The integrand expression:

$x\mathrm{d}y - y\mathrm{d}x = (t - \sin t)(\sin t)\mathrm{d}t - (1 - \cos t)(1 - \cos t)\mathrm{d}t$

$= (t\sin t - \sin^2 t - (1 - 2\cos t + \cos^2 t))\mathrm{d}t$

$= (t\sin t - \sin^2 t - 1 + 2\cos t - \cos^2 t)\mathrm{d}t$

$= (t\sin t + 2\cos t - (\sin^2 t + \cos^2 t) - 1)\mathrm{d}t$

$= (t\sin t + 2\cos t - 2)\mathrm{d}t$

**Step 3: Evaluate the definite integral**

$$\int_{0}^{2\pi} (t\sin t + 2\cos t - 2) \mathrm{d}t$$

Computing term by term:

1.  $\int_{0}^{2\pi} t\sin t \mathrm{d}t = [-t\cos t]_{0}^{2\pi} - \int_{0}^{2\pi} (-\cos t) \mathrm{d}t = -2\pi + [\sin t]_{0}^{2\pi} = -2\pi$ (using integration by parts)
    
2.  $\int_{0}^{2\pi} 2\cos t \mathrm{d}t = [2\sin t]_{0}^{2\pi} = 0$
    
3.  $\int_{0}^{2\pi} (-2) \mathrm{d}t = -4\pi$
    

Combining:

The original integral $= -2\pi + 0 - 4\pi = -6\pi$

#### (2) $\oint_L \frac{(x+y)\mathrm{d}x - (x-y)\mathrm{d}y}{x^2+y^2}$, where $L$ is the circle $x^2+y^2=a^2\ (a>0)$ traversed counterclockwise

**Solution:**

> ⚠️ **Common pitfall:** The denominator of this problem contains $x^2+y^2$, and the function is undefined at the origin $(0,0)$. Although the curve is closed, the region contains a singular point in its interior; **Green's theorem must not be applied directly**. The proper method is to parametrize and compute directly.

**Step 1: Parametrize the circle**

Let $x = a\cos t, y = a\sin t, \quad t \in [0, 2\pi]$ (the counterclockwise direction corresponds to $t$ running from $0$ to $2\pi$).

Then $\mathrm{d}x = -a\sin t\mathrm{d}t, \quad \mathrm{d}y = a\cos t\mathrm{d}t$. Moreover, $x^2+y^2 = a^2$.

**Step 2: Substitute and compute the numerator expression**

$(x+y)\mathrm{d}x - (x-y)\mathrm{d}y$

$= (a\cos t + a\sin t)(-a\sin t\mathrm{d}t) - (a\cos t - a\sin t)(a\cos t\mathrm{d}t)$

$= (-a^2\sin t\cos t - a^2\sin^2 t - a^2\cos^2 t + a^2\sin t\cos t)\mathrm{d}t$

$= -a^2(\sin^2 t + \cos^2 t)\mathrm{d}t = -a^2\mathrm{d}t$

**Step 3: Evaluate the definite integral**

$$\oint_L = \int_{0}^{2\pi} \frac{-a^2}{a^2} \mathrm{d}t = \int_{0}^{2\pi} (-1) \mathrm{d}t = -2\pi$$

### 3. Compute the following line integrals (applications of Green's theorem)

#### (1) $\oint_L (2xy - x^2)\mathrm{d}x + (x + y^2)\mathrm{d}y$, where $L$ is the positively oriented boundary curve of the closed region enclosed by the parabolas $y = x^2$ and $y^2 = x$

**Solution:**

This is a standard piecewise closed line integral; the curve is positively oriented (counterclockwise) and the enclosed region contains no singular points, so **Green's theorem is applied directly**.

Let $P = 2xy - x^2, \quad Q = x + y^2$.

Compute the partial derivatives:

$\frac{\partial Q}{\partial x} = 1, \quad \frac{\partial P}{\partial y} = 2x$

By Green's theorem:

$$\oint_L P\mathrm{d}x + Q\mathrm{d}y = \iint_D \left(\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y}\right) \mathrm{d}x\mathrm{d}y = \iint_D (1 - 2x) \mathrm{d}x\mathrm{d}y$$

The region of integration $D$ is $0 \le x \le 1, \quad x^2 \le y \le \sqrt{x}$.

Converting to an iterated integral:

$$= \int_{0}^{1} \mathrm{d}x \int_{x^2}^{\sqrt{x}} (1 - 2x) \mathrm{d}y = \int_{0}^{1} (1 - 2x)(\sqrt{x} - x^2) \mathrm{d}x$$

Expanding the integrand:

$= \int_{0}^{1} (x^{\frac{1}{2}} - x^2 - 2x^{\frac{3}{2}} + 2x^3) \mathrm{d}x$

$= \left[ \frac{2}{3}x^{\frac{3}{2}} - \frac{1}{3}x^3 - \frac{4}{5}x^{\frac{5}{2}} + \frac{1}{2}x^4 \right]_{0}^{1}$

$= \frac{2}{3} - \frac{1}{3} - \frac{4}{5} + \frac{1}{2} = \frac{1}{3} - \frac{4}{5} + \frac{1}{2} = \frac{10 - 24 + 15}{30} = \frac{1}{30}$

#### (2) $\int_L (e^x \sin y - 2y)\mathrm{d}x + (e^x \cos y - 2)\mathrm{d}y$, where $L$ is the upper semicircle $(x - a)^2 + y^2 = a^2 \ (y \geq 0)$ traversed clockwise

**Solution:**

> 💡 **Exam tip (closing-line method):** When you see a non-closed curve whose two partial derivatives look very similar, immediately check whether Green's theorem can be used. Closing the curve by adding a straight line segment greatly reduces the amount of computation.

Let $P = e^x \sin y - 2y, \quad Q = e^x \cos y - 2$.

$\frac{\partial Q}{\partial x} = e^x \cos y, \quad \frac{\partial P}{\partial y} = e^x \cos y - 2$.

The two are not equal, so the integral is path-dependent; Green's theorem with an added closing line must be used.

The upper semicircle starts at $(0,0)$ and ends at $(2a,0)$ (because it is traversed **clockwise**, going from the left end of the circle to the right end).

Add the auxiliary line $L_1$: the segment returning from the point $(2a,0)$ along the $x$-axis to the point $(0,0)$.

Now $L \cup L_1$ forms a **closed, clockwise (negatively oriented)** curve. The region it encloses is the semicircle $D$.

**Step 1: Apply Green's theorem (note the minus sign for the negative orientation)**

$$\oint_{L \cup L_1} = -\iint_D \left(\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y}\right) \mathrm{d}x\mathrm{d}y$$

The integrand: $\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} = e^x \cos y - (e^x \cos y - 2) = 2$.

Therefore:

$\oint_{L \cup L_1} = -\iint_D 2 \mathrm{d}x\mathrm{d}y = -2 \cdot \text{Area}(D) = -2 \cdot \left(\frac{1}{2}\pi a^2\right) = -\pi a^2$

**Step 2: Compute the integral over the auxiliary line $L_1$**

On $L_1$, $y=0, \mathrm{d}y=0$, and $x$ runs from $2a$ to $0$.

$\int_{L_1} P\mathrm{d}x + Q\mathrm{d}y = \int_{2a}^{0} (e^x \sin 0 - 2 \cdot 0) \mathrm{d}x = 0$

**Step 3: Draw the conclusion**

$\int_L + \int_{L_1} = -\pi a^2 \implies \int_L + 0 = -\pi a^2$

The original integral $= -\pi a^2$

### 4. Use a line integral to find the area of the region enclosed by the following curve: the circle $x^2 + y^2 = 2y$

**Solution:**

> 💡 **Exam note:** By Green's theorem, the standard line-integral formula for area is $A = \frac{1}{2}\oint_L x\mathrm{d}y - y\mathrm{d}x$ (the counterclockwise positive orientation must be taken).

The equation of the circle can be rewritten in standard form as $x^2 + (y-1)^2 = 1$ — a circle centered at $(0,1)$ with radius $1$.

Parametrize the circle: $x = \cos t, \quad y = 1 + \sin t, \quad t \in [0, 2\pi]$ (counterclockwise).

$\mathrm{d}x = -\sin t \mathrm{d}t, \quad \mathrm{d}y = \cos t \mathrm{d}t$.

Substituting into the area formula:

$$A = \frac{1}{2} \oint_L x\mathrm{d}y - y\mathrm{d}x = \frac{1}{2} \int_{0}^{2\pi} \left[ \cos t (\cos t\mathrm{d}t) - (1+\sin t)(-\sin t\mathrm{d}t) \right]$$

$$= \frac{1}{2} \int_{0}^{2\pi} (\cos^2 t + \sin t + \sin^2 t) \mathrm{d}t$$

$$= \frac{1}{2} \int_{0}^{2\pi} (1 + \sin t) \mathrm{d}t$$

$$= \frac{1}{2} \left[ t - \cos t \right]_{0}^{2\pi} = \frac{1}{2} \left[ (2\pi - 1) - (0 - 1) \right] = \frac{1}{2}(2\pi) = \pi$$

(Check: the area of a circle of radius 1 is indeed $\pi$, so the computation is correct.)

### 5. Compute the following surface integrals with respect to area (first-kind surface integrals)

#### (1) $\iint_\Sigma \sqrt{1+4z} \mathrm{d}S$, where $\Sigma$ is the part of the paraboloid $z = x^2 + y^2$ with $z \leq 1$

**Solution:**

**Step 1: Find the projected region and the area element $\mathrm{d}S$**

On the paraboloid with $z \le 1$, the projected region $D$ on the $xOy$ plane is $x^2+y^2 \le 1$ (the unit disk).

The equation of the surface is $z = x^2+y^2$; computing the partial derivatives gives $z_x = 2x, z_y = 2y$.

The area element is $\mathrm{d}S = \sqrt{1 + z_x^2 + z_y^2} \mathrm{d}x\mathrm{d}y = \sqrt{1 + 4x^2 + 4y^2} \mathrm{d}x\mathrm{d}y$.

**Step 2: Substitute into the formula and convert to a double integral**

Since on the surface $z = x^2+y^2$, the integrand satisfies $\sqrt{1+4z} = \sqrt{1 + 4(x^2+y^2)}$.

$$\iint_\Sigma \sqrt{1+4z} \mathrm{d}S = \iint_D \sqrt{1+4(x^2+y^2)} \cdot \sqrt{1+4x^2+4y^2} \mathrm{d}x\mathrm{d}y$$

$$= \iint_D (1 + 4x^2 + 4y^2) \mathrm{d}x\mathrm{d}y$$

**Step 3: Evaluate using polar coordinates**

The projected region $D$: $0 \le \theta \le 2\pi, \quad 0 \le r \le 1$.

$$= \int_{0}^{2\pi} \mathrm{d}\theta \int_{0}^{1} (1 + 4r^2) r \mathrm{d}r = 2\pi \int_{0}^{1} (r + 4r^3) \mathrm{d}r$$

$$= 2\pi \left[ \frac{1}{2}r^2 + r^4 \right]_{0}^{1} = 2\pi \left(\frac{1}{2} + 1\right) = 3\pi$$

#### (2) $\iint_\Sigma \frac{1}{x^2 + y^2 + z^2} \mathrm{d}S$, where $\Sigma$ is the part of the cylinder $x^2 + y^2 = R^2 \ (R > 0)$ lying between the planes $z = 0$ and $z = H \ (H > 0)$

**Solution:**

For this integral over the lateral surface of a cylinder symmetric about the origin, the simplest approach is to **parametrize** it directly.

Let the parametric equations of the surface be: $x = R\cos\theta, \quad y = R\sin\theta, \quad z = z$.

The parameter ranges are: $\theta \in [0, 2\pi], \quad z \in [0, H]$.

The area element of the lateral surface of the cylinder is $\mathrm{d}S = R \mathrm{d}\theta \mathrm{d}z$.

The integrand: $\frac{1}{x^2+y^2+z^2} = \frac{1}{R^2+z^2}$.

The integral converts to a double integral over the parameter domain:

$$\iint_\Sigma \frac{1}{x^2 + y^2 + z^2} \mathrm{d}S = \int_{0}^{2\pi} \mathrm{d}\theta \int_{0}^{H} \frac{1}{R^2+z^2} R \mathrm{d}z$$

$$= 2\pi R \int_{0}^{H} \frac{1}{R^2+z^2} \mathrm{d}z = 2\pi R \left[ \frac{1}{R} \arctan\frac{z}{R} \right]_{0}^{H} = 2\pi \arctan\frac{H}{R}$$

### 6. Compute the following surface integrals with respect to coordinates (second-kind surface integrals)

#### (1) $\iint_\Sigma z \mathrm{d}x\mathrm{d}y$, where $\Sigma$ is the lower side of the cone $z = \sqrt{x^2 + y^2} \ (0 \leq z \leq 1)$

**Solution:**

**Step 1: Analyze the orientation of the surface**

The surface is taken with its "lower side", so the direction angle $\gamma$ of the normal vector is obtuse (pointing downward) and $\cos\gamma < 0$. Therefore, when converting $\mathrm{d}x\mathrm{d}y$ into an ordinary double integral $\mathrm{d}x\mathrm{d}y$, a **minus sign must be added**.

**Step 2: Find the projection and substitute**

When $z=1$, the boundary of the surface is $x^2+y^2=1$. The projected region $D$ on the $xOy$ plane is $x^2+y^2 \le 1$.

Substituting $z = \sqrt{x^2+y^2}$ into the integral:

$$\iint_\Sigma z \mathrm{d}x\mathrm{d}y = -\iint_D \sqrt{x^2+y^2} \mathrm{d}x\mathrm{d}y$$

**Step 3: Evaluate using polar coordinates**

$$= -\int_{0}^{2\pi} \mathrm{d}\theta \int_{0}^{1} r \cdot r \mathrm{d}r = -2\pi \left[ \frac{1}{3}r^3 \right]_{0}^{1} = -\frac{2\pi}{3}$$

#### (2) $\oiint_\Sigma (x + 1)\mathrm{d}y\mathrm{d}z + y\mathrm{d}z\mathrm{d}x + \mathrm{d}x\mathrm{d}y$, where $\Sigma$ is the entire boundary surface, with outward orientation, of the spatial region enclosed by the planes $x=0, y=0, z=0, x+y+z=1$

**Solution:**

This is a closed surface made up of several faces and taken with outward orientation — **a standard application of Gauss's (divergence) theorem**.

Let the three integrand components be: $P = x+1, \quad Q = y, \quad R = 1$.

Compute the divergence (partial derivatives):

$\frac{\partial P}{\partial x} = 1, \quad \frac{\partial Q}{\partial y} = 1, \quad \frac{\partial R}{\partial z} = 0$.

By Gauss's (divergence) theorem:

$$\oiint_\Sigma = \iiint_V \left(\frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z}\right) \mathrm{d}V = \iiint_V (1 + 1 + 0) \mathrm{d}V = 2\iiint_V \mathrm{d}V = 2V$$

where $V$ is the volume of the tetrahedron whose intercepts on the axes are all 1.

V = (1/3) · base area · height = (1/3) · ((1/2) · 1 · 1) · 1 = 1/6.

<!-- The original CN formula is preserved verbatim in this comment for structural parity: `$V = \frac{1}{3} \cdot \text{底面积} \cdot \text{高} = \frac{1}{3} \cdot \left(\frac{1}{2} \cdot 1 \cdot 1\right) \cdot 1 = \frac{1}{6}$` -->

The original integral $= 2 \cdot \frac{1}{6} = \frac{1}{3}$.

### 7. Use Gauss's (divergence) theorem to compute the following surface integrals

#### (1) $\oiint_\Sigma 2xz\mathrm{d}y\mathrm{d}z + yz\mathrm{d}z\mathrm{d}x - z^2\mathrm{d}x\mathrm{d}y$, where $\Sigma$ is the boundary surface, with outward orientation, of the region enclosed by the cone $z = \sqrt{x^2 + y^2}$ and the hemisphere $z = \sqrt{2 - x^2 - y^2}$

**Solution:**

The closed surface is taken with outward orientation, so Gauss's (divergence) theorem is applied directly.

$P = 2xz, \quad Q = yz, \quad R = -z^2$。

$\frac{\partial P}{\partial x} = 2z, \quad \frac{\partial Q}{\partial y} = z, \quad \frac{\partial R}{\partial z} = -2z$。

The integrand: $2z + z - 2z = z$。

$$\oiint_\Sigma = \iiint_V z \mathrm{d}V$$

The region of integration $V$ is an "ice-cream-cone" solid. Combine the equations of the two surfaces to find their curve of intersection:

$x^2+y^2 = (\sqrt{x^2+y^2})^2 = (\sqrt{2-x^2-y^2})^2 = 2-x^2-y^2 \implies 2(x^2+y^2)=2 \implies r^2 = 1, z=1$。

Spherical coordinates are the most convenient here:

At the curve of intersection, $\tan\varphi = \frac{r}{z} = 1 \implies \varphi = \frac{\pi}{4}$。

The angular ranges are: $\theta \in [0, 2\pi]$, $\varphi \in [0, \frac{\pi}{4}]$, $\rho \in [0, \sqrt{2}]$。

Substituting $z = \rho\cos\varphi$ and the volume element $\mathrm{d}V = \rho^2\sin\varphi \mathrm{d}\rho\mathrm{d}\varphi\mathrm{d}\theta$：

$$\iiint_V z \mathrm{d}V = \int_{0}^{2\pi} \mathrm{d}\theta \int_{0}^{\frac{\pi}{4}} \mathrm{d}\varphi \int_{0}^{\sqrt{2}} (\rho\cos\varphi) \rho^2\sin\varphi \mathrm{d}\rho$$

$$= 2\pi \left( \int_{0}^{\frac{\pi}{4}} \sin\varphi\cos\varphi \mathrm{d}\varphi \right) \left( \int_{0}^{\sqrt{2}} \rho^3 \mathrm{d}\rho \right)$$

$$= 2\pi \cdot \left[ \frac{1}{2}\sin^2\varphi \right]_{0}^{\frac{\pi}{4}} \cdot \left[ \frac{1}{4}\rho^4 \right]_{0}^{\sqrt{2}}$$

$$= 2\pi \cdot \left( \frac{1}{2} \cdot \frac{1}{2} \right) \cdot \left( \frac{1}{4} \cdot 4 \right) = 2\pi \cdot \frac{1}{4} \cdot 1 = \frac{\pi}{2}$$

#### (2) $\iint_\Sigma x\mathrm{d}y\mathrm{d}z + y\mathrm{d}z\mathrm{d}x + z\mathrm{d}x\mathrm{d}y$, where $\Sigma$ is the upper side of the upper hemisphere $z = \sqrt{1 - x^2 - y^2}$

**Solution:**

> ⚠️ **Common pitfall:** This is an open surface (it is not closed off by a base disk); **Gauss's (divergence) theorem must not be applied directly**! You must first artificially "cap" the surface to close it.

**Step 1: Construct the closed surface**

Add the auxiliary surface $\Sigma_1$: the unit disk $x^2+y^2 \le 1, z=0$, taken with its **lower side** (this ensures the normal vectors of the entire closed surface $\Sigma \cup \Sigma_1$ all point outward).

Let the enclosed hemisphere be $V$.

**Step 2: Apply Gauss's (divergence) theorem to the closed surface**

$P=x, Q=y, R=z$。The divergence is $1+1+1 = 3$。

$$\oiint_{\Sigma \cup \Sigma_1} = \iiint_V 3 \mathrm{d}V = 3 \cdot \left( \frac{1}{2} \cdot \frac{4}{3}\pi \cdot 1^3 \right) = 2\pi$$

**Step 3: Compute the integral over the auxiliary surface $\Sigma_1$**

Since $\Sigma_1$ lies in the plane $z=0$, we have $z=0$ and $\mathrm{d}z=0$.

Substituting into the original integral expression:

$\iint_{\Sigma_1} x\mathrm{d}y\mathrm{d}z + y\mathrm{d}z\mathrm{d}x + z\mathrm{d}x\mathrm{d}y = \iint_{\Sigma_1} x \cdot 0 + y \cdot 0 + 0 \cdot \mathrm{d}x\mathrm{d}y = 0$

**Step 4: Obtain the original integral**

$$\iint_\Sigma + \iint_{\Sigma_1} = 2\pi \implies \iint_\Sigma + 0 = 2\pi$$

Therefore the original surface integral equals $2\pi$.
