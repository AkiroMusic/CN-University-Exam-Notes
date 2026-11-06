## Chapter 9: Differentiation of Functions of Several Variables and Its Applications — Complete Solutions

### 1. Find each of the following limits

#### (1) $\lim\limits_{(x,y)\to(0,1)} \dfrac{1-xy}{x^2+y^2}$

**Solution:**
Since the function $f(x,y) = \dfrac{1-xy}{x^2+y^2}$ is continuous at the point $(0,1)$, the limit can be found by direct substitution:


$$\lim_{(x,y)\to(0,1)} \dfrac{1-xy}{x^2+y^2} = \dfrac{1 - 0 \times 1}{0^2 + 1^2} = \dfrac{1}{1} = 1$$

#### (2) $\lim\limits_{(x,y)\to(0,0)} \dfrac{2-\sqrt{xy+4}}{xy}$

**Solution:**

> 💡 **Exam tip:** For a $\frac{0}{0}$ limit involving a square root, first consider rationalizing the numerator.

Multiply numerator and denominator by $(2+\sqrt{xy+4})$:


$$\lim_{(x,y)\to(0,0)} \dfrac{(2-\sqrt{xy+4})(2+\sqrt{xy+4})}{xy(2+\sqrt{xy+4})}$$

$$= \lim_{(x,y)\to(0,0)} \dfrac{4 - (xy+4)}{xy(2+\sqrt{xy+4})} = \lim_{(x,y)\to(0,0)} \dfrac{-xy}{xy(2+\sqrt{xy+4})}$$


After canceling the nonzero factor $xy$, substitute to get the limit:


$$= \lim_{(x,y)\to(0,0)} \dfrac{-1}{2+\sqrt{xy+4}} = \dfrac{-1}{2+\sqrt{0+4}} = -\dfrac{1}{4}$$

#### (3) $\lim\limits_{(x,y)\to(0,0)} \dfrac{1-\cos(x^2+y^2)}{(x^2+y^2)e^{x^2y^2}}$

**Solution:**
Using equivalent-infinitesimal substitution: as $(x,y) \to (0,0)$, $x^2+y^2 \to 0$, so $1-\cos(x^2+y^2) \sim \dfrac{1}{2}(x^2+y^2)^2$.
The original limit becomes:


$$\lim_{(x,y)\to(0,0)} \dfrac{\frac{1}{2}(x^2+y^2)^2}{(x^2+y^2)e^{x^2y^2}} = \lim_{(x,y)\to(0,0)} \dfrac{x^2+y^2}{2e^{x^2y^2}}$$


Since the denominator $2e^{x^2y^2} \to 2$ while the numerator $x^2+y^2 \to 0$, the limit is:


$$\dfrac{0}{2} = 0$$

---

### 2. Find the partial derivatives of the following functions

#### (1) $z=\ln\left(\tan\dfrac{x}{y}\right)$

**Solution:**
Differentiate with respect to $x$ (treating $y$ as a constant):


$$\dfrac{\partial z}{\partial x} = \dfrac{1}{\tan\frac{x}{y}} \cdot \sec^2\left(\dfrac{x}{y}\right) \cdot \dfrac{1}{y} = \dfrac{\cos\frac{x}{y}}{\sin\frac{x}{y}} \cdot \dfrac{1}{\cos^2\frac{x}{y}} \cdot \dfrac{1}{y} = \dfrac{1}{y\sin\frac{x}{y}\cos\frac{x}{y}} = \dfrac{2}{y\sin\frac{2x}{y}}$$


Differentiate with respect to $y$ (treating $x$ as a constant):


$$\dfrac{\partial z}{\partial y} = \dfrac{1}{\tan\frac{x}{y}} \cdot \sec^2\left(\dfrac{x}{y}\right) \cdot \left(-\dfrac{x}{y^2}\right) = -\dfrac{x}{y^2\sin\frac{x}{y}\cos\frac{x}{y}} = -\dfrac{2x}{y^2\sin\frac{2x}{y}}$$

#### (2) $u=x^{\frac{y}{z}}$

**Solution:**

> ⚠️ **Common pitfall:** This is a power-exponential function; before differentiating, be sure to rewrite it in exponential form $u = e^{\frac{y}{z}\ln x}$.

$$\dfrac{\partial u}{\partial x} = e^{\frac{y}{z}\ln x} \cdot \left(\dfrac{y}{z} \cdot \dfrac{1}{x}\right) = \dfrac{y}{z}x^{\frac{y}{z}-1}$$

$$\dfrac{\partial u}{\partial y} = e^{\frac{y}{z}\ln x} \cdot \left(\dfrac{1}{z}\ln x\right) = \dfrac{x^{\frac{y}{z}}\ln x}{z}$$

$$\dfrac{\partial u}{\partial z} = e^{\frac{y}{z}\ln x} \cdot \left(-\dfrac{y}{z^2}\ln x\right) = -\dfrac{yx^{\frac{y}{z}}\ln x}{z^2}$$

---

### 3. For $z=y^x$, find $\dfrac{\partial^2 z}{\partial x^2}$, $\dfrac{\partial^2 z}{\partial y^2}$ and $\dfrac{\partial^2 z}{\partial x\partial y}$

**Solution:**
First compute the first-order partial derivatives:


$$\dfrac{\partial z}{\partial x} = y^x \ln y$$

$$\dfrac{\partial z}{\partial y} = x y^{x-1}$$


Then compute the second-order partial derivatives:


$$\dfrac{\partial^2 z}{\partial x^2} = \dfrac{\partial}{\partial x}(y^x \ln y) = y^x (\ln y)^2$$

$$\dfrac{\partial^2 z}{\partial y^2} = \dfrac{\partial}{\partial y}(x y^{x-1}) = x(x-1)y^{x-2}$$

$$\dfrac{\partial^2 z}{\partial x\partial y} = \dfrac{\partial}{\partial y}(y^x \ln y) = x y^{x-1} \ln y + y^x \cdot \dfrac{1}{y} = y^{x-1}(x \ln y + 1)$$

---

### 4. Let $f(x,y,z)=xy^2+yz^2+zx^2$. Find $f_{xx}(0,0,1)$, $f_{xx}(1,0,2)$, $f_{yz}(0,-1,0)$ and $f_{zzx}(2,0,1)$

**Solution:**
First compute the relevant first-order partial derivatives:


$$f_x = y^2 + 2zx$$

$$f_y = 2xy + z^2$$

$$f_z = 2yz + x^2$$

Then compute the higher-order partial derivatives:

1. $f_{xx} = \dfrac{\partial}{\partial x}(y^2 + 2zx) = 2z$
Substituting: $f_{xx}(0,0,1) = 2 \times 1 = 2$; $f_{xx}(1,0,2) = 2 \times 2 = 4$
2. $f_{yz} = \dfrac{\partial}{\partial z}(f_y) = \dfrac{\partial}{\partial z}(2xy + z^2) = 2z$
Substituting: $f_{yz}(0,-1,0) = 2 \times 0 = 0$
3. $f_{zz} = \dfrac{\partial}{\partial z}(f_z) = \dfrac{\partial}{\partial z}(2yz + x^2) = 2y$
$f_{zzx} = \dfrac{\partial}{\partial x}(f_{zz}) = \dfrac{\partial}{\partial x}(2y) = 0$
Substituting: $f_{zzx}(2,0,1) = 0$

---

### 5. Find the total differentials of the following functions

#### (1) $z=\sin(x\cos y)$

**Solution:**
The total differential formula is $dz = \dfrac{\partial z}{\partial x}dx + \dfrac{\partial z}{\partial y}dy$.


$$\dfrac{\partial z}{\partial x} = \cos(x\cos y) \cdot \cos y$$

$$\dfrac{\partial z}{\partial y} = \cos(x\cos y) \cdot (-x\sin y)$$


Hence the total differential is:


$$dz = \cos(x\cos y) \cos y \, dx - x \cos(x\cos y) \sin y \, dy = \cos(x\cos y) (\cos y \, dx - x\sin y \, dy)$$

#### (2) $z=e^{\frac{y}{x}}$

**Solution:**


$$\dfrac{\partial z}{\partial x} = e^{\frac{y}{x}} \cdot \left(-\dfrac{y}{x^2}\right)$$

$$\dfrac{\partial z}{\partial y} = e^{\frac{y}{x}} \cdot \dfrac{1}{x}$$


Hence the total differential is:


$$dz = -\dfrac{y}{x^2}e^{\frac{y}{x}} \, dx + \dfrac{1}{x}e^{\frac{y}{x}} \, dy = \dfrac{e^{\frac{y}{x}}}{x^2}(-y \, dx + x \, dy)$$

---

### 6. Find the total differential of $z=\dfrac{x}{\sqrt{x^2+y^2}}$ at the points $(1,0),(0,1)$

**Solution:**
First compute the partial derivatives:


$$\dfrac{\partial z}{\partial x} = \dfrac{1 \cdot \sqrt{x^2+y^2} - x \cdot \frac{x}{\sqrt{x^2+y^2}}}{x^2+y^2} = \dfrac{x^2+y^2-x^2}{(x^2+y^2)^{\frac{3}{2}}} = \dfrac{y^2}{(x^2+y^2)^{\frac{3}{2}}}$$

$$\dfrac{\partial z}{\partial y} = x \cdot \left(-\dfrac{1}{2}\right)(x^2+y^2)^{-\frac{3}{2}} \cdot 2y = -\dfrac{xy}{(x^2+y^2)^{\frac{3}{2}}}$$

1. **At the point $(1,0)$:**
$\left.\dfrac{\partial z}{\partial x}\right|_{(1,0)} = \dfrac{0}{1} = 0$, $\left.\dfrac{\partial z}{\partial y}\right|_{(1,0)} = -\dfrac{0}{1} = 0$
Hence $dz|_{(1,0)} = 0 \cdot dx + 0 \cdot dy = 0$
2. **At the point $(0,1)$:**
$\left.\dfrac{\partial z}{\partial x}\right|_{(0,1)} = \dfrac{1}{1} = 1$, $\left.\dfrac{\partial z}{\partial y}\right|_{(0,1)} = -\dfrac{0}{1} = 0$
Hence $dz|_{(0,1)} = 1 \cdot dx + 0 \cdot dy = dx$

---

### 7. Let $z=e^{x-2y}$, where $x=\sin t$ and $y=t^3$. Find $\dfrac{dz}{dt}$

**Solution:**
By the chain rule for differentiation of composite functions of several variables:


$$\dfrac{dz}{dt} = \dfrac{\partial z}{\partial x}\dfrac{dx}{dt} + \dfrac{\partial z}{\partial y}\dfrac{dy}{dt}$$


Compute each term separately:


$$\dfrac{\partial z}{\partial x} = e^{x-2y}, \quad \dfrac{dx}{dt} = \cos t$$

$$\dfrac{\partial z}{\partial y} = -2e^{x-2y}, \quad \dfrac{dy}{dt} = 3t^2$$


Substituting into the rule and replacing $x,y$ by their expressions in $t$:


$$\dfrac{dz}{dt} = e^{x-2y}\cos t - 2e^{x-2y}(3t^2) = e^{\sin t - 2t^3}(\cos t - 6t^2)$$

---

### 8. Let $z=(x^2+y^2)^{xy}$. Find $\dfrac{\partial z}{\partial x},\dfrac{\partial z}{\partial y}$

**Solution:**
Use the logarithmic identity to convert the function whose base and exponent both contain variables into exponential form:


$$z = e^{xy \ln(x^2+y^2)}$$


Differentiate with respect to $x$:


$$\dfrac{\partial z}{\partial x} = e^{xy \ln(x^2+y^2)} \cdot \dfrac{\partial}{\partial x}[xy \ln(x^2+y^2)]$$

$$= (x^2+y^2)^{xy} \left[ y \ln(x^2+y^2) + xy \cdot \dfrac{2x}{x^2+y^2} \right] = (x^2+y^2)^{xy} \left[ y \ln(x^2+y^2) + \dfrac{2x^2y}{x^2+y^2} \right]$$


Since in the original function $x$ and $y$ are symmetric, the partial derivative with respect to $y$ is obtained simply by swapping $x$ and $y$ in the expression above:


$$\dfrac{\partial z}{\partial y} = (x^2+y^2)^{xy} \left[ x \ln(x^2+y^2) + \dfrac{2xy^2}{x^2+y^2} \right]$$

---

### 9. Find the first-order partial derivatives of $u=f(x^2-y^2,xy)$

**Solution:**
Let $v = x^2-y^2$, $w = xy$; then $u = f(v, w)$.
Using the chain rule (note that $f_1, f_2$ denote the partial derivatives of $f$ with respect to the first and second intermediate variables respectively):


$$\dfrac{\partial u}{\partial x} = f_1 \cdot \dfrac{\partial v}{\partial x} + f_2 \cdot \dfrac{\partial w}{\partial x} = f_1 \cdot (2x) + f_2 \cdot (y) = 2xf_1 + yf_2$$

$$\dfrac{\partial u}{\partial y} = f_1 \cdot \dfrac{\partial v}{\partial y} + f_2 \cdot \dfrac{\partial w}{\partial y} = f_1 \cdot (-2y) + f_2 \cdot (x) = -2yf_1 + xf_2$$

---

### 10. Let $u=f(x+y+z,x^2+y^2+z^2)$. Find $\Delta u=\dfrac{\partial^2 u}{\partial x^2}+\dfrac{\partial^2 u}{\partial y^2}+\dfrac{\partial^2 u}{\partial z^2}$

**Solution:**
Let the intermediate variables be $v = x+y+z$, $w = x^2+y^2+z^2$.
First differentiate in the $x$ direction:


$$\dfrac{\partial u}{\partial x} = f_1 \cdot 1 + f_2 \cdot 2x$$


Differentiate again (note that $f_1, f_2$ are still functions of $v, w$, so the chain rule must continue to be applied!):


$$\dfrac{\partial^2 u}{\partial x^2} = \dfrac{\partial}{\partial x}(f_1) + 2f_2 + 2x \dfrac{\partial}{\partial x}(f_2)$$

$$= (f_{11}\cdot 1 + f_{12}\cdot 2x) + 2f_2 + 2x(f_{21}\cdot 1 + f_{22}\cdot 2x)$$


Since $f$ has continuous second-order partial derivatives, $f_{12} = f_{21}$; collecting terms gives:


$$\dfrac{\partial^2 u}{\partial x^2} = f_{11} + 4xf_{12} + 4x^2f_{22} + 2f_2$$

By the cyclic symmetry of the function, the following can be written down directly by the same argument:


$$\dfrac{\partial^2 u}{\partial y^2} = f_{11} + 4yf_{12} + 4y^2f_{22} + 2f_2$$

$$\dfrac{\partial^2 u}{\partial z^2} = f_{11} + 4zf_{12} + 4z^2f_{22} + 2f_2$$

Adding the three expressions gives the Laplace operator $\Delta u$:


$$\Delta u = 3f_{11} + 4(x+y+z)f_{12} + 4(x^2+y^2+z^2)f_{22} + 6f_2$$

---

### 11. Let $\sin y + e^x - xy^2 = 0$. Find $\dfrac{dy}{dx}$

**Solution:**
Let $F(x,y) = \sin y + e^x - xy^2$, and use the implicit differentiation formula $\dfrac{dy}{dx} = -\dfrac{F_x}{F_y}$.


$$F_x = e^x - y^2$$

$$F_y = \cos y - 2xy$$


Substituting into the formula gives:


$$\dfrac{dy}{dx} = -\dfrac{e^x - y^2}{\cos y - 2xy} = \dfrac{y^2 - e^x}{\cos y - 2xy}$$

---

### 12. Let $\dfrac{x}{z} = \ln\dfrac{z}{y}$. Find $\dfrac{\partial z}{\partial x}$ and $\dfrac{\partial z}{\partial y}$

**Solution:**
The original equation can be rewritten as $F(x,y,z) = \dfrac{x}{z} - \ln z + \ln y = 0$.
Compute the partial derivatives:


$$F_x = \dfrac{1}{z}$$

$$F_y = \dfrac{1}{y}$$

$$F_z = -\dfrac{x}{z^2} - \dfrac{1}{z} = -\dfrac{x+z}{z^2}$$


By the implicit differentiation formula:


$$\dfrac{\partial z}{\partial x} = -\dfrac{F_x}{F_z} = -\dfrac{\frac{1}{z}}{-\frac{x+z}{z^2}} = \dfrac{z}{x+z}$$

$$\dfrac{\partial z}{\partial y} = -\dfrac{F_y}{F_z} = -\dfrac{\frac{1}{y}}{-\frac{x+z}{z^2}} = \dfrac{z^2}{y(x+z)}$$

---

### 13. Let $e^z - xyz = 0$. Find $\dfrac{\partial^2 z}{\partial x^2}$

**Solution:**

> 💡 **Exam tip (logarithm-first method):** When the equation contains $e^z$ together with an equality of product terms, taking logarithms first and then differentiating implicitly greatly simplifies the computation and avoids complicated derivatives of quotients!

Take logarithms of both sides of the equation (assuming the variables lie in the range where the expressions are meaningful):


$$z = \ln x + \ln y + \ln z$$


Differentiate both sides once with respect to $x$ (note that $z$ is a function of $x,y$):


$$\dfrac{\partial z}{\partial x} = \dfrac{1}{x} + \dfrac{1}{z}\dfrac{\partial z}{\partial x}$$


Rearranging to solve for $\dfrac{\partial z}{\partial x}$:


$$\dfrac{\partial z}{\partial x}\left(1 - \dfrac{1}{z}\right) = \dfrac{1}{x} \implies \dfrac{\partial z}{\partial x}\left(\dfrac{z-1}{z}\right) = \dfrac{1}{x} \implies \dfrac{\partial z}{\partial x} = \dfrac{z}{x(z-1)}$$


Differentiate both sides again with respect to $x$; apply implicit differentiation to the identity $\dfrac{\partial z}{\partial x} - \dfrac{1}{z}\dfrac{\partial z}{\partial x} = \dfrac{1}{x}$:


$$\dfrac{\partial^2 z}{\partial x^2} - \left( -\dfrac{1}{z^2}\left(\dfrac{\partial z}{\partial x}\right)^2 + \dfrac{1}{z}\dfrac{\partial^2 z}{\partial x^2} \right) = -\dfrac{1}{x^2}$$


Collecting terms gives:


$$\dfrac{\partial^2 z}{\partial x^2}\left(\dfrac{z-1}{z}\right) + \dfrac{1}{z^2}\left(\dfrac{z}{x(z-1)}\right)^2 = -\dfrac{1}{x^2}$$

$$\dfrac{\partial^2 z}{\partial x^2}\left(\dfrac{z-1}{z}\right) = -\dfrac{1}{x^2} - \dfrac{1}{x^2(z-1)^2} = -\dfrac{(z-1)^2+1}{x^2(z-1)^2} = -\dfrac{z^2-2z+2}{x^2(z-1)^2}$$


Solving finally gives:


$$\dfrac{\partial^2 z}{\partial x^2} = -\dfrac{z}{z-1} \cdot \dfrac{z^2-2z+2}{x^2(z-1)^3}$$

---

### 14. Find the derivatives or partial derivatives of the functions determined by the following systems of equations

#### (1) Let $\begin{cases} z = x^2 + y^2 \\ x^2 + 2y^2 + 3z^2 = 20 \end{cases}$; find $\dfrac{dy}{dx}$ and $\dfrac{dz}{dx}$

**Solution:**
This is a system of implicit equations in which $y,z$ are regarded as functions of the single variable $x$. Differentiate both equations with respect to $x$ simultaneously:


$$\begin{cases} \dfrac{dz}{dx} = 2x + 2y\dfrac{dy}{dx} \\ 2x + 4y\dfrac{dy}{dx} + 6z\dfrac{dz}{dx} = 0 \implies x + 2y\dfrac{dy}{dx} + 3z\dfrac{dz}{dx} = 0 \end{cases}$$


Substitute the first equation into the second:


$$x + 2y\dfrac{dy}{dx} + 3z\left(2x + 2y\dfrac{dy}{dx}\right) = 0$$

$$(x + 6xz) + (2y + 6yz)\dfrac{dy}{dx} = 0$$


Solving gives:


$$\dfrac{dy}{dx} = -\dfrac{x(1+6z)}{2y(1+3z)}$$


Substituting this back into the first equation to find $\dfrac{dz}{dx}$:


$$\dfrac{dz}{dx} = 2x + 2y\left( -\dfrac{x(1+6z)}{2y(1+3z)} \right) = 2x - \dfrac{x(1+6z)}{1+3z} = \dfrac{2x(1+3z) - x(1+6z)}{1+3z} = \dfrac{x}{1+3z}$$

#### (3) Let $\begin{cases} u = f(ux, v + y) \\ v = g(u - x, v^2y) \end{cases}$; find $\dfrac{\partial u}{\partial x}$ and $\dfrac{\partial v}{\partial x}$

**Solution:**
Differentiate both sides of the system of equations with respect to $x$ simultaneously (note that here $y$ is an independent variable held constant, while $u,v$ are dependent variables):


$$\begin{cases} u_x = f_1 \cdot (u_x x + u \cdot 1) + f_2 \cdot (v_x + 0) \\ v_x = g_1 \cdot (u_x - 1) + g_2 \cdot (2v v_x y) \end{cases}$$


Rearrange into a linear system in the unknowns $u_x, v_x$:


$$\begin{cases} (1 - x f_1) u_x - f_2 v_x = u f_1 \\ -g_1 u_x + (1 - 2vy g_2) v_x = -g_1 \end{cases}$$


Compute the coefficient determinant by Cramer's rule:


$$\Delta = (1 - x f_1)(1 - 2vy g_2) - f_2 g_1$$


Solving gives:


$$\dfrac{\partial u}{\partial x} = \dfrac{u f_1 (1 - 2vy g_2) - f_2 g_1}{\Delta}$$

$$\dfrac{\partial v}{\partial x} = \dfrac{(1 - x f_1)(-g_1) + u f_1 g_1}{\Delta} = \dfrac{g_1(u f_1 + x f_1 - 1)}{\Delta}$$

---

### 15. Find the tangent line and normal plane of the curve $\boldsymbol{r} = (t - \sin t)\boldsymbol{i} + (1 - \cos t)\boldsymbol{j} + \left(4\sin\dfrac{t}{2}\right)\boldsymbol{k}$ at the point corresponding to $t_0 = \dfrac{\pi}{2}$

**Solution:**
**Step 1: Find the coordinates of the point of tangency**
Substitute $t_0 = \dfrac{\pi}{2}$ into the parametric equations:
$x_0 = \dfrac{\pi}{2} - 1$, $y_0 = 1 - 0 = 1$, $z_0 = 4\sin\dfrac{\pi}{4} = 2\sqrt{2}$
The point of tangency is $M_0\left(\dfrac{\pi}{2}-1, 1, 2\sqrt{2}\right)$.

**Step 2: Find the tangent vector**
Differentiate the parametric equations:
$\boldsymbol{r}'(t) = (1 - \cos t)\boldsymbol{i} + (\sin t)\boldsymbol{j} + \left(2\cos\dfrac{t}{2}\right)\boldsymbol{k}$
Substituting $t_0 = \dfrac{\pi}{2}$ gives the tangent vector $\boldsymbol{v}$:
$\boldsymbol{v} = \boldsymbol{r}'\left(\dfrac{\pi}{2}\right) = (1 - 0)\boldsymbol{i} + 1\boldsymbol{j} + 2\cos\dfrac{\pi}{4}\boldsymbol{k} = \{1, 1, \sqrt{2}\}$

**Step 3: Write down the equations**
Equation of the tangent line (symmetric form):


$$\dfrac{x - (\frac{\pi}{2} - 1)}{1} = \dfrac{y - 1}{1} = \dfrac{z - 2\sqrt{2}}{\sqrt{2}}$$


Equation of the normal plane (point–normal form, with the tangent vector as normal vector):


$$1 \cdot \left(x - \dfrac{\pi}{2} + 1\right) + 1 \cdot (y - 1) + \sqrt{2} \cdot (z - 2\sqrt{2}) = 0$$


Expanding and simplifying gives the equation of the normal plane:


$$x + y + \sqrt{2}z - \dfrac{\pi}{2} - 4 = 0$$

---

### 16. Find the tangent line and normal plane of the curve $\begin{cases} x^2 + y^2 + z^2 - 3x = 0 \\ 2x - 3y + 5z - 4 = 0 \end{cases}$ at the point $(1,1,1)$

**Solution:**
The space curve is formed by the intersection of the two surfaces $F(x,y,z)=0$ and $G(x,y,z)=0$. The tangent vector of the curve is the cross product of the normal vectors of the two surfaces at that point.
Let $F = x^2 + y^2 + z^2 - 3x$, $G = 2x - 3y + 5z - 4$.
Compute the partial derivatives and evaluate them at the point $(1,1,1)$:


$$\nabla F = \{2x-3, 2y, 2z\}, \quad \nabla F(1,1,1) = \{-1, 2, 2\}$$

$$\nabla G = \{2, -3, 5\}, \quad \nabla G(1,1,1) = \{2, -3, 5\}$$


The tangent vector $\boldsymbol{v}$ of the curve at the point $(1,1,1)$ is:


$$\boldsymbol{v} = \nabla F \times \nabla G = \begin{vmatrix} \boldsymbol{i} & \boldsymbol{j} & \boldsymbol{k} \\ -1 & 2 & 2 \\ 2 & -3 & 5 \end{vmatrix} = (10 - (-6))\boldsymbol{i} - (-5 - 4)\boldsymbol{j} + (3 - 4)\boldsymbol{k} = \{16, 9, -1\}$$

The equation of the tangent line is:


$$\dfrac{x-1}{16} = \dfrac{y-1}{9} = \dfrac{z-1}{-1}$$


The equation of the normal plane is:


$$16(x-1) + 9(y-1) - 1(z-1) = 0 \implies 16x + 9y - z - 24 = 0$$

---

### 17. Find the equations of the tangent planes to the ellipsoid $x^2 + 2y^2 + z^2 = 1$ that are parallel to the plane $x - y + 2z = 0$

**Solution:**
Let the equation of the ellipsoid be $F(x,y,z) = x^2 + 2y^2 + z^2 - 1 = 0$.
Its normal vector at the point $(x_0, y_0, z_0)$ is $\boldsymbol{n} = \nabla F = \{2x_0, 4y_0, 2z_0\}$.
Since the tangent plane is parallel to the given plane $x - y + 2z = 0$ (whose normal vector is $\boldsymbol{n}_1 = \{1, -1, 2\}$), the two normal vectors must be collinear, i.e. there exists a real number $\lambda \ne 0$ such that $\boldsymbol{n} = \lambda \boldsymbol{n}_1$:


$$\{2x_0, 4y_0, 2z_0\} = \{\lambda, -\lambda, 2\lambda\}$$


This yields the coordinate relations:
$x_0 = \dfrac{\lambda}{2}$, $y_0 = -\dfrac{\lambda}{4}$, $z_0 = \lambda$

Since the point of tangency lies on the ellipsoid, substitute it into the original ellipsoid equation:


$$\left(\dfrac{\lambda}{2}\right)^2 + 2\left(-\dfrac{\lambda}{4}\right)^2 + \lambda^2 = 1$$

$$\dfrac{\lambda^2}{4} + \dfrac{2\lambda^2}{16} + \lambda^2 = 1 \implies \dfrac{11}{8}\lambda^2 = 1 \implies \lambda = \pm \sqrt{\dfrac{8}{11}} = \pm \dfrac{2\sqrt{22}}{11}$$


This gives the coordinates of the two corresponding points of tangency. Using the normal vector $\{1, -1, 2\}$ directly, the equation of the tangent plane is set up as $x - y + 2z = D$.
Substituting the expressions of $x_0, y_0, z_0$ in terms of $\lambda$:
$D = x_0 - y_0 + 2z_0 = \dfrac{\lambda}{2} - \left(-\dfrac{\lambda}{4}\right) + 2\lambda = \dfrac{11}{4}\lambda$
When $\lambda = \dfrac{2\sqrt{22}}{11}$, $D = \dfrac{11}{4} \cdot \dfrac{2\sqrt{22}}{11} = \dfrac{\sqrt{22}}{2}$
When $\lambda = -\dfrac{2\sqrt{22}}{11}$, $D = -\dfrac{\sqrt{22}}{2}$

Hence the required equations of the tangent planes are:


$$x - y + 2z \pm \dfrac{\sqrt{22}}{2} = 0$$

---

### 18. Among the directional derivatives of the function $z=2+ax^2+by^2$ at the point $(3,4)$, the directional derivative along the direction $(-3,-4)$ is the largest, with maximum value $10$. Find $a,b$

**Solution:**
**Key theorem:** The gradient direction of a function at a point is the direction in which the directional derivative at that point is largest, and the magnitude of the gradient is the maximum value of the directional derivative.

Find the gradient of the function at $(3,4)$:
$\nabla z = \{2ax, 2by\}|_{(3,4)} = \{6a, 8b\}$
Since the directional derivative along the vector $\boldsymbol{l} = \{-3, -4\}$ is the largest, the gradient vector $\{6a, 8b\}$ and $\{-3, -4\}$ must be **collinear and point in the same direction**.
That is, there exists a positive constant $k > 0$ such that:


$$\{6a, 8b\} = k\{-3, -4\} \implies 6a = -3k, \; 8b = -4k \implies a = -\dfrac{k}{2}, \; b = -\dfrac{k}{2}$$


Hence necessarily $a = b$, and since $k>0$, we infer $a < 0, b < 0$.

We also know that the magnitude of the gradient equals the maximum directional derivative $10$:


$$\|\nabla z\| = \sqrt{(6a)^2 + (8b)^2} = \sqrt{36a^2 + 64a^2} = \sqrt{100a^2} = 10|a| = 10$$


Solving gives $|a| = 1$.
Combined with the earlier conclusion $a < 0$, we obtain:


$$a = -1, \quad b = -1$$

---

### 19. Find the local extrema of the following functions

#### (1) $z = x^3 - 4x^2 + 2xy - y^2$

**Solution:**
Compute the first-order partial derivatives and set them equal to $0$:


$$\begin{cases} z_x = 3x^2 - 8x + 2y = 0 \\ z_y = 2x - 2y = 0 \implies y = x \end{cases}$$


Substituting $y=x$ into the first equation: $3x^2 - 6x = 0 \implies 3x(x - 2) = 0$.
The stationary points are $M_1(0,0)$ and $M_2(2,2)$.

Compute the second-order partial derivatives:
$A = z_{xx} = 6x - 8$, $B = z_{xy} = 2$, $C = z_{yy} = -2$.

* **At the stationary point $M_1(0,0)$:**
$A = -8, B = 2, C = -2$. $\Delta = AC - B^2 = (-8)(-2) - 2^2 = 12 > 0$.
Since $A < 0$, the function attains a **local maximum** at $(0,0)$, and the local maximum value is $z(0,0) = 0$.
* **At the stationary point $M_2(2,2)$:**
$A = 12 - 8 = 4, B = 2, C = -2$. $\Delta = AC - B^2 = (4)(-2) - 2^2 = -12 < 0$.
Hence this point is not a point of extremum (saddle point).

#### (2) $z = (x^2 + y^2)^2 - 2x^2 + 2y^2$

**Solution:**
Compute the first-order partial derivatives and set them equal to $0$:


$$\begin{cases} z_x = 2(x^2 + y^2)(2x) - 4x = 4x(x^2 + y^2 - 1) = 0 \\ z_y = 2(x^2 + y^2)(2y) + 4y = 4y(x^2 + y^2 + 1) = 0 \end{cases}$$


From the second equation, since $x^2 + y^2 + 1 > 0$ always holds over the real numbers, we can only have $y = 0$.
Substituting $y = 0$ into the first equation gives: $4x(x^2 - 1) = 0 \implies x = 0, \pm 1$.
The three stationary points are $M_1(0,0)$, $M_2(1,0)$, $M_3(-1,0)$.

Compute the second-order partial derivatives:
$z_{xx} = 4(x^2+y^2-1) + 4x(2x) = 12x^2 + 4y^2 - 4$
$z_{xy} = 8xy$
$z_{yy} = 4(x^2+y^2+1) + 4y(2y) = 4x^2 + 12y^2 + 4$

* **At the stationary point $M_1(0,0)$:**
$A = -4, B = 0, C = 4$. $\Delta = AC - B^2 = -16 < 0$, so it is not a point of extremum.
* **At the stationary points $M_2(1,0)$ and $M_3(-1,0)$ (the two points are symmetric in the variables):**
Substituting gives $A = 12 - 4 = 8$, $B = 0$, $C = 4 + 4 = 8$.
$\Delta = AC - B^2 = 64 > 0$.
Since $A = 8 > 0$, the function attains a **local minimum** at $(\pm 1, 0)$.
The local minimum value is: $z(\pm 1, 0) = (1^2 + 0^2)^2 - 2(1^2) + 2(0) = -1$.
