## Chapter 12: Ordinary Differential Equations — Complete Solutions

### 1. Prove that the following function is a solution of the corresponding ordinary differential equation: $y = e^x$ , $e^{-x}\frac{\mathrm{d}y}{\mathrm{d}x} + y^2 - 2ye^x = 1 - e^{2x}$

**Proof:**

Since $y = e^x$, differentiating gives $\frac{\mathrm{d}y}{\mathrm{d}x} = e^x$.

Substituting $y$ and $\frac{\mathrm{d}y}{\mathrm{d}x}$ into the left-hand side (LHS) of the differential equation:

$$\text{LHS} = e^{-x} \cdot (e^x) + (e^x)^2 - 2(e^x) \cdot e^x = 1 + e^{2x} - 2e^{2x} = 1 - e^{2x}$$

The left-hand side equals the right-hand side (RHS), so $y = e^x$ is a solution of this ordinary differential equation.

### 2. Find the general solutions of the following ordinary differential equations

#### (1) $\frac{\mathrm{d}y}{\mathrm{d}x} = x(2y + 1)$

**Solution:** A separable differential equation.

$$\frac{\mathrm{d}y}{2y+1} = x\mathrm{d}x \implies \frac{1}{2}\ln|2y+1| = \frac{1}{2}x^2 + C_1 \implies \ln|2y+1| = x^2 + C_2$$

$$2y+1 = C e^{x^2} \implies y = C e^{x^2} - \frac{1}{2}$$

#### (2) $\frac{\mathrm{d}y}{\mathrm{d}x} = \frac{y}{x} + \sqrt{\left( \frac{y}{x} \right)^2 + 1}$

**Solution:** A homogeneous differential equation. Let $y = ux \implies \frac{\mathrm{d}y}{\mathrm{d}x} = u + x\frac{\mathrm{d}u}{\mathrm{d}x}$.

$$u + x\frac{\mathrm{d}u}{\mathrm{d}x} = u + \sqrt{u^2+1} \implies x\frac{\mathrm{d}u}{\mathrm{d}x} = \sqrt{u^2+1} \implies \frac{\mathrm{d}u}{\sqrt{u^2+1}} = \frac{\mathrm{d}x}{x}$$

Integrating both sides gives: $\ln(u + \sqrt{u^2+1}) = \ln|x| + \ln C \implies u + \sqrt{u^2+1} = Cx$.

Substituting back $u = \frac{y}{x}$: $\frac{y}{x} + \sqrt{\frac{y^2}{x^2}+1} = Cx \implies y + \sqrt{x^2+y^2} = Cx^2$.

#### (3) $\frac{\mathrm{d}y}{\mathrm{d}x} = 3y - 2$

**Solution:**

$$\frac{\mathrm{d}y}{3y-2} = \mathrm{d}x \implies \frac{1}{3}\ln|3y-2| = x + C_1 \implies 3y-2 = C e^{3x} \implies y = C e^{3x} + \frac{2}{3}$$

#### (4) $\frac{\mathrm{d}y}{\mathrm{d}x} = \frac{3y}{x} + \frac{x+1}{x}$

**Solution:** A standard first-order linear nonhomogeneous equation: $\frac{\mathrm{d}y}{\mathrm{d}x} - \frac{3}{x}y = 1 + \frac{1}{x}$.

The integrating factor is $I(x) = e^{\int -\frac{3}{x}\mathrm{d}x} = x^{-3}$. Multiplying both sides by $x^{-3}$:

$$\frac{\mathrm{d}}{\mathrm{d}x}(y x^{-3}) = (1 + \frac{1}{x})x^{-3} = x^{-3} + x^{-4}$$

$$y x^{-3} = \int (x^{-3} + x^{-4})\mathrm{d}x = -\frac{1}{2}x^{-2} - \frac{1}{3}x^{-3} + C \implies y = -\frac{1}{2}x - \frac{1}{3} + Cx^3$$

#### (5) $\frac{\mathrm{d}y}{\mathrm{d}x} = \frac{2y}{x+1} + (x+1)^3$

**Solution:** Rewrite as $\frac{\mathrm{d}y}{\mathrm{d}x} - \frac{2}{x+1}y = (x+1)^3$.

The integrating factor is $I(x) = e^{\int -\frac{2}{x+1}\mathrm{d}x} = (x+1)^{-2}$. Multiplying both sides by $(x+1)^{-2}$:

$$\frac{\mathrm{d}}{\mathrm{d}x}\left[y (x+1)^{-2}\right] = (x+1)^3 \cdot (x+1)^{-2} = x+1$$

$$y (x+1)^{-2} = \int (x+1)\mathrm{d}x = \frac{1}{2}(x+1)^2 + C \implies y = \frac{1}{2}(x+1)^4 + C(x+1)^2$$

### 3. Find the general solutions of the following ordinary differential equations

#### (1) $\frac{\mathrm{d}^2 y}{\mathrm{d}x^2} + \frac{2}{1 - x} \frac{\mathrm{d}y}{\mathrm{d}x} = 0$

**Solution:** A higher-order differential equation that can be reduced in order. Let $p = \frac{\mathrm{d}y}{\mathrm{d}x}$; then $\frac{\mathrm{d}p}{\mathrm{d}x} + \frac{2}{1-x}p = 0$.

$$\frac{\mathrm{d}p}{p} = \frac{2}{x-1}\mathrm{d}x \implies \ln|p| = 2\ln|x-1| + \ln C_1 \implies p = C_1(x-1)^2$$

Since $p = \frac{\mathrm{d}y}{\mathrm{d}x}$, integrate once more:

$$y = \int C_1(x-1)^2 \mathrm{d}x = C_1(x-1)^3 + C_2$$

#### (2) $2\frac{\mathrm{d}y}{\mathrm{d}x} \cdot \frac{\mathrm{d}^2 y}{\mathrm{d}x^2} = 1$

**Solution:** Let $p = \frac{\mathrm{d}y}{\mathrm{d}x}$; the equation becomes $2p \frac{\mathrm{d}p}{\mathrm{d}x} = 1 \implies 2p\mathrm{d}p = \mathrm{d}x$.

Integrating both sides gives: $p^2 = x + C_1 \implies p = \pm \sqrt{x+C_1}$.

That is, $\frac{\mathrm{d}y}{\mathrm{d}x} = \pm \sqrt{x+C_1}$; integrating once more gives the general solution:

$$y = \pm \frac{2}{3}(x+C_1)^{\frac{3}{2}} + C_2$$

### 4. Prove that $y = (c_1 + c_2 x)e^{-2x} + \frac{1}{8}\sin2x$ is the general solution of the equation $\frac{\mathrm{d}^2 y}{\mathrm{d}x^2} + 4\frac{\mathrm{d}y}{\mathrm{d}x} + 4y = \cos2x$

**Proof:**

1.  **Verification of the general solution of the homogeneous equation**: the characteristic equation is $r^2+4r+4=0 \implies (r+2)^2=0$, with repeated roots $r_{1,2}=-2$.
    
    The corresponding general solution of the homogeneous equation is $y_h = (c_1 + c_2 x)e^{-2x}$.
    
2.  **Verification of the particular solution of the nonhomogeneous equation**: let the particular solution be $y_p = \frac{1}{8}\sin2x$. Differentiating:
    
    $$y_p' = \frac{1}{4}\cos2x, \quad y_p'' = -\frac{1}{2}\sin2x$$
    
    Substituting into the left-hand side of the nonhomogeneous equation:
    
    $$\text{LHS} = -\frac{1}{2}\sin2x + 4\left(\frac{1}{4}\cos2x\right) + 4\left(\frac{1}{8}\sin2x\right) = \cos2x = \text{RHS}$$
    
    It satisfies the structure $y = y_h + y_p$ and contains two independent arbitrary constants, which completes the proof.
    

### 5. Prove that $y = c_1 \cos x + c_2 \sin x - \frac{1}{3}x\cos2x + \frac{4}{9}\sin2x$ is the general solution of the equation $\frac{\mathrm{d}^2 y}{\mathrm{d}x^2} + y = x\cos2x$

**Proof:**

1.  **Homogeneous part**: the characteristic equation is $r^2+1=0 \implies r=\pm i$, and the general solution of the homogeneous equation is $y_h = c_1 \cos x + c_2 \sin x$.
    
2.  **Particular solution of the nonhomogeneous equation**: let the particular solution be $y_p = -\frac{1}{3}x\cos2x + \frac{4}{9}\sin2x$. Differentiating:
    
    $$y_p' = -\frac{1}{3}\cos2x + \frac{2}{3}x\sin2x + \frac{8}{9}\cos2x = \frac{5}{9}\cos2x + \frac{2}{3}x\sin2x$$
    
    $$y_p'' = -\frac{10}{9}\sin2x + \frac{2}{3}\sin2x + \frac{4}{3}x\cos2x = -\frac{4}{9}\sin2x + \frac{4}{3}x\cos2x$$
    
    Substituting into the left-hand side of the equation:
    
    $$\text{LHS} = y_p'' + y_p = \left( -\frac{4}{9}\sin2x + \frac{4}{3}x\cos2x \right) + \left( -\frac{1}{3}x\cos2x + \frac{4}{9}\sin2x \right) = x\cos2x = \text{RHS}$$
    
    Since it contains two arbitrary constants and has the complete form, this expression is indeed the general solution of the equation.
    

### 6. Find the general solutions of the following ordinary differential equations

#### (1) $\frac{\mathrm{d}^2 y}{\mathrm{d}x^2} - 3\frac{\mathrm{d}y}{\mathrm{d}x} + 2y = 0$

**Solution:** The characteristic equation is $r^2 - 3r + 2 = 0 \implies (r-1)(r-2) = 0 \implies r_1 = 1, r_2 = 2$.

The general solution is: $y = C_1 e^x + C_2 e^{2x}$.

#### (2) $\frac{\mathrm{d}^2 y}{\mathrm{d}x^2} - 3y = 0$

**Solution:** The characteristic equation is $r^2 - 3 = 0 \implies r = \pm\sqrt{3}$.

The general solution is: $y = C_1 e^{\sqrt{3}x} + C_2 e^{-\sqrt{3}x}$.

#### (3) $\frac{\mathrm{d}^2 y}{\mathrm{d}x^2} + 5\frac{\mathrm{d}y}{\mathrm{d}x} + 4y = x$

**Solution:**

1.  **General solution of the homogeneous equation**: the characteristic equation is $r^2+5r+4=0 \implies r_1=-1, r_2=-4 \implies y_h = C_1 e^{-x} + C_2 e^{-4x}$.
    
2.  **Particular solution of the nonhomogeneous equation**: let the particular solution be $y_p = Ax + B \implies y_p' = A, y_p'' = 0$.
    
    Substituting into the equation: $5A + 4(Ax + B) = x \implies 4Ax + (5A + 4B) = x$.
    
    Equating corresponding coefficients: $4A = 1 \implies A = \frac{1}{4}$; $5A + 4B = 0 \implies B = -\frac{5}{16}$.
    
    The general solution is: $y = C_1 e^{-x} + C_2 e^{-4x} + \frac{1}{4}x - \frac{5}{16}$.
    

#### (4) $\frac{\mathrm{d}^2 y}{\mathrm{d}x^2} + y = 5e^{2x}$

**Solution:**

1.  **General solution of the homogeneous equation**: the characteristic equation is $r^2+1=0 \implies r=\pm i \implies y_h = C_1\cos x + C_2\sin x$.
    
2.  **Particular solution of the nonhomogeneous equation**: let the particular solution be $y_p = Ae^{2x} \implies y_p' = 2Ae^{2x}, y_p'' = 4Ae^{2x}$.
    
    Substituting into the equation: $4Ae^{2x} + Ae^{2x} = 5e^{2x} \implies 5A = 5 \implies A = 1$.
    
    The general solution is: $y = C_1\cos x + C_2\sin x + e^{2x}$.
