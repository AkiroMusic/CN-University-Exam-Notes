## Chapter 8: Analytic Geometry in Space and Vector Algebra — Complete Solutions

### 1. Given that the vector $\boldsymbol{b}$ is collinear with $\boldsymbol{a}=2\boldsymbol{i}-\boldsymbol{j}+2\boldsymbol{k}$ and $\boldsymbol{a} \cdot \boldsymbol{b} = -18$, find the vector $\boldsymbol{b}$

**Solution:**

Since the vector $\boldsymbol{b}$ is collinear with $\boldsymbol{a}$, by the necessary and sufficient condition for collinearity of vectors there must exist a real number $\lambda$ such that:

$$\boldsymbol{b} = \lambda \boldsymbol{a} = 2\lambda\boldsymbol{i} - \lambda\boldsymbol{j} + 2\lambda\boldsymbol{k}$$

By the given condition, the dot product of the two vectors is $\boldsymbol{a} \cdot \boldsymbol{b} = -18$; substituting into the equation above gives:

$$\boldsymbol{a} \cdot (\lambda \boldsymbol{a}) = \lambda \|\boldsymbol{a}\|^2 = -18$$

Compute the squared magnitude of the vector $\boldsymbol{a}$:

$$\|\boldsymbol{a}\|^2 = 2^2 + (-1)^2 + 2^2 = 4 + 1 + 4 = 9$$

Substituting this into the dot-product equation:

$$9\lambda = -18 \implies \lambda = -2$$

Substituting $\lambda = -2$ back into the original expression gives the vector $\boldsymbol{b}$:

$$\boldsymbol{b} = -2(2\boldsymbol{i}-\boldsymbol{j}+2\boldsymbol{k}) = -4\boldsymbol{i}+2\boldsymbol{j}-4\boldsymbol{k}$$

Or, in coordinate form: $\boldsymbol{b} = (-4, 2, -4)$.

### 2. Given $\|\boldsymbol{a}\|=4$, $\|\boldsymbol{b}\|=2$, $\|\boldsymbol{a}-\boldsymbol{b}\|=2\sqrt{7}$, find the angle between $\boldsymbol{a}$ and $\boldsymbol{b}$

**Solution:**

Squaring both sides of the given condition $\|\boldsymbol{a}-\boldsymbol{b}\|=2\sqrt{7}$ gives:

$$\|\boldsymbol{a}-\boldsymbol{b}\|^2 = (2\sqrt{7})^2 = 28$$

Expanding the left-hand side gives:

$$\|\boldsymbol{a}\|^2 - 2\boldsymbol{a} \cdot \boldsymbol{b} + \|\boldsymbol{b}\|^2 = 28$$

Substituting $\|\boldsymbol{a}\|=4$ and $\|\boldsymbol{b}\|=2$ into the equation above:

$$4^2 - 2\boldsymbol{a} \cdot \boldsymbol{b} + 2^2 = 28$$

$$16 - 2\boldsymbol{a} \cdot \boldsymbol{b} + 4 = 28 \implies -2\boldsymbol{a} \cdot \boldsymbol{b} = 8 \implies \boldsymbol{a} \cdot \boldsymbol{b} = -4$$

Let the angle between $\boldsymbol{a}$ and $\boldsymbol{b}$ be $\theta$ (where $\theta \in [0, \pi]$). By the definition of the dot product:

$$\cos\theta = \frac{\boldsymbol{a} \cdot \boldsymbol{b}}{\|\boldsymbol{a}\| \|\boldsymbol{b}\|} = \frac{-4}{4 \times 2} = -\frac{1}{2}$$

Since $\theta \in [0, \pi]$, we have:

$$\theta = \frac{2\pi}{3} \quad (\text{or } 120^\circ)$$

### 3. Find the area of the triangle with vertices $A(1,-1,1)$, $B(-1,0,2)$, $C(2,-2,1)$, and the height on the side $AB$

**Solution:**

**Step 1: Compute the coordinates of the vectors $\vec{AB}$ and $\vec{AC}$**

$$\vec{AB} = (-1-1, 0-(-1), 2-1) = (-2, 1, 1)$$

$$\vec{AC} = (2-1, -2-(-1), 1-1) = (1, -1, 0)$$

**Step 2: Compute the cross product (vector product) of the vectors, $\vec{AB} \times \vec{AC}$**

$$\vec{AB} \times \vec{AC} = \begin{vmatrix} \boldsymbol{i} & \boldsymbol{j} & \boldsymbol{k} \\ -2 & 1 & 1 \\ 1 & -1 & 0 \end{vmatrix} = (0 - (-1))\boldsymbol{i} - (0 - 1)\boldsymbol{j} + (2 - 1)\boldsymbol{k} = \boldsymbol{i} + \boldsymbol{j} + \boldsymbol{k}$$

**Step 3: Find the area $S$ of $\triangle ABC$**

The magnitude of the cross product is:

$$\|\vec{AB} \times \vec{AC}\| = \sqrt{1^2 + 1^2 + 1^2} = \sqrt{3}$$

The area of the triangle is therefore:

$$S = \frac{1}{2}\|\vec{AB} \times \vec{AC}\| = \frac{\sqrt{3}}{2}$$

**Step 4: Find the height $h$ on the side $AB$**

First compute the length of the base $AB$:

$$\|\vec{AB}\| = \sqrt{(-2)^2 + 1^2 + 1^2} = \sqrt{6}$$

By the triangle area formula $S = \frac{1}{2} \|\vec{AB}\| \cdot h$, we get:

$$\frac{\sqrt{3}}{2} = \frac{1}{2} \sqrt{6} \cdot h \implies h = \frac{\sqrt{3}}{\sqrt{6}} = \frac{1}{\sqrt{2}} = \frac{\sqrt{2}}{2}$$

### 4. Given two points $M_1(3,-1,2)$ and $M_2(4,-2,-1)$, find the plane through $M_1$ perpendicular to $M_1M_2$

**Solution:**

Since the plane is perpendicular to the line $M_1M_2$, the vector $\vec{M_1M_2}$ can serve as the normal vector $\boldsymbol{n}$ of the plane:

$$\boldsymbol{n} = \vec{M_1M_2} = (4-3, -2-(-1), -1-2) = (1, -1, -3)$$

Moreover, the plane passes through the point $M_1(3,-1,2)$, so the **point–normal form** of the equation of a plane gives:

$$1 \cdot (x - 3) - 1 \cdot (y - (-1)) - 3 \cdot (z - 2) = 0$$

Expanding and simplifying gives the standard equation of the plane:

$$x - 3 - y - 1 - 3z + 6 = 0 \implies x - y - 3z + 2 = 0$$

### 5. Find the angle between each pair of planes: $2x-3y+6z-12=0$ and $x+2y+2z-7=0$

**Solution:**

It is easy to see that the normal vectors of the two planes are respectively:

$$\boldsymbol{n}_1 = (2, -3, 6), \quad \boldsymbol{n}_2 = (1, 2, 2)$$

Let the angle between the two planes be $\theta$ (the angle between two planes usually refers to the acute or right angle, i.e. $\theta \in [0, \frac{\pi}{2}]$). Then:

$$\cos\theta = \frac{|\boldsymbol{n}_1 \cdot \boldsymbol{n}_2|}{\|\boldsymbol{n}_1\| \|\boldsymbol{n}_2\|}$$

Compute the numerator and the denominator separately:

$$\boldsymbol{n}_1 \cdot \boldsymbol{n}_2 = 2 \times 1 + (-3) \times 2 + 6 \times 2 = 2 - 6 + 12 = 8$$

$$\|\boldsymbol{n}_1\| = \sqrt{2^2 + (-3)^2 + 6^2} = \sqrt{4 + 9 + 36} = \sqrt{49} = 7$$

$$\|\boldsymbol{n}_2\| = \sqrt{1^2 + 2^2 + 2^2} = \sqrt{1 + 4 + 4} = \sqrt{9} = 3$$

Substituting into the angle formula gives:

$$\cos\theta = \frac{8}{7 \times 3} = \frac{8}{21}$$

Therefore, the angle between the two planes is:

$$\theta = \arccos\frac{8}{21}$$

### 6. Find the distance between the following two parallel planes: $19x-4y+8z+21=0$ and $19x-4y+8z+42=0$

**Solution:**

By the distance formula between the two parallel planes $Ax+By+Cz+D_1=0$ and $Ax+By+Cz+D_2=0$:

$$d = \frac{|D_1 - D_2|}{\sqrt{A^2 + B^2 + C^2}}$$

In this problem $A=19, B=-4, C=8, D_1=21, D_2=42$; substituting into the formula gives:

$$d = \frac{|21 - 42|}{\sqrt{19^2 + (-4)^2 + 8^2}}$$

Compute the denominator:

$$\sqrt{19^2 + (-4)^2 + 8^2} = \sqrt{361 + 16 + 64} = \sqrt{441} = 21$$

The distance is therefore:

$$d = \frac{|-21|}{21} = \frac{21}{21} = 1$$

### 7. Compute the distance from the point to the plane: $M(1,2,-3)$, $\Pi:5x-3y+z+4=0$

**Solution:**

By the distance formula from a point $(x_0, y_0, z_0)$ to the plane $Ax+By+Cz+D=0$:

$$d = \frac{|Ax_0 + By_0 + Cz_0 + D|}{\sqrt{A^2 + B^2 + C^2}}$$

Substituting the coordinates of the point $M(1,2,-3)$ into the numerator of the formula:

$$\text{numerator} = |5 \times 1 - 3 \times 2 + 1 \times (-3) + 4| = |5 - 6 - 3 + 4| = |0| = 0$$

Compute the denominator (although the numerator is 0, in an exam it is advisable to write out the denominator step to show rigor):

$$\text{denominator} = \sqrt{5^2 + (-3)^2 + 1^2} = \sqrt{35}$$

Therefore, the distance from the point to the plane is:

$$d = \frac{0}{\sqrt{35}} = 0$$

> 💡 **Exam note:** A distance of $0$ means that the point $M$ lies on the plane $\Pi$.

### 8. Find the equations of the following lines

#### (1) The line through the point $(1,0,-2)$ perpendicular to both lines $\frac{x-1}{1} = \frac{y}{1} = \frac{z+1}{-1}$ and $\frac{x}{1} = \frac{y-1}{-1} = \frac{z}{0}$

**Solution:**

The direction vectors of the two given lines are $\boldsymbol{s}_1 = (1, 1, -1)$ and $\boldsymbol{s}_2 = (1, -1, 0)$ respectively.

Since the required line is perpendicular to both of these lines, its direction vector $\boldsymbol{s}$ is perpendicular to $\boldsymbol{s}_1$ and $\boldsymbol{s}_2$.

Use the cross product to find the direction vector $\boldsymbol{s}$:

$$\boldsymbol{s} = \boldsymbol{s}_1 \times \boldsymbol{s}_2 = \begin{vmatrix} \boldsymbol{i} & \boldsymbol{j} & \boldsymbol{k} \\ 1 & 1 & -1 \\ 1 & -1 & 0 \end{vmatrix} = (0 - 1)\boldsymbol{i} - (0 - (-1))\boldsymbol{j} + (-1 - 1)\boldsymbol{k} = -\boldsymbol{i} - \boldsymbol{j} - 2\boldsymbol{k}$$

That is, $\boldsymbol{s} = (-1, -1, -2)$; for ease of writing, we may take the vector pointing in the same direction, $\boldsymbol{s} = (1, 1, 2)$.

The line also passes through the point $(1, 0, -2)$, so the **symmetric form (point-direction form)** of the equation of a line gives:

$$\frac{x-1}{1} = \frac{y}{1} = \frac{z+2}{2}$$

#### (2) The line through the point $A(2,-1,3)$ that intersects the line $\frac{x+3}{7} = \frac{y}{1} = \frac{z+6}{2}$ perpendicularly

**Solution:**

Let the given line be $L_1$, whose direction vector is $\boldsymbol{s}_1 = (7, 1, 2)$.

**Step 1: Set up the coordinates of the intersection point**

Introduce a parameter $t$ and rewrite the line $L_1$ in parametric form, so that the coordinates of an arbitrary point $B$ on $L_1$ (that is, the intersection point of the two lines) are:

$$x = 7t - 3, \quad y = t, \quad z = 2t - 6$$

That is, the intersection point is $B(7t-3, t, 2t-6)$.

**Step 2: Set up an equation using the perpendicularity condition**

The direction vector of the required line can be written as $\vec{AB}$:

$$\vec{AB} = (7t - 3 - 2, t - (-1), 2t - 6 - 3) = (7t - 5, t + 1, 2t - 9)$$

Since the two lines are perpendicular, the dot product of their direction vectors is $0$, i.e. $\vec{AB} \cdot \boldsymbol{s}_1 = 0$:

$$7(7t - 5) + 1(t + 1) + 2(2t - 9) = 0$$

$$49t - 35 + t + 1 + 4t - 18 = 0 \implies 54t - 52 = 0 \implies t = \frac{26}{27}$$

**Step 3: Compute the direction vector of the required line and write down the equation**

Substituting $t = \frac{26}{27}$ into the coordinates of $\vec{AB}$:

$$\vec{AB} = \left(7 \times \frac{26}{27} - 5, \, \frac{26}{27} + 1, \, 2 \times \frac{26}{27} - 9\right) = \left(\frac{47}{27}, \, \frac{53}{27}, \, -\frac{191}{27}\right)$$

Take the direction vector of the line to be $\boldsymbol{s} = (47, 53, -191)$.

The line passes through the point $A(2,-1,3)$, so its symmetric-form equation is:

$$\frac{x-2}{47} = \frac{y+1}{53} = \frac{z-3}{-191}$$

### 9. Find the equations of the following planes

#### (1) The plane through the point $A(2,0,-1)$ that contains the line $\frac{x+1}{2} = \frac{y}{-1} = \frac{z-2}{3}$

**Solution:**

A known point on the given line is $M_0(-1, 0, 2)$, and its direction vector is $\boldsymbol{s} = (2, -1, 3)$.

Since the plane contains this line and passes through the point $A(2, 0, -1)$, we can construct another vector $\vec{M_0A}$ lying in the plane:

$$\vec{M_0A} = (2 - (-1), 0 - 0, -1 - 2) = (3, 0, -3)$$

The normal vector $\boldsymbol{n}$ of the plane must be perpendicular to both the direction vector $\boldsymbol{s}$ of the line and the vector $\vec{M_0A}$:

$$\boldsymbol{n} = \boldsymbol{s} \times \vec{M_0A} = \begin{vmatrix} \boldsymbol{i} & \boldsymbol{j} & \boldsymbol{k} \\ 2 & -1 & 3 \\ 3 & 0 & -3 \end{vmatrix} = (3 - 0)\boldsymbol{i} - (-6 - 9)\boldsymbol{j} + (0 - (-3))\boldsymbol{k} = 3\boldsymbol{i} + 15\boldsymbol{j} + 3\boldsymbol{k}$$

After simplification, take the normal vector $\boldsymbol{n} = (1, 5, 1)$.

Using the point $A(2, 0, -1)$ and the normal vector, write the equation of the plane:

$$1 \cdot (x - 2) + 5 \cdot (y - 0) + 1 \cdot (z - (-1)) = 0$$

Simplifying gives:

$$x + 5y + z - 1 = 0$$

#### (2) The plane containing the line $\frac{x-2}{1} = \frac{y+3}{-5} = \frac{z+1}{-1}$ and parallel to the line $\begin{cases}2x-y+z-3=0 \\ x+2y-z-5=0\end{cases}$

**Solution:**

**Step 1: Find the direction vector $\boldsymbol{s}_2$ of the second given line**

This line is given as the intersection of two planes; its direction vector equals the cross product of the normal vectors of the two planes:

$$\boldsymbol{s}_2 = \begin{vmatrix} \boldsymbol{i} & \boldsymbol{j} & \boldsymbol{k} \\ 2 & -1 & 1 \\ 1 & 2 & -1 \end{vmatrix} = (1 - 2)\boldsymbol{i} - (-2 - 1)\boldsymbol{j} + (4 - (-1))\boldsymbol{k} = -\boldsymbol{i} + 3\boldsymbol{j} + 5\boldsymbol{k} = (-1, 3, 5)$$

**Step 2: Find the normal vector $\boldsymbol{n}$ of the required plane**

The first line lies in the plane; its direction vector is $\boldsymbol{s}_1 = (1, -5, -1)$, and the plane passes through the point $M_1(2, -3, -1)$.

Since the plane is parallel to the second line, the normal vector $\boldsymbol{n}$ of the plane is perpendicular to both $\boldsymbol{s}_1$ and $\boldsymbol{s}_2$:

$$\boldsymbol{n} = \boldsymbol{s}_1 \times \boldsymbol{s}_2 = \begin{vmatrix} \boldsymbol{i} & \boldsymbol{j} & \boldsymbol{k} \\ 1 & -5 & -1 \\ -1 & 3 & 5 \end{vmatrix} = (-25 - (-3))\boldsymbol{i} - (5 - 1)\boldsymbol{j} + (3 - 5)\boldsymbol{k} = -22\boldsymbol{i} - 4\boldsymbol{j} - 2\boldsymbol{k}$$

After simplification, take the normal vector $\boldsymbol{n} = (11, 2, 1)$.

**Step 3: Write down the equation of the plane**

Using the point $M_1(2, -3, -1)$ and the normal vector $\boldsymbol{n} = (11, 2, 1)$, we get:

$$11(x - 2) + 2(y - (-3)) + 1(z - (-1)) = 0$$

$$11x - 22 + 2y + 6 + z + 1 = 0 \implies 11x + 2y + z - 15 = 0$$

### 10. Find the line through the point $A(4,0,-1)$ that intersects both lines $L_1:\begin{cases}x+y+z=1 \\ 2x-y-z=2\end{cases}$ and $L_2:\begin{cases}x-y-z=3 \\ 2x+4y-z=4\end{cases}$

**Solution:**

> 💡 **Exam tip (pencil-of-planes method):** The required line can be viewed as the line of intersection of the "plane $\Pi_1$ that passes through $A$ and contains $L_1$" and the "plane $\Pi_2$ that passes through $A$ and contains $L_2$". Solving this problem with pencil-of-planes equations is the fastest approach and the least error-prone.

**Step 1: Construct the plane $\Pi_1$ that contains $L_1$ and passes through the point $A$**

The pencil-of-planes equation containing $L_1$ is:

$$(x + y + z - 1) + \lambda(2x - y - z - 2) = 0$$

Substitute the point $A(4, 0, -1)$ into this equation to determine $\lambda$:

$$(4 + 0 - 1 - 1) + \lambda(2(4) - 0 - (-1) - 2) = 0$$

$$2 + 7\lambda = 0 \implies \lambda = -\frac{2}{7}$$

Substituting back into the pencil-of-planes equation and simplifying:

$$7(x + y + z - 1) - 2(2x - y - z - 2) = 0 \implies 3x + 9y + 9z - 3 = 0 \implies x + 3y + 3z - 1 = 0 \quad (\Pi_1)$$

**Step 2: Construct the plane $\Pi_2$ that contains $L_2$ and passes through the point $A$**

The pencil-of-planes equation containing $L_2$ is:

$$(x - y - z - 3) + \mu(2x + 4y - z - 4) = 0$$

Substitute the point $A(4, 0, -1)$ into the equation to determine $\mu$:

$$(4 - 0 - (-1) - 3) + \mu(2(4) + 4(0) - (-1) - 4) = 0$$

$$2 + 5\mu = 0 \implies \mu = -\frac{2}{5}$$

Substituting back into the pencil-of-planes equation and simplifying:

$$5(x - y - z - 3) - 2(2x + 4y - z - 4) = 0 \implies x - 13y - 3z - 7 = 0 \quad (\Pi_2)$$

**Step 3: Find the equation of the line**

Combining the two planes gives the general equations of the line:

$$\begin{cases} x + 3y + 3z - 1 = 0 \\ x - 13y - 3z - 7 = 0 \end{cases}$$

If the symmetric form is needed, the direction vector is computed as $\boldsymbol{s} = (15, 3, -8)$; passing through the point $A(4, 0, -1)$, the symmetric form is:

$$\frac{x-4}{15} = \frac{y}{3} = \frac{z+1}{-8}$$

### 11. Find the distance from the point $P(3,-1,2)$ to the line $L:\begin{cases}x+y-z+1=0 \\ 2x-y+z-4=0\end{cases}$

**Solution:**

**Step 1: Find a known point $M_0$ on the line $L$ and the direction vector $\boldsymbol{s}$**

Adding the two equations eliminates $y$ and $z$:

$$3x - 3 = 0 \implies x = 1$$

Substituting into the first equation gives $1 + y - z + 1 = 0 \implies z = y + 2$.

Setting $y = 0$ gives $z = 2$. This yields a point $M_0(1, 0, 2)$ on the line.

The direction vector $\boldsymbol{s}$ of the line is the cross product of the normal vectors of the two planes:

$$\boldsymbol{s} = \begin{vmatrix} \boldsymbol{i} & \boldsymbol{j} & \boldsymbol{k} \\ 1 & 1 & -1 \\ 2 & -1 & 1 \end{vmatrix} = (1 - 1)\boldsymbol{i} - (1 - (-2))\boldsymbol{j} + (-1 - 2)\boldsymbol{k} = -3\boldsymbol{j} - 3\boldsymbol{k}$$

After simplification, take the direction vector $\boldsymbol{s} = (0, 1, 1)$.

**Step 2: Use the vector projection formula to find the distance from the point to the line**

Construct the vector $\vec{M_0P}$, where $P(3, -1, 2)$:

$$\vec{M_0P} = (3 - 1, -1 - 0, 2 - 2) = (2, -1, 0)$$

Compute $\vec{M_0P} \times \boldsymbol{s}$:

$$\vec{M_0P} \times \boldsymbol{s} = \begin{vmatrix} \boldsymbol{i} & \boldsymbol{j} & \boldsymbol{k} \\ 2 & -1 & 0 \\ 0 & 1 & 1 \end{vmatrix} = (-1 - 0)\boldsymbol{i} - (2 - 0)\boldsymbol{j} + (2 - 0)\boldsymbol{k} = -\boldsymbol{i} - 2\boldsymbol{j} + 2\boldsymbol{k} = (-1, -2, 2)$$

The formula for the distance from a point to a line is:

$$d = \frac{\|\vec{M_0P} \times \boldsymbol{s}\|}{\|\boldsymbol{s}\|} = \frac{\sqrt{(-1)^2 + (-2)^2 + 2^2}}{\sqrt{0^2 + 1^2 + 1^2}} = \frac{\sqrt{9}}{\sqrt{2}} = \frac{3}{\sqrt{2}} = \frac{3\sqrt{2}}{2}$$

### 12. Write down the equations of the surfaces of revolution formed by rotating the following curves about the specified axes

#### (1) The circle $x^2+z^2=9$ in the $zOx$ plane rotated about the $z$-axis

**Solution:**

In the $zOx$ plane, the equation of the curve is $x^2+z^2=9, y=0$.

When it is rotated about the $z$-axis, the coordinate along the axis of rotation remains unchanged (here $z$ is unchanged), while the other coordinate $x$ is replaced by $\pm\sqrt{x^2+y^2}$.

Substituting into the original equation gives:

$$\left(\pm\sqrt{x^2+y^2}\right)^2 + z^2 = 9$$

Simplifying gives the required equation of the surface of revolution (a sphere):

$$x^2 + y^2 + z^2 = 9$$

#### (2) The parabola $z^2=2px$ in the $zOx$ plane rotated about its axis of symmetry and about the tangent line through its vertex, respectively

**Solution:**

This parabola lies in the $zOx$ plane, with equation $z^2=2px, y=0$.

-   **Case 1: Rotation about its axis of symmetry**
    
    The axis of symmetry of the parabola $z^2=2px$ is the $x$-axis.
    
    When rotating about the $x$-axis, $x$ remains unchanged and $z$ is replaced by $\pm\sqrt{z^2+y^2}$.
    
    Substituting into the original equation gives:
    
    $$\left(\pm\sqrt{z^2+y^2}\right)^2 = 2px \implies y^2 + z^2 = 2px$$
    
-   **Case 2: Rotation about the tangent line through the vertex**
    
    The vertex of the parabola is $(0,0)$; in the $zOx$ plane, the tangent line through the vertex is the $z$-axis (i.e. $x=0$).
    
    When rotating about the $z$-axis, $z$ remains unchanged and $x$ is replaced by $\pm\sqrt{x^2+y^2}$.
    
    Substituting into the original equation gives:
    
    $$z^2 = 2p\left(\pm\sqrt{x^2+y^2}\right)$$
    
    Squaring both sides to remove the radical gives the polynomial equation:
    
    $$z^4 = 4p^2(x^2 + y^2)$$
    

### 13. Find the equation of the cylinder whose generators are parallel to the $z$-axis and which passes through the curve $\begin{cases}x^2+y^2+4z^2=1 \\ x^2=y^2+z^2\end{cases}$

**Solution:**

By the properties of cylinders, the equation of a cylinder whose generators are parallel to the $z$-axis **does not explicitly contain the variable $z$**. Therefore, it suffices to eliminate the variable $z$ from the given system of equations of the space curve.

The given system of equations is:

$$\begin{cases} x^2+y^2+4z^2=1 & \text{--- (1)} \\ x^2=y^2+z^2 & \text{--- (2)} \end{cases}$$

Rearranging equation (2) gives:

$$z^2 = x^2 - y^2$$

Substituting the equation above into (1) eliminates $z$:

$$x^2 + y^2 + 4(x^2 - y^2) = 1$$

$$x^2 + y^2 + 4x^2 - 4y^2 = 1 \implies 5x^2 - 3y^2 = 1$$

Therefore, the required equation of the cylinder is:

$$5x^2 - 3y^2 = 1$$

### 14. Find the projection equations of the space curve $\begin{cases}x^2+(y-1)^2+(z-1)^2=1 \\ x^2+y^2+z^2=1\end{cases}$ on the three coordinate planes

**Solution:**

> ⚠️ **Common pitfall:** The projection of a space curve onto a coordinate plane is a **planar figure (a curve together with its boundary)**; in analytic geometry it must be expressed as a **system of equations** (the equation of the projecting cylinder joined with the equation of the corresponding coordinate plane), and the range restrictions must be observed!

First expand and simplify the equations of the two spheres:

(1) $x^2 + y^2 - 2y + 1 + z^2 - 2z + 1 = 1 \implies x^2 + y^2 + z^2 - 2y - 2z + 1 = 0$

(2) $x^2 + y^2 + z^2 = 1$

Subtracting the two equations ((2) $-$ (1)) eliminates the quadratic terms and gives the equation of the plane containing the intersection line of the two spheres:

$$2y + 2z - 1 = 1 \implies y + z = 1$$

#### (1) The projection equation on the $xOy$ plane

Eliminate the variable $z$. From $y+z=1 \implies z = 1-y$; substituting into equation (2):

$$x^2 + y^2 + (1-y)^2 = 1 \implies x^2 + 2y^2 - 2y = 0$$

Combining with the equation of the $xOy$ plane, $z=0$, gives the projection equations:

$$\begin{cases} x^2 + 2y^2 - 2y = 0 \\ z = 0 \end{cases}$$

#### (2) The projection equation on the $zOx$ plane

Eliminate the variable $y$. From $y+z=1 \implies y = 1-z$; substituting into equation (2):

$$x^2 + (1-z)^2 + z^2 = 1 \implies x^2 + 2z^2 - 2z = 0$$

Combining with the equation of the $zOx$ plane, $y=0$, gives the projection equations:

$$\begin{cases} x^2 + 2z^2 - 2z = 0 \\ y = 0 \end{cases}$$

#### (3) The projection equation on the $yOz$ plane

Eliminate the variable $x$. Directly use the cylinder equation already obtained (which here happens to degenerate to a plane), $y+z=1$.

Since the original space curve is the intersection line of two spheres (that is, a circle), and the plane $y+z=1$ containing this circle is perpendicular to the $yOz$ plane, its projection onto the $yOz$ plane **degenerates into a line segment**.

We need to determine the range of values of this line segment:

From $x^2 = 1 - y^2 - z^2 \ge 0 \implies y^2 + z^2 \le 1$.

Substituting $z = 1-y$ into this range inequality:

$$y^2 + (1-y)^2 \le 1 \implies 2y^2 - 2y \le 0 \implies 0 \le y \le 1$$

By the same reasoning, $0 \le z \le 1$.

Combining with the equation of the $yOz$ plane, $x=0$, gives the projection equations:

$$\begin{cases} y + z = 1 \\ x = 0 \end{cases} \quad (\text{where } 0 \le y \le 1)$$
