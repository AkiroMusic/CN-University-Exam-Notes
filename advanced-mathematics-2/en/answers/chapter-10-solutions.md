## Chapter 10: Multiple Integrals — Complete Solutions

### 1. $I=\iint\limits_D \sqrt{1-x^2-y^2}\,\mathrm{d}\sigma$, where $D$ is the region enclosed by the curve $y=\sqrt{1-x^2}$ and the line $y=0$

**Solution:**

**Step 1: Determine the region of integration**

Squaring both sides of the curve equation $y=\sqrt{1-x^2}$ gives $x^2+y^2=1$ (with $y \ge 0$).

Hence the region $D$ is the upper half of the unit disk: $x^2+y^2 \le 1, y \ge 0$.

**Step 2: Convert to polar coordinates**

Let $x = r\cos\theta, y = r\sin\theta$; then the area element is $\mathrm{d}\sigma = r\,\mathrm{d}r\,\mathrm{d}\theta$.

The range of integration in polar coordinates is: $0 \le \theta \le \pi, \quad 0 \le r \le 1$.

**Step 3: Evaluate the integral**

$$I = \int_{0}^{\pi} \mathrm{d}\theta \int_{0}^{1} \sqrt{1-r^2} \cdot r\,\mathrm{d}r$$

Since the integrand depends only on $r$, the integral separates:

$$I = \left( \int_{0}^{\pi} 1 \,\mathrm{d}\theta \right) \cdot \left( \int_{0}^{1} (1-r^2)^{\frac{1}{2}} r\,\mathrm{d}r \right)$$

$$I = [\theta]_{0}^{\pi} \cdot \left[ -\frac{1}{3}(1-r^2)^{\frac{3}{2}} \right]_{0}^{1}$$

$$I = \pi \cdot \left( 0 - \left(-\frac{1}{3}\right) \right) = \frac{\pi}{3}$$

### 2. Sketch each region of integration and change the order of integration of each iterated integral

#### (1) $\int_{1}^{2}\mathrm{d}x\int_{2-x}^{\sqrt{2x-x^2}} f(x,y)\mathrm{d}y$

**Solution:**

**Step 1: Recover the boundary of the region of integration $D$**

From the original limits of integration, the region $D$ satisfies: $1 \le x \le 2$, and $2-x \le y \le \sqrt{2x-x^2}$.

-   Lower boundary: $y = 2-x \implies x = 2-y$ (a straight line through the points $(1,1)$ and $(2,0)$)
    
-   Upper boundary: $y = \sqrt{2x-x^2} \implies y^2 = 2x-x^2 \implies (x-1)^2+y^2=1$ (the part, lying in the first quadrant, of the circle centered at $(1,0)$ with radius 1). Solving the equation for $x$: $x = 1 + \sqrt{1-y^2}$ (taking the right half of the circle).
    

**Step 2: Change the order of integration ($x$ first, then $y$)**

From the sketch, the two boundaries intersect at $(1,1)$ and $(2,0)$.

Projecting the region onto the $y$-axis, the range of $y$ is $0 \le y \le 1$.

For fixed $y$, the left boundary (entry point) is the line $x = 2-y$, and the right boundary (exit point) is the circular arc $x = 1+\sqrt{1-y^2}$.

Hence the integral with the order changed is:

$$\int_{0}^{1}\mathrm{d}y\int_{2-y}^{1+\sqrt{1-y^2}} f(x,y)\mathrm{d}x$$

#### (2) $\int_{1}^{2}\mathrm{d}x\int_{\frac{1}{x}}^{1} f(x,y)\mathrm{d}y$

**Solution:**

**Step 1: Recover the region of integration $D$**

The region $D$ satisfies: $1 \le x \le 2$, and $\frac{1}{x} \le y \le 1$.

The boundary curves are the hyperbola $y = \frac{1}{x}$, the horizontal line $y = 1$, and the vertical lines $x = 1$ and $x = 2$.

**Step 2: Change the order of integration ($x$ first, then $y$)**

According to the intersection points, the hyperbola meets $x=2$ at $(2, \frac{1}{2})$ and $x=1$ at $(1,1)$.

Projecting the region onto the $y$-axis, the range of $y$ is $\frac{1}{2} \le y \le 1$.

For fixed $y$, crossing the region from left to right, the left boundary is the hyperbola $x = \frac{1}{y}$ and the right boundary is the line $x = 2$.

Hence the integral with the order changed is:

$$\int_{\frac{1}{2}}^{1}\mathrm{d}y\int_{\frac{1}{y}}^{2} f(x,y)\mathrm{d}x$$

### 3. Compute the following double integrals

#### (1) $\iint\limits_D (3x-2y)\mathrm{d}\sigma$, where $D$ is the closed region enclosed by the two coordinate axes and the line $x+y=2$

**Solution:**

The region $D$ is an isosceles right triangle with vertices $(0,0), (2,0), (0,2)$.

Convert to an iterated integral with $y$ first and then $x$:

$$\iint\limits_D (3x-2y)\mathrm{d}\sigma = \int_{0}^{2}\mathrm{d}x\int_{0}^{2-x} (3x-2y)\mathrm{d}y$$

First compute the inner integral:

$$\int_{0}^{2-x} (3x-2y)\mathrm{d}y = \left[ 3xy - y^2 \right]_{0}^{2-x} = 3x(2-x) - (2-x)^2$$

Expanding gives:

$$= 6x - 3x^2 - (4 - 4x + x^2) = -4x^2 + 10x - 4$$

Then compute the outer integral:

$$\int_{0}^{2} (-4x^2 + 10x - 4)\mathrm{d}x = \left[ -\frac{4}{3}x^3 + 5x^2 - 4x \right]_{0}^{2}$$

$$= -\frac{32}{3} + 20 - 8 = 12 - \frac{32}{3} = \frac{4}{3}$$

#### (2) $\iint\limits_D xy^2\mathrm{d}\sigma$, where $D$ is the closed right half-region enclosed by the circle $x^2+y^2=4$ and the $y$-axis

**Solution:**

Since the region is related to a circle, polar coordinates are the most convenient.

The region $D$ is the right half-disk: $0 \le r \le 2, \quad -\frac{\pi}{2} \le \theta \le \frac{\pi}{2}$.

The integrand becomes: $xy^2 = (r\cos\theta)(r\sin\theta)^2 = r^3\cos\theta\sin^2\theta$.

Substituting into the double-integral formula in polar coordinates:

$$\iint\limits_D xy^2\mathrm{d}\sigma = \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\mathrm{d}\theta\int_{0}^{2} (r^3\cos\theta\sin^2\theta) \cdot r\,\mathrm{d}r$$

Separating the variables and integrating:

$$= \left( \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}} \cos\theta\sin^2\theta\,\mathrm{d}\theta \right) \cdot \left( \int_{0}^{2} r^4\,\mathrm{d}r \right)$$

Computing each separately:

$$\int_{0}^{2} r^4\,\mathrm{d}r = \left[ \frac{1}{5}r^5 \right]_{0}^{2} = \frac{32}{5}$$

$$\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}} \sin^2\theta\,\mathrm{d}(\sin\theta) = \left[ \frac{1}{3}\sin^3\theta \right]_{-\frac{\pi}{2}}^{\frac{\pi}{2}} = \frac{1}{3}(1 - (-1)) = \frac{2}{3}$$

Multiplying the two:

$$\iint\limits_D xy^2\mathrm{d}\sigma = \frac{2}{3} \cdot \frac{32}{5} = \frac{64}{15}$$

### 4. Compute the volume of the solid enclosed by the coordinate planes, the planes $x=4$, $y=4$, and the paraboloid $z=x^2+y^2+1$

**Solution:**

Since the base of the solid lies in the coordinate plane ($z=0$), the top boundary is the paraboloid $z=x^2+y^2+1$, and the region of integration is the square region $D=\{(x,y) \mid 0 \le x \le 4, 0 \le y \le 4\}$.

The volume $V$ can be expressed as the double integral of the curved-top cylindrical solid:

$$V = \iint\limits_D (x^2+y^2+1)\mathrm{d}\sigma = \int_{0}^{4}\mathrm{d}x\int_{0}^{4} (x^2+y^2+1)\mathrm{d}y$$

Compute the inner integral:

$$\int_{0}^{4} (x^2+y^2+1)\mathrm{d}y = \left[ x^2y + \frac{1}{3}y^3 + y \right]_{0}^{4} = 4x^2 + \frac{64}{3} + 4 = 4x^2 + \frac{76}{3}$$

Compute the outer integral:

$$V = \int_{0}^{4} \left( 4x^2 + \frac{76}{3} \right)\mathrm{d}x = \left[ \frac{4}{3}x^3 + \frac{76}{3}x \right]_{0}^{4}$$

$$V = \frac{4}{3}(64) + \frac{76}{3}(4) = \frac{256}{3} + \frac{304}{3} = \frac{560}{3}$$

### 5. Use polar coordinates to compute the following double integrals

#### (1) $\iint\limits_D e^{-x^2-y^2}\,\mathrm{d}\sigma$, where $D$ is the part of the unit disk in the first quadrant

**Solution:**

In polar coordinates the region $D$ is given by: $0 \le \theta \le \frac{\pi}{2}, \quad 0 \le r \le 1$.

The integrand becomes $e^{-x^2-y^2} = e^{-r^2}$.

$$\iint\limits_D e^{-x^2-y^2}\,\mathrm{d}\sigma = \int_{0}^{\frac{\pi}{2}}\mathrm{d}\theta\int_{0}^{1} e^{-r^2} r\,\mathrm{d}r$$

The outer integral is immediate: $\int_{0}^{\frac{\pi}{2}}\mathrm{d}\theta = \frac{\pi}{2}$.

For the inner integral, recognize the differential:

$$\int_{0}^{1} e^{-r^2} r\,\mathrm{d}r = -\frac{1}{2}\int_{0}^{1} e^{-r^2} \mathrm{d}(-r^2) = \left[ -\frac{1}{2}e^{-r^2} \right]_{0}^{1} = -\frac{1}{2}(e^{-1} - 1) = \frac{1}{2}\left(1 - \frac{1}{e}\right)$$

Hence the original integral is:

$$\frac{\pi}{2} \cdot \frac{1}{2}\left(1 - \frac{1}{e}\right) = \frac{\pi}{4}\left(1 - \frac{1}{e}\right)$$

#### (2) $\iint\limits_D (4 - x - y)\,\mathrm{d}\sigma$, where $D$ is the disk $x^2 + y^2 \le 2y$

**Solution:**

> 💡 **Exam tip:** The problem explicitly asks to "compute using polar coordinates", so the polar-coordinate steps must be written out. However, after finishing, it is strongly recommended to verify using **odd–even symmetry plus the centroid formula**: the region is a disk centered at $(0,1)$ with area $\pi$; by symmetry $\iint x\,\mathrm{d}\sigma = 0$, and $\iint y\,\mathrm{d}\sigma = \bar{y} \cdot A = 1 \cdot \pi = \pi$, so the total integral is $4\pi - 0 - \pi = 3\pi$.

**Formal polar-coordinate solution:**

Convert the boundary $x^2 + y^2 = 2y$ to polar coordinates: $r^2 = 2r\sin\theta \implies r = 2\sin\theta$.

Since $r \ge 0$, we have $\sin\theta \ge 0$, so the polar-angle range of the region is: $0 \le \theta \le \pi$.

The integrand becomes $4 - r\cos\theta - r\sin\theta$.

$$I = \int_{0}^{\pi}\mathrm{d}\theta\int_{0}^{2\sin\theta} (4 - r\cos\theta - r\sin\theta)r\,\mathrm{d}r$$

The inner integral:

$$\int_{0}^{2\sin\theta} (4r - r^2\cos\theta - r^2\sin\theta)\,\mathrm{d}r = \left[ 2r^2 - \frac{1}{3}r^3\cos\theta - \frac{1}{3}r^3\sin\theta \right]_{0}^{2\sin\theta}$$

$$= 8\sin^2\theta - \frac{8}{3}\sin^3\theta\cos\theta - \frac{8}{3}\sin^4\theta$$

Substituting into the outer integral and computing term by term:

1.  $\int_{0}^{\pi} 8\sin^2\theta\,\mathrm{d}\theta = 8 \times 2\int_{0}^{\frac{\pi}{2}} \sin^2\theta\,\mathrm{d}\theta = 16 \times \frac{1}{2}\frac{\pi}{2} = 4\pi$ (using Wallis' formula)
    
2.  $\int_{0}^{\pi} \frac{8}{3}\sin^3\theta\cos\theta\,\mathrm{d}\theta = \frac{8}{3}\left[ \frac{1}{4}\sin^4\theta \right]_{0}^{\pi} = 0$
    
3.  $\int_{0}^{\pi} \frac{8}{3}\sin^4\theta\,\mathrm{d}\theta = \frac{8}{3} \times 2\int_{0}^{\frac{\pi}{2}} \sin^4\theta\,\mathrm{d}\theta = \frac{16}{3} \times \frac{3}{4}\frac{1}{2}\frac{\pi}{2} = \pi$
    

Combining the results:

$$I = 4\pi - 0 - \pi = 3\pi$$

### 6. Find the area of the part of the hemisphere $z=\sqrt{2-x^2-y^2}$ cut out by the cone $z=\sqrt{x^2+y^2}$ that lies inside the cone

**Solution:**

> ⚠️ **Common pitfall:** What is asked for is the "area", not the "volume"; the first-kind surface integral formula $A = \iint\limits_D \sqrt{1 + z_x^2 + z_y^2} \,\mathrm{d}\sigma$ must be used.

**Step 1: Find the projected region of integration $D$**

Combine the equations of the two surfaces to find their curve of intersection:

$\sqrt{2-x^2-y^2} = \sqrt{x^2+y^2} \implies 2-(x^2+y^2) = x^2+y^2 \implies x^2+y^2 = 1$.

Hence the region $D$ projected onto the $xOy$ plane is the unit disk: $x^2+y^2 \le 1$.

**Step 2: Compute the area element $dS$ of the surface**

Compute the partial derivatives of the hemisphere $z=\sqrt{2-x^2-y^2}$:

$z_x = \frac{-x}{\sqrt{2-x^2-y^2}}, \quad z_y = \frac{-y}{\sqrt{2-x^2-y^2}}$

$1 + z_x^2 + z_y^2 = 1 + \frac{x^2}{2-x^2-y^2} + \frac{y^2}{2-x^2-y^2} = \frac{2-x^2-y^2+x^2+y^2}{2-x^2-y^2} = \frac{2}{2-x^2-y^2}$

The area element is $dS = \frac{\sqrt{2}}{\sqrt{2-x^2-y^2}}\mathrm{d}x\mathrm{d}y$.

**Step 3: Evaluate the integral**

Convert to polar coordinates:

$$A = \iint\limits_D \frac{\sqrt{2}}{\sqrt{2-x^2-y^2}}\mathrm{d}\sigma = \int_{0}^{2\pi}\mathrm{d}\theta\int_{0}^{1} \frac{\sqrt{2}}{\sqrt{2-r^2}} r\,\mathrm{d}r$$

The outer integral equals $2\pi$. For the inner integral, recognize the differential:

$$\int_{0}^{1} \sqrt{2}(2-r^2)^{-\frac{1}{2}} r\,\mathrm{d}r = -\frac{\sqrt{2}}{2}\int_{0}^{1} (2-r^2)^{-\frac{1}{2}} \mathrm{d}(2-r^2) = -\frac{\sqrt{2}}{2} \left[ 2(2-r^2)^{\frac{1}{2}} \right]_{0}^{1}$$

$$= -\sqrt{2} \left( \sqrt{1} - \sqrt{2} \right) = -\sqrt{2} + 2 = 2 - \sqrt{2}$$

The total area:

$$A = 2\pi(2 - \sqrt{2})$$

### 7. Find the surface area of the solid enclosed by two mutually perpendicular circular cylinders $x^2+y^2=R^2$ and $x^2+z^2=R^2$ with the same base radius

**Solution:**

> 💡 **Exam tip (ultimate symmetry method):** This is the surface area of the famous "mou he fang gai" (Steinmetz) solid. The solid is pieced together from completely identical surface patches in the 8 octants (front/back, left/right, top/bottom), and the surfaces of the two cylinders are symmetric to each other. We only need to compute the surface area of one cylinder piece (say $x^2+z^2=R^2$) in the first octant, and then multiply by **16** (2 cylinders $\times$ 8 octants = 16 patches).

**Step 1: Determine the single integration surface and the projected region**

Consider a portion of the cylinder $x^2+z^2=R^2$ inside the first octant ($x \ge 0, y \ge 0, z \ge 0$).

Its equation is $z = \sqrt{R^2-x^2}$.

This portion of surface lies inside the other cylinder $x^2+y^2=R^2$, so its projected region $D_1$ on the $xOy$ plane is:

$0 \le x \le R, \quad 0 \le y \le \sqrt{R^2-x^2}$.

**Step 2: Compute the area element $dS$**

Compute the partial derivatives of $z = \sqrt{R^2-x^2}$:

$z_x = \frac{-x}{\sqrt{R^2-x^2}}, \quad z_y = 0$

$1 + z_x^2 + z_y^2 = 1 + \frac{x^2}{R^2-x^2} = \frac{R^2}{R^2-x^2}$

The area element is $dS = \frac{R}{\sqrt{R^2-x^2}}\mathrm{d}x\mathrm{d}y$.

**Step 3: Compute the area $S_1$ of the single patch in the first octant**

$$S_1 = \iint\limits_{D_1} \frac{R}{\sqrt{R^2-x^2}}\mathrm{d}\sigma = \int_{0}^{R}\mathrm{d}x\int_{0}^{\sqrt{R^2-x^2}} \frac{R}{\sqrt{R^2-x^2}}\mathrm{d}y$$

The inner integral is:

$$\left[ \frac{R}{\sqrt{R^2-x^2}} y \right]_{0}^{\sqrt{R^2-x^2}} = \frac{R}{\sqrt{R^2-x^2}} \cdot \sqrt{R^2-x^2} = R$$

The outer integral is:

$$S_1 = \int_{0}^{R} R\,\mathrm{d}x = R \cdot R = R^2$$

**Step 4: Obtain the total area**

The solid is made up of two cylinder surfaces, each of which has surface patches of area $R^2$ in each of the 8 octants — 16 patches in total.

The total surface area is $S = 16 \times S_1 = 16R^2$.
