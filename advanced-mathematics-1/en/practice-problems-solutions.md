# Advanced Mathematics (Part 1) — Practice Problems: Detailed Solutions

## 1. Limit Computation and Proofs

### 1 Limits of Functions and Sequences

---

### 1

$$\lim_{n\to\infty}\left(\frac{1}{2}+\frac{3}{2^2}+\cdots+\frac{2n-1}{2^n}\right)$$

**Solution** Let

$$S_n=\frac{1}{2}+\frac{3}{2^2}+\cdots+\frac{2n-1}{2^n}$$

Use the shift-and-subtract method: multiply by the common ratio $\dfrac{1}{2}$ and subtract, which gives

$$S_n=3-\frac{2n+3}{2^n}$$

As $n\to\infty$, $\dfrac{2n+3}{2^n}\to 0$, so the limit is $3$.

---

### 2

$$\lim_{n\to\infty}\left(\sqrt{n+2}-2\sqrt{n+1}+\sqrt{n}\right)$$

**Solution** Write it in difference form

$$\sqrt{n+2}-\sqrt{n+1}-\left(\sqrt{n+1}-\sqrt{n}\right)$$

After rationalizing we get

$$\frac{1}{\sqrt{n+2}+\sqrt{n+1}}-\frac{1}{\sqrt{n+1}+\sqrt{n}}$$

After combining over a common denominator, the numerator is $\sqrt{n}-\sqrt{n+2}$ and the denominator is a product of positive terms; using the Lagrange mean value theorem or a Taylor expansion, the limit is $0$.

---

### 3

$$\lim_{x\to 1}\frac{\sqrt{x+8}-3}{\sqrt{x+3}-2}$$

**Solution** Rationalize both the numerator and the denominator. The numerator

$$\sqrt{x+8}-3=\frac{x-1}{\sqrt{x+8}+3}$$

The denominator

$$\sqrt{x+3}-2=\frac{x-1}{\sqrt{x+3}+2}$$

After cancelling $x-1$ we get

$$\frac{\sqrt{x+3}+2}{\sqrt{x+8}+3}\to\frac{2+2}{3+3}=\frac{2}{3}$$

The limit is $\dfrac{2}{3}$.

---

### 4

$$\lim_{x\to+\infty}\frac{(x-1)^2+1-3x}{x^2+2x^3}$$

**Solution** Expanding the numerator

$$(x-1)^2+1-3x=x^2-5x+2$$

The denominator is

$$2x^3+x^2$$

Dividing by the highest power $x^3$:

$$\frac{\dfrac{1}{x}-\dfrac{5}{x^2}+\dfrac{2}{x^3}}{2+\dfrac{1}{x}}\to\frac{0}{2}=0$$

The limit is $0$.

---

### 5

$$\lim_{x\to-\infty}\frac{\sqrt{x^2-1}}{x}$$

**Solution** For $x<0$,

$$\sqrt{x^2-1}=|x|\sqrt{1-\frac{1}{x^2}}=-x\sqrt{1-\frac{1}{x^2}}$$

so

$$\frac{\sqrt{x^2-1}}{x}=-\sqrt{1-\frac{1}{x^2}}\to -1$$

The limit is $-1$.

---

### 6

$$\lim_{x\to 0}\frac{\sin x^2}{1-\cos x}$$

**Solution** Equivalent-infinitesimal substitution

$$\sin x^2\sim x^2$$

$$1-\cos x\sim\frac{1}{2}x^2$$

so

$$\frac{x^2}{\dfrac{1}{2}x^2}=2$$

The limit is $2$.

---

### 7

$$\lim_{x\to 0}\frac{\sin x-\tan x}{x^3}$$

**Solution**

$$\tan x=\frac{\sin x}{\cos x}$$

so

$$\sin x-\tan x=\sin x\left(1-\frac{1}{\cos x}\right)=\frac{\sin x(\cos x-1)}{\cos x}$$

Substituting into the limit

$$\lim_{x\to 0}\frac{\sin x(\cos x-1)}{x^3\cos x}=\lim_{x\to 0}\frac{x\cdot\left(-\frac{1}{2}x^2\right)}{x^3\cdot 1}=-\frac{1}{2}$$

The limit is $-\dfrac{1}{2}$.

---

### 8

$$\lim_{x\to 0}\left(1+2\tan^2 x\right)^{\cot^2 x}$$

**Solution** Let

$$y=\left(1+2\tan^2 x\right)^{\cot^2 x}$$

then

$$\ln y=\cot^2 x\cdot\ln\left(1+2\tan^2 x\right)$$

Let $t=\tan^2 x\to 0$; then

$$\cot^2 x=\frac{1}{t}$$

$$\ln y=\frac{\ln(1+2t)}{t}\to\frac{2t}{t}=2$$

so

$$y\to e^2$$

The limit is $e^2$.

---

### 9

$$\lim_{x\to 0}\frac{\tan x-\sin x}{\sin^3 x}$$

**Solution**

$$\tan x-\sin x=\sin x\left(\frac{1}{\cos x}-1\right)=\frac{\sin x(1-\cos x)}{\cos x}$$

so

$$\frac{\tan x-\sin x}{\sin^3 x}=\frac{1-\cos x}{\cos x\sin^2 x}\sim\frac{\frac{1}{2}x^2}{1\cdot x^2}=\frac{1}{2}$$

The limit is $\dfrac{1}{2}$.

---

### 10

$$\lim_{x\to 0^+}\frac{\int_0^x t\sin t\,dt}{x^2\ln(1+x)}$$

**Solution** L'Hôpital's rule. Differentiating the numerator gives

$$x\sin x$$

Differentiating the denominator gives

$$2x\ln(1+x)+\frac{x^2}{1+x}$$

so

$$\lim_{x\to 0^+}\frac{x\sin x}{2x\ln(1+x)+\frac{x^2}{1+x}}=\lim_{x\to 0^+}\frac{\sin x}{2\ln(1+x)+\frac{x}{1+x}}$$

By equivalent infinitesimals, $\sin x\sim x$ and $\ln(1+x)\sim x$, and the denominator $\sim 2x+x=3x$; the limit is $\dfrac{1}{3}$.

---

### 11

$$\lim_{x\to 0}\frac{\int_0^x \ln(1+t)\,dt}{x\left(e^x-1\right)}$$

**Solution** L'Hôpital's rule. Differentiating the numerator gives

$$\ln(1+x)$$

Differentiating the denominator gives

$$e^x-1+xe^x$$

so

$$\lim_{x\to 0}\frac{\ln(1+x)}{e^x-1+xe^x}$$

By equivalent infinitesimals, $\ln(1+x)\sim x$ and the denominator $\sim x+x=2x$; the limit is $\dfrac{1}{2}$.

---

### 12 Find the following limits

#### 1

$$\lim_{x\to\pi}\frac{1+\cos x}{\tan^2 x}$$

**Solution** Let $t=x-\pi$; then

$$\cos x=-\cos t$$

$$\tan x=\tan t$$

The original expression becomes

$$\frac{1-\cos t}{\tan^2 t}\sim\frac{\frac{1}{2}t^2}{t^2}=\frac{1}{2}$$

The limit is $\dfrac{1}{2}$.

#### 2

$$\lim_{x\to 0}\frac{\tan x-x}{x^2\tan x}$$

**Solution** Taylor expansion

$$\tan x=x+\frac{1}{3}x^3+o(x^3)$$

so

$$\tan x-x\sim\frac{1}{3}x^3$$

$$x^2\tan x\sim x^3$$

The limit is $\dfrac{1}{3}$.

#### 3

$$\lim_{x\to 1}x^{\frac{1}{1-x}}$$

**Solution** Let $t=1-x$; then

$$x^{\frac{1}{1-x}}=(1-t)^{\frac{1}{t}}=\left[(1-t)^{-\frac{1}{t}}\right]^{-1}\to e^{-1}$$

The limit is $\dfrac{1}{e}$.

#### 4

$$\lim_{x\to 0^+}x^{\sin x}$$

**Solution** Take logarithms

$$\ln y=\sin x\ln x\sim x\ln x\to 0$$

so

$$y\to 1$$

The limit is $1$.

#### 5

$$\lim_{x\to 0}\frac{1-x^2-e^{-x^2}}{x^{\sin^3 2x}}$$

**Solution** The denominator

$$x^{\sin^3 2x}$$

Taking the logarithm gives

$$\sin^3 2x\ln x\sim 8x^3\ln x\to 0$$

so the denominator tends to $1$. Taylor-expanding the numerator

$$e^{-x^2}=1-x^2+\frac{1}{2}x^4+o(x^4)$$

therefore

$$1-x^2-e^{-x^2}=-\frac{1}{2}x^4+o(x^4)$$

The limit is $0$.

#### 6

$$\lim_{x\to 0}\left(\frac{1}{x}-\frac{\cos x}{\sin x}\right)\cdot\frac{1}{x}$$

**Solution** Combine over a common denominator

$$\frac{1}{x}-\frac{\cos x}{\sin x}=\frac{\sin x-x\cos x}{x\sin x}$$

The original expression

$$=\frac{\sin x-x\cos x}{x^2\sin x}$$

Taylor expansion

$$\sin x=x-\frac{1}{6}x^3$$

$$\cos x=1-\frac{1}{2}x^2$$

then

$$\sin x-x\cos x=\frac{1}{3}x^3+o(x^3)$$

so the limit is $\dfrac{1}{3}$.

---

### 2 Proof Problems

### 1

$f(x)$ is continuous on $[0,2]$ and $f(0)=f(2)$; prove that there exists at least one point $\xi\in[0,1]$ such that $f(\xi)=f(\xi+1)$.

**Proof** Construct the auxiliary function

$$F(x)=f(x)-f(x+1)$$

$$x\in[0,1]$$

then

$$F(0)=f(0)-f(1)$$

$$F(1)=f(1)-f(2)=f(1)-f(0)=-F(0)$$

If $F(0)=0$, then $\xi=0$ works; otherwise $F(0)$ and $F(1)$ have opposite signs, so by the zero-point theorem there exists $\xi\in(0,1)$ such that

$$F(\xi)=0$$

that is,

$$f(\xi)=f(\xi+1)$$

---

### 2 Proof: when

$x\ge 1$, we have

$$2\arctan x+\arcsin\frac{2x}{1+x^2}=\pi$$

**Proof** Let

$$f(x)=2\arctan x+\arcsin\frac{2x}{1+x^2}$$

Differentiating gives

$$f'(x)=0$$

so $f(x)$ is constant. Computing

$$f(1)=2\cdot\frac{\pi}{4}+\arcsin 1=\frac{\pi}{2}+\frac{\pi}{2}=\pi$$

therefore

$$f(x)\equiv\pi$$

---

### 3 Suppose the function

$f(x)$ is continuous on the closed interval $[0,1]$ and differentiable on the open interval $(0,1)$, with $f(1)=0$. Prove that in the open interval $(0,1)$ there exists at least one point $\xi$ such that

$$f'(\xi)=-\frac{1}{\xi}f(\xi)$$

**Proof** Construct

$$F(x)=xf(x)$$

then

$$F(0)=0$$

$$F(1)=0$$

By Rolle's theorem, there exists $\xi\in(0,1)$ such that

$$F'(\xi)=0$$

that is,

$$\xi f'(\xi)+f(\xi)=0$$

so

$$f'(\xi)=-\frac{1}{\xi}f(\xi)$$

---

### 4 Proof

$$pb^{p-1}(a-b)\le a^p-b^p\le pa^{p-1}(a-b)$$

where $0<b<a$ and $p>1$.

**Proof** Apply the Lagrange mean value theorem to $f(x)=x^p$ on $[b,a]$:

$$a^p-b^p=p\xi^{p-1}(a-b)$$

$$b<\xi<a$$

Since $p>1$, $x^{p-1}$ is increasing, so

$$b^{p-1}<\xi^{p-1}<a^{p-1}$$

Multiplying by the positive number $p(a-b)$ gives the inequality.

---

## 2. Derivatives and Differentials

### 1 For the curve

$$\begin{cases}x=te^{-t}\\y=e^t\end{cases}$$

find the equations of the tangent line and the normal line at the point where $t=0$.

**Solution** When $t=0$, $x=0$ and $y=1$.

$$\frac{dx}{dt}=(1-t)e^{-t}$$

$$\frac{dy}{dt}=e^t$$

$$\frac{dy}{dx}=\frac{e^t}{(1-t)e^{-t}}=\frac{e^{2t}}{1-t}$$

At $t=0$ the slope is $1$. The tangent line is

$$y=x+1$$

The normal line is

$$y=-x+1$$

---

### 2 For the curve

$$y=\ln x$$

find the equation of the tangent line on it that is parallel to the line $y=x$.

**Solution**

$$y'=\frac{1}{x}$$

Setting $\dfrac{1}{x}=1$ gives $x=1$, so the point of tangency is $(1,0)$, and the tangent line is

$$y=x-1$$

---

### 3 Suppose

$$y=e^x\ln x$$

find $y'$.

**Solution** By the product rule

$$y'=e^x\ln x+e^x\cdot\frac{1}{x}=e^x\left(\ln x+\frac{1}{x}\right)$$

---

### 4 Suppose

$$y=\left(\arctan\frac{x}{3}\right)^2$$

find $y'$.

**Solution** By the chain rule

$$y'=2\arctan\frac{x}{3}\cdot\frac{1}{1+\left(\frac{x}{3}\right)^2}\cdot\frac{1}{3}=\frac{6\arctan\frac{x}{3}}{9+x^2}$$

---

### 5 Suppose

$$y=\sin^2 x\cdot\sin(x^2)$$

find $y'$.

**Solution** By the product rule

$$y'=\sin 2x\cdot\sin(x^2)+\sin^2 x\cdot 2x\cos(x^2)$$

---

### 6 Suppose

$$y=\log_2(e^x-1)$$

find $y'$.

**Solution** Change of base

$$y=\frac{\ln(e^x-1)}{\ln 2}$$

$$y'=\frac{1}{\ln 2}\cdot\frac{e^x}{e^x-1}$$

---

### 7 For the astroid

$$x^3+y^3=a^3\ (a>0)$$

find the equation of the tangent line at the point $M\left(\dfrac{\sqrt{2}}{4}a,\dfrac{\sqrt{2}}{4}a\right)$.

**Solution** Implicit differentiation

$$3x^2+3y^2y'=0\Rightarrow y'=-\frac{x^2}{y^2}$$

At $M$ we have $x=y$, so

$$y'=-1$$

The tangent line is

$$x+y=\frac{\sqrt{2}}{2}a$$

---

### 8 Suppose the function

$$y=\arctan\frac{1}{x}$$

find $dy$ and $dy\big|_{x=1}$.

**Solution**

$$y'=-\frac{1}{1+x^2}$$

so

$$dy=-\frac{1}{1+x^2}dx$$

$$dy\big|_{x=1}=-\frac{1}{2}dx$$

---

### 9 Suppose

$$y=y(x)$$

is determined by the equation

$$2xy=x+y$$

find $dy\big|_{x=0}$.

**Solution** Differentiate both sides

$$2(y\,dx+x\,dy)=dx+dy$$

Rearranging gives

$$(2x-1)dy=(1-2y)dx$$

so

$$dy=\frac{1-2y}{2x-1}dx$$

When $x=0$, the original equation gives $y=0$, so

$$dy\big|_{x=0}=-dx$$

---

### 10 Given

$$y=\ln^2(1-x)$$

find $dy$.

**Solution**

$$y'=-\frac{2\ln(1-x)}{1-x}$$

$$dy=-\frac{2\ln(1-x)}{1-x}dx$$

---

### 11 Given

$$y=\int_0^x \tan t^2\,dt$$

find $y'$.

**Solution** By the Fundamental Theorem of Calculus

$$y'=\tan x^2$$

---

## 3. Indefinite and Definite Integrals

### 1 Computing Indefinite Integrals

#### 1

$$\int\left(1-\sqrt[3]{x^2}\right)^2 dx$$

**Solution**

$$\sqrt[3]{x^2}=x^{2/3}$$

Expanding

$$\left(1-x^{2/3}\right)^2=1-2x^{2/3}+x^{4/3}$$

Integrating gives

$$x-\frac{6}{5}x^{5/3}+\frac{3}{7}x^{7/3}+C$$

---

#### 2

$$\int\frac{1}{\cos^2 x\sin^2 x}dx$$

**Solution**

$$\frac{1}{\cos^2 x\sin^2 x}=\sec^2 x+\csc^2 x$$

Integrating gives

$$\tan x-\cot x+C$$

---

#### 3

$$\int\frac{1}{4x^2+a^2}dx$$

**Solution**

$$\int\frac{1}{4x^2+a^2}dx=\frac{1}{2a}\arctan\frac{2x}{a}+C$$

---

#### 4

$$\int x^2e^{-x^3}dx$$

**Solution** Let

$$u=-x^3$$

then

$$\int x^2e^{-x^3}dx=-\frac{1}{3}e^{-x^3}+C$$

---

#### 5

$$\int\frac{e^{2x}}{1+e^x}dx$$

**Solution** Let

$$u=e^x$$

then

$$\int\frac{e^{2x}}{1+e^x}dx=e^x-\ln(1+e^x)+C$$

---

#### 6

$$\int\sqrt{a^2-x^2}\,dx\quad(a>0)$$

**Solution** Let

$$x=a\sin t$$

then

$$\int\sqrt{a^2-x^2}\,dx=\frac{a^2}{2}\arcsin\frac{x}{a}+\frac{x}{2}\sqrt{a^2-x^2}+C$$

---

#### 7

$$\int xe^x dx$$

**Solution** Integration by parts

$$\int xe^x dx=e^x(x-1)+C$$

---

#### 8

$$\int x\ln x\,dx$$

**Solution** Integration by parts

$$\int x\ln x\,dx=\frac{x^2}{2}\ln x-\frac{x^2}{4}+C$$

---

#### 9

$$\int\sec^3 x\,dx$$

**Solution** Integration by parts gives

$$\int\sec^3 x\,dx=\frac{1}{2}\left(\sec x\tan x+\ln|\sec x+\tan x|\right)+C$$

---

### 2 Computing Definite Integrals

#### 1

$$\int_0^{\pi}\sqrt{1+\cos 2x}\,dx$$

**Solution**

$$\sqrt{1+\cos 2x}=\sqrt{2}|\cos x|$$

Integrating piecewise gives

$$2\sqrt{2}$$

---

#### 2

$$\int_0^{2\pi}|\sin x|\,dx$$

**Solution** Using symmetry

$$\int_0^{2\pi}|\sin x|\,dx=2\int_0^{\pi}\sin x\,dx=4$$

---

#### 3

$$\int_{-1}^{3}\frac{dt}{1+t^2}$$

**Solution**

$$\int_{-1}^{3}\frac{dt}{1+t^2}=\arctan 3+\frac{\pi}{4}$$

---

#### 4

$$\int_e^e|\ln x|\,dx$$

**Solution** The interval of integration has length $0$, so the integral is $0$.

---

#### 5

$$\int_0^{\pi^2}\sqrt{x}\cos\sqrt{x}\,dx$$

**Solution** Let

$$t=\sqrt{x}$$

then

$$\int_0^{\pi^2}\sqrt{x}\cos\sqrt{x}\,dx=2\int_0^{\pi}t^2\cos t\,dt=-4\pi$$

---

#### 6

$$\int_0^{\pi/2}e^x\cos x\,dx$$

**Solution** Integrating by parts twice gives

$$\int_0^{\pi/2}e^x\cos x\,dx=\frac{1}{2}\left(e^{\pi/2}-1\right)$$

---

## 4. Applications of Integration: Area, Volume, Arc Length

### 1 Region enclosed by the parabola

$$y^2=2x$$

and the line

$$y=x-4$$

Compute the area of the enclosed region.

**Solution** The intersection points are $(2,-2)$ and $(8,4)$. Integrating with respect to $y$

$$S=\int_{-2}^{4}\left(y+4-\frac{y^2}{2}\right)dy=18$$

---

### 2 Region enclosed by the ellipse

$$\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$$

Compute the volume of the solid of revolution obtained by revolving the enclosed region one full turn about the $x$-axis.

**Solution**

$$V=\pi\int_{-a}^{a}y^2\,dx=\frac{4}{3}\pi ab^2$$

---

### 3 A plane passes through the center of the base circle

of a cylinder of base radius $R$, and makes an angle $\alpha$ with the base plane; compute the volume of the solid cut from the cylinder by this plane.

**Solution** Take the plane

$$z=x\tan\alpha$$

The solid lies in the part $x\ge 0$, and the cross-sectional area is

$$2\sqrt{R^2-x^2}\cdot x\tan\alpha$$

Integrating gives

$$V=\frac{2}{3}R^3\tan\alpha$$

---

### 4 The cardioid

$$\rho=a(1+\cos\theta)\ (a>0)$$

Compute the area of the region it encloses.

**Solution**

$$A=\frac{1}{2}\int_0^{2\pi}a^2(1+\cos\theta)^2\,d\theta=\frac{3}{2}\pi a^2$$

---

### 5 The cardioid

$$\rho=a(1+\cos\theta)\ (a>0)$$

Find its arc length.

**Solution**

$$L=\int_0^{2\pi}\sqrt{\rho^2+(\rho')^2}\,d\theta=8a$$

---

### 6 The equations of the cycloid are

$$\begin{cases}x=a(t-\sin t)\\y=a(1-\cos t)\end{cases}\quad(a>0)\quad(0\le t\le 2\pi)$$

#### 1 Find the area of the region enclosed by one arch of the cycloid and the

$x$-axis.

**Solution**

$$A=\int_0^{2\pi}yx'\,dt=a^2\int_0^{2\pi}(1-\cos t)^2\,dt=3\pi a^2$$

#### 2 For the region enclosed by one arch of the cycloid and the

$x$-axis, find the volumes of the solids obtained by revolving it one full turn about the $x$-axis and the $y$-axis, respectively.

**Solution** About the $x$-axis

$$V_x=\pi\int_0^{2\pi}y^2x'\,dt=5\pi^2a^3$$

About the $y$-axis

$$V_y=2\pi\int_0^{2\pi}xyx'\,dt=6\pi^3a^3$$

#### 3 Find the length of one arch of the cycloid

**Solution**

$$L=\int_0^{2\pi}\sqrt{x'^2+y'^2}\,dt=8a$$

---

## 5. Taylor's Formula and the Behavior of Functions

### 1 For the function

$$f(x)=\sin x$$

find its $n$th-order Maclaurin formula with the Lagrange remainder.

**Solution**

$$\sin x=\sum_{k=0}^{m-1}(-1)^k\frac{x^{2k+1}}{(2k+1)!}+R_n(x)$$

where

$$R_n(x)=\frac{\sin^{(n+1)}(\theta x)}{(n+1)!}x^{n+1}$$

$$\theta\in(0,1)$$

---

### 2 For the function

$$f(x)=e^x$$

find its $n$th-order Maclaurin formula with the Lagrange remainder.

**Solution**

$$e^x=\sum_{k=0}^{n}\frac{x^k}{k!}+R_n(x)$$

$$R_n(x)=\frac{e^{\xi}}{(n+1)!}x^{n+1}$$

$$\xi\in(0,x)$$

---

### 3 For

$$y=\ln(1+x^2)$$

find the intervals of concavity and the inflection points.

**Solution**

$$y'=\frac{2x}{1+x^2}$$

$$y''=\frac{2(1-x^2)}{(1+x^2)^2}$$

Setting $y''=0$ gives

$$x=\pm 1$$

Concave interval

$$(-1,1)$$

Convex interval

$$(-\infty,-1)\cup(1,+\infty)$$

Inflection points

$$(\pm 1,\ln 2)$$

---

## 6. Power Series

### 1 Find the radius of convergence, open interval of convergence, and interval of convergence of the following power series

#### 1

$$\sum_{n=1}^{\infty}\frac{x^n}{2^n n}$$

**Solution** Radius of convergence

$$R=2$$

Open interval of convergence

$$(-2,2)$$

Interval of convergence

$$[-2,2)$$

---

#### 2

$$\sum_{n=1}^{\infty}(\sqrt{n+1}-\sqrt{n})(x-2)^n$$

**Solution** Radius of convergence

$$R=1$$

Open interval of convergence

$$(1,3)$$

Interval of convergence

$$[1,3)$$

---

#### 3

$$\sum_{n=1}^{\infty}\frac{3^n+(-2)^n}{n}x^n$$

**Solution** Radius of convergence

$$R=\frac{1}{3}$$

Open interval of convergence

$$\left(-\frac{1}{3},\frac{1}{3}\right)$$

Interval of convergence

$$\left[-\frac{1}{3},\frac{1}{3}\right)$$

---

### 2 For the power series

$$\sum_{n=1}^{\infty}\frac{x^{n+1}}{n}$$

find the sum function, and for the series

$$\sum_{n=1}^{\infty}\frac{1}{n\cdot 2^n}$$

find the sum.

**Solution** The sum function

$$S(x)=-x\ln(1-x)$$

$$|x|<1$$

Let

$$x=\frac{1}{2}$$

which gives

$$\sum_{n=1}^{\infty}\frac{1}{n\cdot 2^n}=\ln 2$$

---

### 3 For the power series

$$\sum_{n=1}^{\infty}nx^n$$

find the sum function, and use it for the numerical series

$$\sum_{n=1}^{\infty}\frac{n}{2^n}$$

to find its sum.

**Solution** The sum function

$$S(x)=\frac{x}{(1-x)^2}$$

$$|x|<1$$

Let

$$x=\frac{1}{2}$$

which gives

$$\sum_{n=1}^{\infty}\frac{n}{2^n}=2$$

---

### 4 For

$$\sum_{n=1}^{\infty}\frac{x^n}{n(n+1)}$$

find the sum function.

**Solution** Decompose

$$\frac{1}{n(n+1)}=\frac{1}{n}-\frac{1}{n+1}$$

which gives the sum function

$$S(x)=1+\frac{(1-x)\ln(1-x)}{x}$$

$$|x|<1,\ x\ne 0$$

$$S(0)=0$$
