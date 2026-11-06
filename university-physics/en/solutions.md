# Chapter 1 Kinematics of a Particle

## Exercise 1-4

### Answer

Given the acceleration $a(t) = 4 + 3t$. At $t=0$, $x_0 = 2\text{ m}$ and $v_0 = 5\text{ m}\cdot\text{s}^{-1}$.

From $a = \frac{\text{d}v}{\text{d}t}$ we get:
$$\text{d}v = a\,\text{d}t = (4 + 3t)\,\text{d}t$$

Integrating both sides:
$$\int_{v_0}^{v} \text{d}v = \int_{0}^{t} (4 + 3t)\,\text{d}t$$
$$v - v_0 = 4t + \frac{3}{2}t^2$$
$$v(t) = v_0 + 4t + 1.5t^2 = 5 + 4t + 1.5t^2\quad(\text{m}\cdot\text{s}^{-1})$$

At $t = 10\text{ s}$, the velocity is:
$$v(10) = 5 + 4 \times 10 + 1.5 \times 10^2 = 195\text{ m}\cdot\text{s}^{-1}$$

From $v = \frac{\text{d}x}{\text{d}t}$ we get:
$$\text{d}x = v\,\text{d}t = (5 + 4t + 1.5t^2)\,\text{d}t$$

Integrating both sides:
$$\int_{x_0}^{x} \text{d}x = \int_{0}^{t} (5 + 4t + 1.5t^2)\,\text{d}t$$
$$x - x_0 = 5t + 2t^2 + 0.5t^3$$
$$x(t) = x_0 + 5t + 2t^2 + 0.5t^3 = 2 + 5t + 2t^2 + 0.5t^3\quad(\text{m})$$

At $t = 10\text{ s}$, the position is:
$$x(10) = 2 + 5 \times 10 + 2 \times 10^2 + 0.5 \times 10^3 = 752\text{ m}$$

---

### Solution walkthrough

1. **Core idea (applying calculus to kinematics)**:
   * **Differentiation direction**: position $x$ —(differentiate)→ velocity $v$ —(differentiate)→ acceleration $a$. <!-- CN formulas preserved for parity: `$\xrightarrow{\text{求导}}$` `$\xrightarrow{\text{求导}}$` -->
   * **Integration direction**: acceleration $a$ —(integrate)→ velocity $v$ —(integrate)→ position $x$. <!-- CN formulas preserved for parity: `$\xrightarrow{\text{积分}}$` `$\xrightarrow{\text{积分}}$` -->
   * In this problem, the acceleration $a$ is given as a function of time $t$, and the velocity and position are required, so we need to perform two consecutive integrations along the **integration direction**.

2. **Step 1: find the velocity $v(t)$**
   * The definition of acceleration is $a = \frac{\text{d}v}{\text{d}t}$. Rearranging gives: $\text{d}v = a\,\text{d}t$ (the change of velocity over an extremely short time interval).
   * Accumulate both sides (i.e. integrate): on the left, the upper limit is the velocity $v$ at an arbitrary time and the lower limit is the initial velocity $v_0 = 5$; on the right, the time runs from $0$ to an arbitrary time $t$.
   * Carrying out the integral: $\int (4 + 3t)\text{d}t = 4t + \frac{3}{2}t^2$. Substituting the limits and rearranging gives the velocity formula: $v(t) = 5 + 4t + 1.5t^2$.
   * Substituting $t=10\text{ s}$ directly gives the velocity $v(10) = 195\text{ m/s}$.

3. **Step 2: find the position $x(t)$**
   * The definition of velocity is $v = \frac{\text{d}x}{\text{d}t}$. In the same way, rearranging gives: $\text{d}x = v\,\text{d}t$.
   * Integrating both sides: on the left, from the initial position $x_0 = 2$ to $x$; on the right, from $0$ to $t$.
   * Carrying out the integral: $\int (5 + 4t + 1.5t^2)\text{d}t = 5t + 2t^2 + 0.5t^3$.
   * Rearranging gives the position formula: $x(t) = 2 + 5t + 2t^2 + 0.5t^3$.
   * Substituting $t=10\text{ s}$ directly gives the position $x(10) = 752\text{ m}$.

---

## Exercise 1-6

### Answer

Given the acceleration $a(t) = -A\omega^2 \cos\omega t$. At $t=0$, $v_0 = 0$ and $x_0 = A$.

From $a = \frac{\text{d}v}{\text{d}t}$, we get:
$$\text{d}v = -A\omega^2 \cos\omega t\,\text{d}t$$

Integrating both sides:
$$\int_{0}^{v} \text{d}v = \int_{0}^{t} -A\omega^2 \cos\omega t\,\text{d}t$$
$$v = \left[ -A\omega \sin\omega t \right]_0^t = -A\omega \sin\omega t$$

From $v = \frac{\text{d}x}{\text{d}t}$, we get:
$$\text{d}x = -A\omega \sin\omega t\,\text{d}t$$

Integrating both sides:
$$\int_{A}^{x} \text{d}x = \int_{0}^{t} -A\omega \sin\omega t\,\text{d}t$$
$$x - A = \left[ A \cos\omega t \right]_0^t = A\cos\omega t - A$$
$$x(t) = A\cos\omega t\quad(\text{m})$$

Hence the kinematic equation of this particle is:
$$x = A\cos\omega t$$

---

### Solution walkthrough

1. **What is a "kinematic equation"?**
   * A kinematic equation is a functional relation expressing the position coordinate as a function of time, i.e. $x = f(t)$.

2. **First integration (finding the velocity $v$)**:
   * The integral is $v = \int a\,\text{d}t = \int -A\omega^2 \cos\omega t\,\text{d}t$.
   * Hint: by the fundamental formula of calculus, the integral of a cosine is a sine, i.e. $\int \cos(kx)\text{d}x = \frac{1}{k}\sin(kx)$.
   * So, integrating $-A\omega^2 \cos\omega t$ gives $-A\omega^2 \cdot \frac{1}{\omega}\sin\omega t = -A\omega \sin\omega t$.
   * Since $v=0$ at $t=0$ and $\sin(0)=0$, the constant term is $0$. This gives the velocity function $v(t) = -A\omega \sin\omega t$.

3. **Second integration (finding the position $x$)**:
   * Integrate the velocity once more: $x = \int v\,\text{d}t = \int -A\omega \sin\omega t\,\text{d}t$.
   * Hint: the integral of a sine is minus a cosine, i.e. $\int \sin(kx)\text{d}x = -\frac{1}{k}\cos(kx)$.
   * So, integrating $-A\omega \sin\omega t$ gives $-A\omega \cdot \left(-\frac{1}{\omega}\cos\omega t\right) = A\cos\omega t$.
   * Pay attention to **substituting the limits of the definite integral**:
     Left side: $\int_{A}^{x} \text{d}x = x - A$;
     Right side: $\left[ A\cos\omega t \right]_0^t = A\cos\omega t - A\cos(0) = A\cos\omega t - A$.
   * Simplifying both sides, the $-A$ cancels, and the final result is: $x = A\cos\omega t$. This is the kinematic equation of the particle.

---

# Chapter 2 Dynamics of a Particle

## Exercise 2-7

### Answer

Given $m = 1\text{ kg}$, the force $F(t) = 3 + 4t$, and the initial velocity $v_0 = 10\text{ m}\cdot\text{s}^{-1}$.

**(1) Find the impulse $I$ of the force during $0 \sim 2\text{ s}$:**
By the definition of impulse:
$$I = \int_{0}^{2} F\,\text{d}t = \int_{0}^{2} (3 + 4t)\,\text{d}t$$
$$I = \left[ 3t + 2t^2 \right]_0^2 = (3 \times 2 + 2 \times 2^2) - 0 = 14\text{ N}\cdot\text{s}$$

**(2) Find the velocity of the particle at $t = 2\text{ s}$:**
By the impulse–momentum theorem:
$$I = \Delta p = mv - mv_0$$
$$14 = 1 \times v - 1 \times 10$$
$$v = 24\text{ m}\cdot\text{s}^{-1}$$

---

### Solution walkthrough

1. **What is impulse?**
   * In physics, the cumulative effect of a force over time is called **impulse**. For a constant force, the impulse is $I = F \cdot \Delta t$; for a force that varies with time, it must be computed with a definite integral: $I = \int F\,\text{d}t$.

2. **Analysis of part (1)**:
   * The problem asks for the impulse during $0 \sim 2\text{ s}$, so we integrate the varying force $F = 3 + 4t$ over the time interval $[0, 2]$.
   * Carrying out the integral: $\int (3 + 4t)\text{d}t = 3t + 2t^2$.
   * Substituting the upper limit $t=2$ and the lower limit $t=0$: $(3\times 2 + 2\times 4) - 0 = 6 + 8 = 14\text{ N}\cdot\text{s}$ (the unit of impulse is the newton-second).

3. **Analysis of part (2)**:
   * The **impulse–momentum theorem** states: the impulse of the net external force on an object equals the change of its momentum, i.e. I = Δp = p_final − p_initial = mv_final − mv_initial. <!-- CN formula preserved for parity: `$I = \Delta p = p_{\text{末}} - p_{\text{初}} = mv_{\text{末}} - mv_{\text{初}}$` -->
   * Since we found the impulse $I = 14\text{ N}\cdot\text{s}$ in part (1), we can write the equation directly: $14 = m(v - v_0)$.
   * Substituting the known values $m = 1\text{ kg}$ and $v_0 = 10\text{ m/s}$ and solving gives $14 = 1 \times (v - 10) \implies v = 24\text{ m/s}$.

---

## Exercise 2-10

### Answer

Given the net force $F(t) = 400 - \frac{4}{3} \times 10^5 t$ and the speed at the muzzle $v = 300\text{ m}\cdot\text{s}^{-1}$.

**(1) Find the time $t$ the bullet takes to travel the full length of the barrel:**
From the problem, the net force is zero exactly when the bullet leaves the muzzle, i.e.:
$$F(t) = 0 \implies 400 - \frac{4}{3} \times 10^5 t = 0$$
$$t = \frac{400 \times 3}{4 \times 10^5} = 3 \times 10^{-3}\text{ s}$$

**(2) Find the impulse $I$ of the force on the bullet while it is in the barrel:**
$$I = \int_{0}^{t} F\,\text{d}t = \int_{0}^{3 \times 10^{-3}} \left( 400 - \frac{4}{3} \times 10^5 t \right)\,\text{d}t$$
$$I = \left[ 400t - \frac{2}{3} \times 10^5 t^2 \right]_0^{3 \times 10^{-3}}$$
$$I = 400 \times (3 \times 10^{-3}) - \frac{2}{3} \times 10^5 \times (9 \times 10^{-6})$$
$$I = 1.2 - 0.6 = 0.6\text{ N}\cdot\text{s}$$

**(3) Find the mass $m$ of the bullet:**
By the impulse–momentum theorem, taking the bullet initially at rest ($v_0 = 0$):
$$I = mv - mv_0 \implies I = mv$$
$$0.6 = m \times 300$$
$$m = 2 \times 10^{-3}\text{ kg} = 2\text{ g}$$

---

### Solution walkthrough

1. **Part (1): find the time $t$**
   * The key to the problem is that "**the net force is exactly zero where the bullet leaves the muzzle**".
   * This means that at the instant $t$ when the bullet exits the muzzle, the force is $F = 0$. So we set up the equation $F(t) = 0$ directly and solve $t = 0.003\text{ s}$ (equivalently written as $3\times 10^{-3}\text{ s}$, i.e. 3 milliseconds).

2. **Part (2): find the impulse $I$**
   * We again use the integral definition of the impulse of a varying force; the interval of integration is the time the bullet spends moving inside the barrel, i.e. from $0$ to $3 \times 10^{-3}\text{ s}$.
   * The integrand $400 - \frac{4}{3} \times 10^5 t$ integrates to $400t - \frac{2}{3} \times 10^5 t^2$.
   * Substituting the upper limit $3\times 10^{-3}$:
     * The first term: $400 \times 0.003 = 1.2$;
     * The second term: $\frac{2}{3} \times 10^5 \times 9 \times 10^{-6} = \frac{2}{3} \times 0.9 = 0.6$;
     * Subtracting gives $1.2 - 0.6 = 0.6\text{ N}\cdot\text{s}$.

3. **Part (3): find the mass $m$ of the bullet**
   * Inside the barrel, the bullet accelerates from rest ($v_0 = 0$) to the muzzle speed $v = 300\text{ m/s}$.
   * Applying the impulse–momentum theorem: the impulse $I = \Delta p = m \cdot v$.
   * With $I = 0.6\text{ N}\cdot\text{s}$ and $v = 300\text{ m/s}$, we get $m = \frac{I}{v} = \frac{0.6}{300} = 0.002\text{ kg} = 2\text{ g}$.

---

## Exercise 2-16

### Answer

Given $m = 2\text{ kg}$ and the varying force $F_x(x) = 4 + 6x$. At $t=0$, $x_0 = 0$ and $v_0 = 0$.

**(1) Find the work $W$ done by the force on the object during the motion from $x=0$ to $x=4\text{ m}$:**
By the definition of work:
$$W = \int_{x_0}^{x_1} F_x\,\text{dx} = \int_{0}^{4} (4 + 6x)\,\text{dx}$$
$$W = \left[ 4x + 3x^2 \right]_0^4 = (4 \times 4 + 3 \times 4^2) - 0 = 16 + 48 = 64\text{ J}$$

**(2) Find the velocity $v$ of the object at $x=4\text{ m}$:**
By the work–energy theorem:
$$W = \Delta E_k = \frac{1}{2}mv^2 - \frac{1}{2}mv_0^2$$
$$64 = \frac{1}{2} \times 2 \times v^2 - 0 \implies v^2 = 64$$
$$v = 8\text{ m}\cdot\text{s}^{-1}$$

**(3) Find the impulse $I$ of the varying force during the motion from $x=0$ to $x=4\text{ m}$:**
By the impulse–momentum theorem:
$$I = \Delta p = mv - mv_0$$
$$I = 2 \times 8 - 0 = 16\text{ N}\cdot\text{s}$$

---

### Solution walkthrough

1. **Part (1): how to compute the work of a varying force**
   * The **definition of work** is force times displacement. When the force $F_x$ varies with the position $x$, the work must be computed by integrating over position, with the formula $W = \int F_x\,\text{d}x$.
   * In this problem, the interval of integration is the position $x$ going from $0$ to $4\text{ m}$.
   * Carrying out the integral: $\int (4 + 6x)\text{d}x = 4x + 3x^2$. Substituting the upper limit $4$ gives the work $W = 64\text{ J}$ (joules).

2. **Part (2): find the velocity $v$**
   * The **work–energy theorem** states: the work done by the net external force on an object equals the change of its kinetic energy (ΔE_k = E_k,final − E_k,initial). <!-- CN formula preserved for parity: `$\Delta E_k = E_{k\text{末}} - E_{k\text{初}}$` -->
   * Since the object is initially at rest ($v_0 = 0$), the initial kinetic energy is $0$.
   * Writing the equation: $W = \frac{1}{2}mv^2 \implies 64 = \frac{1}{2} \times 2 \times v^2 \implies v^2 = 64$, which easily gives the velocity at $4\text{ m}$ as $8\text{ m/s}$.

3. **Part (3): find the impulse $I$**
   * Computing this problem from the impulse definition $I = \int F\text{d}t$ would be very complicated, because we do not know the force as a function of time $t$.
   * **Shortcut**: use the **impulse–momentum theorem** directly — the impulse equals the change of momentum $\Delta p = mv - mv_0$.
   * Here $m = 2\text{ kg}$, the final velocity is the $8\text{ m/s}$ just found, and the initial velocity is $0$.
   * We immediately get: $I = 2 \times 8 = 16\text{ N}\cdot\text{s}$. Using the relation between kinetic energy and momentum avoids the complicated integral.

---

## Exercise 2-18

### Answer

Given $m = 0.5\text{ kg}$ and the equations of motion $x = 5t$, $y = 0.5t^2$.

Differentiating with respect to time $t$ gives the velocity components:
$$v_x = \frac{\text{d}x}{\text{d}t} = 5\text{ m}\cdot\text{s}^{-1}$$
$$v_y = \frac{\text{d}y}{\text{d}t} = t\text{ m}\cdot\text{s}^{-1}$$

At $t_1 = 2\text{ s}$, the velocity components and the squared speed are:
$$v_{x1} = 5\text{ m}\cdot\text{s}^{-1},\quad v_{y1} = 2\text{ m}\cdot\text{s}^{-1}$$
$$v_1^2 = v_{x1}^2 + v_{y1}^2 = 5^2 + 2^2 = 29\text{ m}^2\cdot\text{s}^{-2}$$

At $t_2 = 4\text{ s}$, the velocity components and the squared speed are:
$$v_{x2} = 5\text{ m}\cdot\text{s}^{-1},\quad v_{y2} = 4\text{ m}\cdot\text{s}^{-1}$$
$$v_2^2 = v_{x2}^2 + v_{y2}^2 = 5^2 + 4^2 = 41\text{ m}^2\cdot\text{s}^{-2}$$

By the work–energy theorem, the work $W$ done by the external force is:
$$W = \Delta E_k = \frac{1}{2}mv_2^2 - \frac{1}{2}mv_1^2$$
$$W = \frac{1}{2} \times 0.5 \times (41 - 29) = 0.25 \times 12 = 3\text{ J}$$

---

### Solution walkthrough

1. **Core method (a clever use of the work–energy theorem)**:
   * The problem asks for the work done by the external force during $2\text{ s} \sim 4\text{ s}$. The work done by the external force directly equals the **change of the kinetic energy** (work–energy theorem). So we only need the speed of the particle at the two instants $t=2\text{ s}$ and $t=4\text{ s}$.

2. **Step 1: find the velocity components**
   * The particle moves in two dimensions in the plane, and its velocity is composed of the $x$ direction and the $y$ direction together.
   * The $x$-velocity $v_x$ is the derivative of the position $x = 5t$ with respect to time $t$; the result is the constant value $5$.
   * The $y$-velocity $v_y$ is the derivative of the position $y = 0.5t^2$ with respect to time $t$; the result is $t$.

3. **Step 2: compute the squared speeds at the two instants**
   * Formula for the squared speed (Pythagorean theorem): $v^2 = v_x^2 + v_y^2$.
   * At $t=2\text{ s}$: $v_1^2 = 5^2 + 2^2 = 29$.
   * At $t=4\text{ s}$: $v_2^2 = 5^2 + 4^2 = 41$.

4. **Step 3: find the work $W$**
   * Change of kinetic energy: $W = \frac{1}{2}m v_2^2 - \frac{1}{2}m v_1^2 = \frac{1}{2}m(v_2^2 - v_1^2)$.
   * Substituting the data: $W = \frac{1}{2} \times 0.5 \times (41 - 29) = 0.25 \times 12 = 3\text{ J}$.

---

# Chapter 3 Rotation of a Rigid Body about a Fixed Axis

## Exercise 3-6

> **Supplementary note:** In the original exam problem, the specific quantities to find after "Find:" are missing. Usually this kind of classic problem has two parts:
> (1) the **angular acceleration** $\beta$ at the instant of release;
> (2) the **angular velocity** $\omega$ when the rod has rotated to the horizontal position. The standard solutions for these two classic quantities are given below.

### Answer

Given $l = 1\text{ m}$, the moment of inertia about the end point $O$ is $J = \frac{1}{3}ml^2$, and the initial release angle is $\theta = 60^\circ$.

```
   / (release position, 60 degrees above the horizontal)
  / 
 /_ 60°
O ------------------- (horizontal position)
```

**(1) Find the angular acceleration $\beta$ at the instant of release:**
At the instant of release, the gravity $mg$ acts at the center of mass of the rod (the midpoint $\frac{l}{2}$), and its moment arm about the axis $O$ is $d = \frac{l}{2}\cos 60^\circ$.
By the law of rotation $M = J\beta$:
$$mg \frac{l}{2} \cos 60^\circ = \frac{1}{3}ml^2 \beta$$
$$\frac{1}{2}g \cos 60^\circ = \frac{1}{3}l \beta$$
$$\beta = \frac{3g\cos 60^\circ}{2l} = \frac{3 \times 9.8 \times 0.5}{2 \times 1} = 7.35\text{ rad}\cdot\text{s}^{-2}$$

**(2) Find the angular velocity $\omega$ when the rod has rotated to the horizontal position:**
Take the horizontal plane containing the point $O$ as the zero level of gravitational potential energy. By the law of conservation of mechanical energy:
$$E_{k1} + E_{p1} = E_{k2} + E_{p2}$$
$$0 + mg \frac{l}{2} \sin 60^\circ = \frac{1}{2} J \omega^2 + 0$$
$$mg \frac{l}{2} \sin 60^\circ = \frac{1}{2} \left( \frac{1}{3}ml^2 \right) \omega^2$$
$$g \sin 60^\circ = \frac{1}{3}l \omega^2$$
$$\omega = \sqrt{\frac{3g\sin 60^\circ}{l}} = \sqrt{\frac{3 \times 9.8 \times \frac{\sqrt{3}}{2}}{1}} = \sqrt{25.46} \approx 5.05\text{ rad}\cdot\text{s}^{-1}$$

---

### Solution walkthrough

1. **Part (1): applying the law of rotation of a rigid body (finding the angular acceleration)**
   * Just as particle motion uses $F=ma$, rigid-body rotation uses the **law of rotation**: $M = J\beta$, where $M$ is the net external torque, $J$ is the moment of inertia, and $\beta$ is the angular acceleration of the rotation.
   * The gravity $mg$ acts at the geometric center of the rod (i.e. the midpoint $l/2$). Gravity points vertically downward and the pivot $O$ is at the left end, so the moment arm (the perpendicular distance from the axis to the line of action of the force) is $\frac{l}{2}\cos 60^\circ$.
   * Setting up the equation: the gravity torque $M = mg \cdot \frac{l}{2}\cos 60^\circ$ equals $J\beta = \frac{1}{3}ml^2 \beta$.
   * Canceling the mass $m$ and one length $l$ on both sides and substituting the data, we get $\beta = 7.35\text{ rad/s}^2$.

2. **Part (2): conservation of mechanical energy (finding the angular velocity when the rod reaches the horizontal)**
   * As the rod swings down, only gravity does work, so **mechanical energy is conserved** (kinetic energy + potential energy = constant).
   * The rotational kinetic energy of a rigid body is given by $E_k = \frac{1}{2}J\omega^2$.
   * Change of the height of the center of mass: initially the center of mass is at the midpoint, tilted upward at $60^\circ$, so its height is $h = \frac{l}{2}\sin 60^\circ$; when the rod reaches the horizontal position, the height of the center of mass is $0$.
   * The decrease of the gravitational potential energy equals the increase of the rotational kinetic energy: $mg \Delta h = \frac{1}{2} J \omega^2$.
   * Substituting the data gives the angular velocity $\omega \approx 5.05\text{ rad/s}$.

---

## Exercise 3-8

### Answer

Given $m_1 = 0.46\text{ kg}$, $m_2 = 0.50\text{ kg}$, $R = 0.05\text{ m}$; starting from rest, the weight descends the height $h = 0.75\text{ m}$ within $t = 5.0\text{ s}$.

The weight moves with uniformly accelerated rectilinear motion:
$$h = \frac{1}{2}at^2 \implies 0.75 = \frac{1}{2} a \times 5.0^2$$
$$a = \frac{2 \times 0.75}{25} = 0.06\text{ m}\cdot\text{s}^{-2}$$

The angular acceleration $\beta$ of the pulley is:
$$\beta = \frac{a}{R} = \frac{0.06}{0.05} = 1.2\text{ rad}\cdot\text{s}^{-2}$$

Write the dynamic equations for $m_2$, $m_1$, and the pulley respectively (let the string tensions be $T_2$ and $T_1$ respectively, and take $g = 9.8\text{ m}\cdot\text{s}^{-2}$):
For $m_2$ (descending):
$$m_2 g - T_2 = m_2 a \implies T_2 = m_2(g - a)$$
For $m_1$ (rising):
$$T_1 - m_1 g = m_1 a \implies T_1 = m_1(g + a)$$
For the pulley (rotating):
$$(T_2 - T_1)R = J\beta$$

Substituting $T_2$ and $T_1$ into the pulley equation:
$$\left[ m_2(g - a) - m_1(g + a) \right] R = J \frac{a}{R}$$
$$J = \frac{R^2}{a} \left[ (m_2 - m_1)g - (m_2 + m_1)a \right]$$

Substituting the numerical values:
$$J = \frac{0.05^2}{0.06} \left[ (0.50 - 0.46) \times 9.8 - (0.50 + 0.46) \times 0.06 \right]$$
$$J = \frac{0.0025}{0.06} \left[ 0.04 \times 9.8 - 0.96 \times 0.06 \right]$$
$$J = \frac{1}{24} \left[ 0.392 - 0.0576 \right] = \frac{1}{24} \times 0.3344 \approx 0.0139\text{ kg}\cdot\text{m}^2$$

---

### Solution walkthrough

1. **Step 1: find the acceleration $a$ and the angular acceleration $\beta$**
   * The falling weight undergoes uniformly accelerated rectilinear motion. Given the initial velocity $0$ and that it descends $h=0.75\text{ m}$ within the time $t=5\text{ s}$.
   * Using the kinematic formula $h = \frac{1}{2}at^2$, we directly find the acceleration $a = 0.06\text{ m/s}^2$.
   * Since the string does not slip on the pulley, the linear acceleration of the pulley rim equals the translational acceleration $a$ of the weight, so the angular acceleration of the pulley's rotation is $\beta = \frac{a}{R} = 1.2\text{ rad/s}^2$.

2. **Step 2: analyze the forces on the system (the core!)**
   * **Note**: because the pulley has mass and moment of inertia, the string tensions $T_1$ and $T_2$ on the two sides are **not equal** (the $m_2$ on the right is heavier, so $T_2 > T_1$, and the two tensions spin the pulley with increasing clockwise speed).
   * For the left $m_2$: it accelerates downward, so gravity is greater than the tension: $m_2 g - T_2 = m_2 a$.
   * For the right $m_1$: it accelerates upward, so the tension is greater than gravity: $T_1 - m_1 g = m_1 a$.
   * For the pulley: the torques come from the clockwise torque $T_2 R$ of $T_2$ and the counterclockwise torque $T_1 R$ of $T_1$. The net torque is $(T_2 - T_1)R$. By the law of rotation, $(T_2 - T_1)R = J\beta$.

3. **Step 3: solve the system by elimination to find $J$**
   * Express $T_2$ and $T_1$ from the first two equations respectively, and substitute them into the third equation.
   * Rearrange into an expression for the moment of inertia $J$, substitute the given mass, radius, gravitational acceleration $g=9.8$, and the computed $a$, and the calculation gives $J \approx 0.0139\text{ kg}\cdot\text{m}^2$.

---

## Exercise 3-10

### Answer

Given $m_1 = 5\text{ kg}$, $\theta = 30^\circ$, $\mu = 0.25$, $m_2 = 10\text{ kg}$, pulley $m = 20\text{ kg}$, radius $R = 0.2\text{ m}$, and the pulley is a disk ($J = \frac{1}{2}m R^2$).

Let the magnitude of the acceleration of the weights be $a$ ($m_2$ accelerates downward, $m_1$ accelerates up the incline), and the angular acceleration of the pulley be $\beta = \frac{a}{R}$. Let the string tension on the $m_1$ side be $T_1$ and the string tension on the $m_2$ side be $T_2$.

Write the dynamic equations for each object:
1. For $m_2$ (accelerating vertically downward):
   $$m_2 g - T_2 = m_2 a \quad \text{--- (1)}$$
2. For $m_1$ (accelerating up the incline):
   $$T_1 - m_1 g \sin\theta - f = m_1 a \quad \text{--- (2)}$$
   where the friction force is $f = \mu N = \mu m_1 g \cos\theta$.
3. For the disk pulley (rotating clockwise):
   $$(T_2 - T_1)R = J\beta = \left(\frac{1}{2}m R^2\right) \left(\frac{a}{R}\right) \implies T_2 - T_1 = \frac{1}{2}m a \quad \text{--- (3)}$$

Adding equations (1) and (2), and using equation (3):
$$(m_2 g - T_2) + (T_1 - m_1 g \sin\theta - \mu m_1 g \cos\theta) = (m_1 + m_2) a$$
$$m_2 g - (T_2 - T_1) - m_1 g(\sin\theta + \mu \cos\theta) = (m_1 + m_2) a$$
$$m_2 g - \frac{1}{2}m a - m_1 g(\sin\theta + \mu \cos\theta) = (m_1 + m_2) a$$

Rearranging gives the formula for the acceleration $a$:
$$a = \frac{m_2 - m_1(\sin\theta + \mu \cos\theta)}{m_1 + m_2 + \frac{1}{2}m} g$$

Substituting the data (taking $g = 9.8\text{ m}\cdot\text{s}^{-2}$):
$$a = \frac{10 - 5 \times (\sin 30^\circ + 0.25 \cos 30^\circ)}{5 + 10 + \frac{1}{2} \times 20} \times 9.8$$
$$a = \frac{10 - 5 \times (0.5 + 0.25 \times 0.866)}{25} \times 9.8 = \frac{10 - 5 \times 0.7165}{25} \times 9.8$$
$$a = \frac{10 - 3.58}{25} \times 9.8 = \frac{6.42}{25} \times 9.8 \approx 2.52\text{ m}\cdot\text{s}^{-2}$$

Find the string tensions:
Substituting $a$ into equation (1) to find $T_2$:
$$T_2 = m_2(g - a) = 10 \times (9.8 - 2.52) = 72.8\text{ N}$$
Substituting $a$ into equation (3) to find $T_1$:
$$T_1 = T_2 - \frac{1}{2}ma = 72.8 - \frac{1}{2} \times 20 \times 2.52 = 72.8 - 25.2 = 47.6\text{ N}$$

---

### Solution walkthrough

1. **Analysis of the overall motion tendency**:
   * The hanging weight on the left, $m_2 = 10\text{ kg}$, is heavier, while the $m_1 = 5\text{ kg}$ on the incline is lighter and is held back by the incline. Therefore, the system must move to the left, i.e. $m_2$ accelerates downward and $m_1$ slides up the incline toward the upper right.

2. **Set up the dynamic equations for each part**:
   * **For the $m_1$ on the incline**: along the incline direction, it feels the upward pull $T_1$ of the string, the component of gravity down the incline $m_1 g \sin\theta$, and the opposing friction force $f$ that hinders the motion.
     By the friction formula: $f = \mu N$, where the normal force perpendicular to the incline is $N = m_1 g \cos\theta$. So $f = \mu m_1 g \cos\theta$.
     Newton's second law gives: $T_1 - m_1 g \sin\theta - \mu m_1 g \cos\theta = m_1 a$.
   * **For the hanging $m_2$**: it feels the downward gravity $m_2 g$ and the upward pull $T_2$ of the string.
     Equation: $m_2 g - T_2 = m_2 a$.
   * **For the disk pulley**: the pulls on the left and right are not equal, producing a driving torque.
     $(T_2 - T_1)R = J\beta$. Because the pulley is a uniform disk, its moment of inertia is $J = \frac{1}{2}mR^2$; substituting $\beta = \frac{a}{R}$ and canceling the radius $R$ simplifies this to: $T_2 - T_1 = \frac{1}{2}ma$.

3. **Solve the simultaneous equations**:
   * This is a system of three equations with the unknowns $a$, $T_1$, and $T_2$.
   * The fastest way is to rearrange the first two equations and substitute them into the third one, which eliminates the tensions directly and gives the acceleration $a \approx 2.52\text{ m/s}^2$.
   * Once the acceleration is found, substitute it back into the step-by-step equations above, and the two string tensions come out easily: $T_1 = 47.6\text{ N}$ and $T_2 = 72.8\text{ N}$.

---

# Chapter 6 Mechanical Oscillations and Mechanical Waves

## Exercise 6-5

### Answer

Given the period $T = 2\text{ s}$, the amplitude $A = 0.06\text{ m}$, and the wave speed $u = 2\text{ m}\cdot\text{s}^{-1}$. At $t=0$, $y_0 = -A = -0.06\text{ m}$.

**(1) Find the kinematic equation of this particle:**
The angular frequency $\omega$ is:
$$\omega = \frac{2\pi}{T} = \frac{2\pi}{2} = \pi\text{ rad}\cdot\text{s}^{-1}$$
Let the simple harmonic oscillation equation be:
$$y = A\cos(\omega t + \phi) = 0.06\cos(\pi t + \phi)$$
Substituting the initial condition $t=0, y = -0.06\text{ m}$:
$$-0.06 = 0.06\cos\phi \implies \cos\phi = -1 \implies \phi = \pi$$
Hence the kinematic equation of this particle is:
$$y = 0.06\cos(\pi t + \pi)\quad(\text{m})$$

**(2) Find the wave expression of the one-dimensional simple harmonic wave propagating along the positive $x$-axis:**
The wave propagates along the positive $x$-axis, so the oscillation phase of every particle lags behind. The wave expression is:
$$y(x, t) = A\cos\left[ \omega \left(t - \frac{x}{u}\right) + \phi \right]$$
Substituting $A = 0.06$, $\omega = \pi$, $u = 2$, $\phi = \pi$:
$$y(x, t) = 0.06\cos\left[ \pi \left(t - \frac{x}{2}\right) + \pi \right]\quad(\text{m})$$

**(3) Find the wavelength $\lambda$ of this wave:**
$$\lambda = uT = 2 \times 2 = 4\text{ m}$$

---

### Solution walkthrough

1. **The basic form of the simple harmonic motion equation**:
   * The general formula of simple harmonic motion is $y = A\cos(\omega t + \phi)$, where:
     * $A$ is the amplitude (the maximum displacement, given as $0.06$).
     * $\omega$ is the angular frequency, related to the period $T$ by $\omega = \frac{2\pi}{T}$, giving $\omega = \pi$.
     * $\phi$ is the initial phase (the angular state at the instant $t=0$).

2. **Part (1): find the initial phase $\phi$**
   * The problem says "at $t=0$ the particle is exactly at the maximum displacement in the negative direction", which means the displacement is $y = -A = -0.06\text{ m}$.
   * Substituting into the simple harmonic formula: $-0.06 = 0.06 \cos\phi \implies \cos\phi = -1 \implies \phi = \pi$.
   * So the equation of motion of this particle is $y = 0.06\cos(\pi t + \pi)$ (using a trigonometric identity it can also be simplified to $y = -0.06\cos(\pi t)$).

3. **Part (2): find the wave expression of the simple harmonic wave**
   * A wave is the propagation of an oscillation through space. If a wave propagates in the **positive** direction of the $x$-axis, then the oscillation of the particle at the distance $x$ from the origin **lags behind** the origin by the time $\Delta t = \frac{x}{u}$ (distance divided by wave speed).
   * So we only need to replace the time $t$ in the oscillation equation of the particle at the origin with $\left(t - \frac{x}{u}\right)$ — that's all!
   * Direct replacement: $y = 0.06\cos\left[\pi \left(t - \frac{x}{2}\right) + \pi\right]$. This is the very classic way of writing the wave expression.

4. **Part (3): find the wavelength $\lambda$**
   * The wavelength is the distance the wave travels in one period: λ = wave speed × period = u × T. <!-- CN formula preserved for parity: `$\lambda = \text{波速} \times \text{周期} = u \times T$` -->
   * Given $u = 2\text{ m/s}$ and $T = 2\text{ s}$, the wavelength is $\lambda = 4\text{ m}$.

---

## Exercise 6-10

### Answer

From the waveform graph at $t=0$ we can read off:
* Amplitude $A = 0.04\text{ m}$
* Wavelength $\lambda = 0.40\text{ m}$
* Wave speed $u = 0.08\text{ m}\cdot\text{s}^{-1}$ (propagating in the positive $x$-axis direction)

```
y (m)
^
|      /\
|     /  \
|----/----\----> x (m)
| O /      \
|  /        \
| /          \
```

The period $T$ and the angular frequency $\omega$ are:
$$T = \frac{\lambda}{u} = \frac{0.40}{0.08} = 5.0\text{ s}$$
$$\omega = \frac{2\pi}{T} = \frac{2\pi}{5} = 0.4\pi\text{ rad}\cdot\text{s}^{-1}$$

**(1) Find the wave expression of this wave:**
Let the oscillation equation of the particle at the point $O$ ($x = 0$) be $y_O = A\cos(\omega t + \phi_0)$.
From the waveform graph at $t=0$, the displacement of the particle at the origin $O$ is $y_O(0) = 0$. Since the wave propagates in the positive $x$ direction and the waveform moves to the right, the particle at $O$ is moving in the negative $y$-axis direction at this moment, i.e. the oscillation velocity satisfies $v_y < 0$.
By the method for determining the initial phase of simple harmonic motion:
$$\begin{cases} \cos\phi_0 = 0 \\ \sin\phi_0 > 0 \end{cases} \implies \phi_0 = \frac{\pi}{2}$$
So the oscillation equation of the origin $O$ is:
$$y_O = 0.04\cos\left(0.4\pi t + \frac{\pi}{2}\right)\quad(\text{m})$$

Since the wave propagates along the positive $x$-axis, the wave expression is:
$$y(x, t) = A\cos\left[ \omega \left(t - \frac{x}{u}\right) + \phi_0 \right]$$
$$y(x, t) = 0.04\cos\left[ 0.4\pi \left(t - \frac{x}{0.08}\right) + \frac{\pi}{2} \right]$$
$$y(x, t) = 0.04\cos\left( 0.4\pi t - 5\pi x + \frac{\pi}{2} \right)\quad(\text{m})$$

**(2) Find the equation of motion of the particle at the point $P$ ($x = 0.20\text{ m}$):**
Substituting $x = 0.20\text{ m}$ into the wave expression:
$$y_P(t) = 0.04\cos\left( 0.4\pi t - 5\pi \times 0.20 + \frac{\pi}{2} \right)$$
$$y_P(t) = 0.04\cos\left( 0.4\pi t - \pi + \frac{\pi}{2} \right)$$
$$y_P(t) = 0.04\cos\left( 0.4\pi t - \frac{\pi}{2} \right)\quad(\text{m})$$

---

### Solution walkthrough

1. **Step 1: extract the useful information from the waveform graph (t=0)**
   * **Amplitude $A$**: the maximum height of a wave crest, which is $0.04\text{ m}$ on the $y$-axis.
   * **Wavelength $\lambda$**: the length of one complete waveform; in the graph, one complete cycle of the wave spans $0.40\text{ m}$ on the $x$-axis.
   * **Wave speed $u$**: the graph directly gives $u = 0.08\text{ m/s}$.
   * Hence the period is $T = \frac{\lambda}{u} = 5\text{ s}$ and the angular frequency is $\omega = \frac{2\pi}{T} = 0.4\pi$.

2. **Step 2: find the initial phase $\phi_0$ of the origin $O$**
   * Look at the position of the origin $O$ at $t=0$: it is exactly at $y=0$ (the equilibrium position). This means $\cos\phi_0 = 0$, so the initial phase could be $\frac{\pi}{2}$ or $-\frac{\pi}{2}$.
   * **Judging the direction of motion by shifting the waveform**: since the wave travels to the right, shift the waveform slightly to the right, and you will find that the particle at the origin $O$ is about to **swing downward** (its velocity points in the negative direction).
   * The velocity points in the negative direction, which means the initial phase $\phi_0$ lies in the first or second quadrant; hence $\phi_0 = \frac{\pi}{2}$.

3. **Step 3: write out the wave expression**
   * Apply the formula for a right-traveling wave: $y = A\cos\left[\omega\left(t - \frac{x}{u}\right) + \phi_0\right]$.
   * Substituting the data and simplifying: $0.4\pi \left(t - \frac{x}{0.08}\right) + \frac{\pi}{2} = 0.4\pi t - 5\pi x + \frac{\pi}{2}$.

4. **Step 4: find the equation of motion at the specific point $P$**
   * The wave expression gives the displacement of **any point** in space at **any time**.
   * Since the equation at the point $P$ (coordinate $x=0.20\text{ m}$) is required, we only need to substitute $x = 0.20$ into the wave expression and simplify the constant terms, which gives a one-dimensional oscillation equation containing only the time $t$: $y_P = 0.04\cos(0.4\pi t - \frac{\pi}{2})$.

---

# Chapter 9 Electrostatic Field

## Exercise 9-9

### Answer

Given two imaginary concentric spherical surfaces of radii $R_1 = 0.1\text{ m}$ and $R_2 = 0.2\text{ m}$ respectively, with volume charge density $\rho = 10^{-9}\text{ C}\cdot\text{m}^{-3}$.

By the spherical symmetry, choose a concentric spherical surface as the Gaussian surface. Gauss's law takes the form:
$$\oint_{S} E\,\text{d}S = E \cdot 4\pi r^2 = \frac{\sum q_{\text{enclosed}}}{\varepsilon_0}$$
$$E = \frac{\sum q_{\text{enclosed}}}{4\pi \varepsilon_0 r^2}$$

**(1) When $r = 5\text{ cm} = 0.05\text{ m}$:**
Since $r < R_1$, the charge enclosed by the Gaussian surface is Σq_enc = 0. <!-- CN formula preserved for parity: `$\sum q_{\text{内}} = 0$` -->
Hence:
$$E_1 = 0$$

**(2) When $r = 15\text{ cm} = 0.15\text{ m}$:**
Since $R_1 < r < R_2$, the charge enclosed by the Gaussian surface is the charge of the spherical shell with radii from $R_1$ to $r$:
$$\sum q_{\text{enclosed}} = \rho V' = \rho \cdot \frac{4}{3}\pi (r^3 - R_1^3)$$
Hence the electric field strength there is:
$$E_2 = \frac{\rho \cdot \frac{4}{3}\pi (r^3 - R_1^3)}{4\pi \varepsilon_0 r^2} = \frac{\rho(r^3 - R_1^3)}{3\varepsilon_0 r^2}$$
Substituting the data (taking $\varepsilon_0 \approx 8.85 \times 10^{-12}\text{ C}^2\cdot\text{N}^{-1}\cdot\text{m}^{-2}$):
$$E_2 = \frac{10^{-9} \times (0.15^3 - 0.1^3)}{3 \times 8.85 \times 10^{-12} \times 0.15^2} = \frac{10^{-9} \times (0.003375 - 0.001)}{3 \times 8.85 \times 10^{-12} \times 0.0225}$$
$$E_2 = \frac{10^{-9} \times 0.002375}{5.97375 \times 10^{-13}} \approx 3.98\text{ V}\cdot\text{m}^{-1}$$

**(3) When $r = 50\text{ cm} = 0.5\text{ m}$:**
Since $r > R_2$, the Gaussian surface encloses the charge of the entire charged spherical shell:
$$\sum q_{\text{enclosed}} = \rho \cdot \frac{4}{3}\pi (R_2^3 - R_1^3)$$
Hence the electric field strength there is:
$$E_3 = \frac{\rho(R_2^3 - R_1^3)}{3\varepsilon_0 r^2}$$
Substituting the data:
$$E_3 = \frac{10^{-9} \times (0.2^3 - 0.1^3)}{3 \times 8.85 \times 10^{-12} \times 0.5^2} = \frac{10^{-9} \times (0.008 - 0.001)}{3 \times 8.85 \times 10^{-12} \times 0.25}$$
$$E_3 = \frac{7 \times 10^{-12}}{6.6375 \times 10^{-12}} \approx 1.05\text{ V}\cdot\text{m}^{-1}$$

---

### Solution walkthrough

1. **The core tool: Gauss's law**
   * In an electrostatic field, if the charge distribution is highly symmetric (e.g. a sphere, a spherical shell, an infinitely long cylinder), the one and only way to find the electric field strength is **Gauss's law**.
   * Formula of Gauss's law: the electric flux $\oint E\text{d}S$ through a closed surface (the Gaussian surface) equals the total net charge Σq_enc enclosed inside that surface divided by the vacuum permittivity $\varepsilon_0$. <!-- CN formula preserved for parity: `$\sum q_{\text{内}}$` -->
   * For a spherically symmetric distribution, we choose a concentric spherical surface of radius $r$ as the Gaussian surface. On this surface, the magnitude of the field strength $E$ is the same everywhere and perpendicular to the surface, so the integral part simplifies directly to $E \cdot (4\pi r^2)$ (the field times the area of the sphere).
   * The general solving formula is: E = Σq_enc / (4πε₀r²). We only need to analyze **how much charge is enclosed by the Gaussian surfaces of different radii**. <!-- CN formula preserved for parity: `$E = \frac{\sum q_{\text{内}}}{4\pi \varepsilon_0 r^2}$` -->

2. **Part (1): $r=5\text{ cm}$ (inside the inner sphere)**
   * All the charge is distributed in the layer between $10\text{ cm} \sim 20\text{ cm}$.
   * The Gaussian surface of radius $5\text{ cm}$ encloses nothing at all, so the enclosed charge is q_enc = 0. The electric field strength inside is therefore simply $0$. <!-- CN formula preserved for parity: `$q_{\text{内}} = 0$` -->

3. **Part (2): $r=15\text{ cm}$ (in the middle)**
   * This Gaussian surface encloses part of the charge. Specifically, it encloses the thickness of the charged spherical shell from the inner radius $10\text{ cm}$ ($0.1\text{ m}$) up to the current radius $15\text{ cm}$ ($0.15\text{ m}$).
   * The charged volume: $V' = \frac{4}{3}\pi r^3 - \frac{4}{3}\pi R_1^3$. The charge is the volume times the volume charge density $\rho$.
   * Substituting into the Gauss's law formula and canceling the constants: $E = \frac{\rho(r^3 - R_1^3)}{3\varepsilon_0 r^2}$. Substituting the numbers gives $E \approx 3.98\text{ V/m}$.

4. **Part (3): $r=50\text{ cm}$ (on the outside)**
   * The Gaussian surface is now very large and encloses the entire charged layer ($10\text{ cm} \sim 20\text{ cm}$).
   * The total enclosed charge is fixed and corresponds to the volume of the entire spherical shell: V_total = (4/3)π(R₂³ − R₁³). <!-- CN formula preserved for parity: `$V_{\text{总}} = \frac{4}{3}\pi (R_2^3 - R_1^3)$` -->
   * Substituting into the Gauss's law formula in the same way: $E = \frac{\rho(R_2^3 - R_1^3)}{3\varepsilon_0 r^2}$. Substituting $r=0.5\text{ m}$ and computing gives $E \approx 1.05\text{ V/m}$.

---

## Exercise 9-12

### Answer

By the axial symmetry of the "infinitely long" charged cylinder, choose a cylindrical surface of radius $r$ and length $L$, coaxial with the cylinder, as the closed Gaussian surface.

Gauss's law:
$$\oint_{S} \boldsymbol{E} \cdot \text{d}\boldsymbol{S} = E \cdot 2\pi r L = \frac{\sum q_{\text{enclosed}}}{\varepsilon_0}$$

**(1) When $r < R$ (inside the cylinder):**
The charge enclosed by the Gaussian surface is:
$$\sum q_{\text{enclosed}} = \rho \cdot \pi r^2 L$$
Substituting into Gauss's law:
$$E \cdot 2\pi r L = \frac{\rho \cdot \pi r^2 L}{\varepsilon_0} \implies E = \frac{\rho}{2\varepsilon_0} r$$

**(2) When $r \geq R$ (outside the cylinder):**
The Gaussian surface encloses all the charge of this segment of the cylinder:
$$\sum q_{\text{enclosed}} = \rho \cdot \pi R^2 L$$
Substituting into Gauss's law:
$$E \cdot 2\pi r L = \frac{\rho \cdot \pi R^2 L}{\varepsilon_0} \implies E = \frac{\rho R^2}{2\varepsilon_0} \frac{1}{r}$$

**(3) The $E$-$r$ curve:**
* In the range $r < R$, $E$ is proportional to $r$ (a linear rise).
* In the range $r \geq R$, $E$ is inversely proportional to $r$ (a hyperbolic fall).
* The field reaches its maximum at $r = R$: $E_{\text{max}} = \frac{\rho R}{2\varepsilon_0}$.

```
 E 
 ^      /|
 |     / | \
 |    /  |  \
 |   /   |   \
 +--/----+----> r
 0       R
```

---

### Solution walkthrough

1. **How to construct the Gaussian surface? (Cylindrical symmetry)**
   * For the "infinitely long" cylinder, its field lines radiate horizontally outward, like a hedgehog's spines.
   * We build a coaxial **cylindrical tin can** of radius $r$ and height $L$ as the Gaussian surface.
   * The field passes only through the curved side of this "can", not through the top and bottom faces.
   * The curved side area of the can is $2\pi r L$, so the total electric flux through the Gaussian surface is $E \cdot (2\pi r L)$.

2. **Stage 1: inside the cylinder ($r < R$)**
   * The Gaussian tin can contains only part of the charged cylinder inside it.
   * The volume of this part of the cylinder is $\pi r^2 L$, so the charge inside it is q_enc = ρ · πr²L. <!-- CN formula preserved for parity: `$q_{\text{内}} = \rho \cdot \pi r^2 L$` -->
   * Substituting into Gauss's formula: $E \cdot 2\pi r L = \frac{\rho \cdot \pi r^2 L}{\varepsilon_0}$.
   * Canceling $\pi, r, L$ on both sides gives $E = \frac{\rho}{2\varepsilon_0} r$.
   * **Physical meaning**: inside the cylinder, the field strength is proportional to the radius $r$; the farther out, the stronger the field (because more charge is enclosed).

3. **Stage 2: outside the cylinder ($r \geq R$)**
   * The Gaussian can is now thicker than the charged cylinder, so it contains the entire charged cylinder segment of radius $R$.
   * The charge it contains is fixed: q_enc = ρ · πR²L. <!-- CN formula preserved for parity: `$q_{\text{内}} = \rho \cdot \pi R^2 L$` -->
   * Substituting into Gauss's formula: $E \cdot 2\pi r L = \frac{\rho \cdot \pi R^2 L}{\varepsilon_0}$.
   * Canceling $\pi, L$ on both sides gives $E = \frac{\rho R^2}{2\varepsilon_0} \frac{1}{r}$.
   * **Physical meaning**: outside the cylinder, the field strength is inversely proportional to the distance $r$; the farther away, the weaker the field.

4. **How to draw the $E$-$r$ curve**:
   * From $0$ to $R$, draw a straight line rising from the origin (a proportional function);
   * Beyond $R$, draw a smooth descending curve that gradually approaches the horizontal axis (an inverse proportional function).

---

## Exercise 9-22

### Answer

Given two concentric spherical surfaces of radii $R_1 = 0.1\text{ m}$ and $R_2 = 0.3\text{ m}$ respectively. The small sphere carries $q_1 = 10^{-8}\text{ C}$ and the large sphere carries $q_2 = 1.5 \times 10^{-8}\text{ C}$.

By the spherical symmetry, use Gauss's law to find the field strength distribution $E(r)$ in each region:
1. When $r < R_1$:
   $$E = 0$$
2. When $R_1 < r < R_2$:
   $$E = \frac{q_1}{4\pi \varepsilon_0 r^2}$$
3. When $r > R_2$:
   $$E = \frac{q_1 + q_2}{4\pi \varepsilon_0 r^2}$$

By the integral relation between the potential and the field strength, $V(r) = \int_{r}^{\infty} E\,\text{d}r$ (taking the potential at infinity to be zero):

**(1) Find the potential $V_1$ at $r = 20\text{ cm} = 0.2\text{ m}$ from the center:**
Since $R_1 < r < R_2$, the potential is a piecewise accumulated integral:
$$V_1 = \int_{r}^{R_2} E(R_1 < r < R_2)\,\text{d}r + \int_{R_2}^{\infty} E(r > R_2)\,\text{d}r$$
$$V_1 = \int_{r}^{R_2} \frac{q_1}{4\pi \varepsilon_0 r^2}\,\text{d}r + \int_{R_2}^{\infty} \frac{q_1 + q_2}{4\pi \varepsilon_0 r^2}\,\text{d}r$$
$$V_1 = \frac{q_1}{4\pi \varepsilon_0} \left( \frac{1}{r} - \frac{1}{R_2} \right) + \frac{q_1 + q_2}{4\pi \varepsilon_0 R_2}$$
$$V_1 = \frac{1}{4\pi \varepsilon_0} \left( \frac{q_1}{r} + \frac{q_2}{R_2} \right)$$

Substituting the data (taking $\frac{1}{4\pi\varepsilon_0} = 9 \times 10^9\text{ N}\cdot\text{m}^2\cdot\text{C}^{-2}$):
$$V_1 = 9 \times 10^9 \times \left( \frac{10^{-8}}{0.2} + \frac{1.5 \times 10^{-8}}{0.3} \right)$$
$$V_1 = 9 \times 10^9 \times \left( 5 \times 10^{-8} + 5 \times 10^{-8} \right) = 9 \times 10^9 \times 10^{-7} = 900\text{ V}$$

**(2) Find the potential $V_2$ at $r = 50\text{ cm} = 0.5\text{ m}$ from the center:**
Since $r > R_2$, the field is determined only by the outside region:
$$V_2 = \int_{r}^{\infty} \frac{q_1 + q_2}{4\pi \varepsilon_0 r^2}\,\text{d}r = \frac{q_1 + q_2}{4\pi \varepsilon_0 r}$$
Substituting the data:
$$V_2 = 9 \times 10^9 \times \frac{10^{-8} + 1.5 \times 10^{-8}}{0.5}$$
$$V_2 = 9 \times 10^9 \times \frac{2.5 \times 10^{-8}}{0.5} = 9 \times 10^9 \times 5 \times 10^{-8} = 450\text{ V}$$

---

### Solution walkthrough

1. **The nature of the potential (superposition principle and integral formula)**
   * The potential is a scalar and enjoys an extremely handy **superposition principle**.
   * For a uniformly charged spherical surface there is a very famous result:
     * If you are **outside** the spherical surface ($r > R$), the potential it produces at your location is identical to that of a point charge with all the charge concentrated at the center: $V = \frac{q}{4\pi \varepsilon_0 r}$.
     * If you are **inside** the spherical surface ($r < R$), the field strength at any point inside is zero, so the potential is the same at every interior point and equals the potential of the surface itself: $V = \frac{q}{4\pi \varepsilon_0 R}$.
   * Once you master this result, this problem needs **no complicated integral at all** — just superpose the formulas!

2. **Part (1): find the potential at $r=20\text{ cm}$**
   * This point is $20\text{ cm}$ from the center, in the **middle** between the two spherical surfaces.
   * It lies **outside** the small sphere (radius $10\text{ cm}$), so the potential produced here by the small sphere is computed with the outside-point formula: V_small = (1/4πε₀) · q₁/r. <!-- CN formula preserved for parity: `$V_{\text{小}} = \frac{1}{4\pi \varepsilon_0} \cdot \frac{q_1}{r}$` -->
   * It lies **inside** the large sphere (radius $30\text{ cm}$), so the potential produced here by the large sphere equals the potential at its surface: V_large = (1/4πε₀) · q₂/R₂. <!-- CN formula preserved for parity: `$V_{\text{大}} = \frac{1}{4\pi \varepsilon_0} \cdot \frac{q_2}{R_2}$` -->
   * The total potential is the direct sum: V = V_small + V_large = 9 × 10⁹ × (10⁻⁸/0.2 + 1.5 × 10⁻⁸/0.3) = 900 V. <!-- CN formula preserved for parity: `$V = V_{\text{小}} + V_{\text{大}} = 9 \times 10^9 \times \left( \frac{10^{-8}}{0.2} + \frac{1.5 \times 10^{-8}}{0.3} \right) = 900\text{ V}$` -->

3. **Part (2): find the potential at $r=50\text{ cm}$**
   * This point is $50\text{ cm}$ from the center, **outside** both spherical surfaces.
   * Therefore it is an "outside point" with respect to both the small and the large sphere.
   * The total potential equals the sum of the outside-point potentials contributed by the two spheres: $V = \frac{1}{4\pi \varepsilon_0} \cdot \frac{q_1 + q_2}{r}$.
   * Substituting and computing: $V = 9 \times 10^9 \times \frac{2.5 \times 10^{-8}}{0.5} = 450\text{ V}$.

---

# Chapter 10 Steady Magnetic Field

## Exercise 10-9

### Answer

Given a hollow cylindrical conductor with inner and outer radii $a$ and $b$, carrying a uniformly distributed current $I$.

The current density $j$ distributed over the cross-section is:
$$j = \frac{I}{\pi(b^2 - a^2)}$$

By the axial symmetry, choose a coaxial circle of radius $r$ as the Ampèrian loop $L$. By Ampère's circuital law:
$$\oint_{L} \boldsymbol{B} \cdot \text{d}\boldsymbol{l} = B \cdot 2\pi r = \mu_0 \sum I_{\text{enclosed}}$$
$$B = \frac{\mu_0 \sum I_{\text{enclosed}}}{2\pi r}$$

**(1) Prove the formula for the magnetic induction in the region $a < r < b$:**
The current enclosed inside the loop $L$ is only the current in the annular region of the cross-section with radii from $a$ to $r$:
$$\sum I_{\text{enclosed}} = j \cdot \pi(r^2 - a^2) = \frac{I}{\pi(b^2 - a^2)} \cdot \pi(r^2 - a^2) = I \frac{r^2 - a^2}{b^2 - a^2}$$
Substituting into Ampère's circuital law:
$$B = \frac{\mu_0}{2\pi r} \left( I \frac{r^2 - a^2}{b^2 - a^2} \right) = \frac{\mu_0 I}{2\pi (b^2 - a^2)} \frac{r^2 - a^2}{r}$$
**Q.E.D.**

**(2) Check the formula in the limiting case $a = 0$:**
When $a = 0$, the hollow cylinder becomes a solid, uniformly current-carrying cylinder of radius $b$. Substituting into the formula:
$$B = \frac{\mu_0 I}{2\pi(b^2 - 0)} \frac{r^2 - 0}{r} = \frac{\mu_0 I r}{2\pi b^2}$$
This agrees exactly with the formula for the magnetic induction inside a solid wire with uniform current, so the formula passes the check.

**(3) When $r \geq b$:**
The Ampèrian loop encloses the entire current of the conductor, i.e. ΣI_enc = I. <!-- CN formula preserved for parity: `$\sum I_{\text{内}} = I$` -->
Substituting into Ampère's circuital law gives:
$$B \cdot 2\pi r = \mu_0 I \implies B = \frac{\mu_0 I}{2\pi r}$$

---

### Solution walkthrough

1. **The core tool: Ampère's circuital law**
   * When finding the magnetic field produced by a symmetric current distribution, we use **Ampère's circuital law**: ∮B dl = μ₀ ΣI_enc. <!-- CN formula preserved for parity: `$\oint B\text{d}l = \mu_0 \sum I_{\text{内}}$` -->
   * Choose a concentric circular loop of radius $r$ as the path; the integral on the left simplifies directly to: the magnetic induction $B$ times the circumference $2\pi r$.
   * The circuital law simplifies to: B = μ₀ΣI_enc / (2πr). The key question is likewise: **how much current passes through the interior of the loop**? <!-- CN formula preserved for parity: `$B = \frac{\mu_0 \sum I_{\text{内}}}{2\pi r}$` -->

2. **How to compute the partial current I_enc (the proportion method)** <!-- CN formula preserved for parity: `$I_{\text{内}}$` -->
   * The current is uniformly distributed over the solid part of the conductor (the annular cross-section).
   * The solid cross-sectional area of the conductor is: $\pi b^2 - \pi a^2 = \pi(b^2 - a^2)$.
   * The circle of radius $r$ we draw ($a < r < b$) encloses the solid cross-sectional area: $\pi r^2 - \pi a^2 = \pi(r^2 - a^2)$.
   * Since the current is uniformly distributed, by the ratio of areas the enclosed current is:
     $$\sum I_{\text{enclosed}} = I \times \frac{\text{enclosed area}}{\text{total cross-sectional area}} = I \frac{r^2 - a^2}{b^2 - a^2}$$
   * Substituting this current into B = μ₀ΣI_enc / (2πr) and rearranging gives the formula the problem asks to prove. <!-- CN formula preserved for parity: `$B = \frac{\mu_0 \sum I_{\text{内}}}{2\pi r}$` -->

3. **What does the limiting case $a = 0$ mean?**
   * $a = 0$ means the inner radius is zero, i.e. there is no hollow core any more and the conductor becomes an ordinary solid wire.
   * Substituting $a=0$ into the proved formula gives $B = \frac{\mu_0 I r}{2\pi b^2}$, which matches the classic result that the magnetic field inside a solid wire is proportional to the distance.

4. **When $r \geq b$ (outside the wire)**:
   * Since the loop is now drawn at the very outside, it naturally packs in all the current $I$ flowing through the cable, so ΣI_enc = I. <!-- CN formula preserved for parity: `$\sum I_{\text{内}} = I$` -->
   * The magnetic field formula is the classic formula outside an infinitely long straight wire: $B = \frac{\mu_0 I}{2\pi r}$.

---

## Exercise 10-10

### Answer

Given a coaxial cable consisting of an inner conductor cylinder (radius $a$) and an outer conductor tube (inner radius $b$, outer radius $c$). The two parts carry currents of the same magnitude $I$ but in opposite directions, uniformly distributed over their cross-sections.

By Ampère's circuital law:
$$B \cdot 2\pi r = \mu_0 \sum I_{\text{enclosed}} \implies B = \frac{\mu_0 \sum I_{\text{enclosed}}}{2\pi r}$$

**(1) When $r < a$ (inside the conductor cylinder):**
The loop encloses only part of the current of the inner conductor cylinder.
The current density of the inner conductor is $j_1 = \frac{I}{\pi a^2}$, and the enclosed current is:
$$\sum I_{\text{enclosed}} = j_1 \cdot \pi r^2 = I \frac{r^2}{a^2}$$
Hence the magnetic induction in this region is:
$$B = \frac{\mu_0 I r}{2\pi a^2}$$

**(2) When $a < r < b$ (between the two conductors):**
The loop encloses the entire current $I$ of the inner conductor, but not yet the current of the outer conductor.
$$\sum I_{\text{enclosed}} = I$$
Hence the magnetic induction in this region is:
$$B = \frac{\mu_0 I}{2\pi r}$$

**(3) When $b < r < c$ (inside the outer conductor):**
The loop completely encloses the current $I$ of the inner conductor (taken as positive), and also encloses part of the current of the outer conductor (whose current is reversed, taken as negative).
The cross-sectional area of the outer conductor is $\pi(c^2 - b^2)$, and the magnitude of the outer-conductor current enclosed by the loop is:
$$I_{\text{enc,outer}} = I \frac{r^2 - b^2}{c^2 - b^2}$$
Hence the net current is:
$$\sum I_{\text{enclosed}} = I - I_{\text{enc,outer}} = I \left( 1 - \frac{r^2 - b^2}{c^2 - b^2} \right) = I \frac{c^2 - r^2}{c^2 - b^2}$$
Hence the magnetic induction in this region is:
$$B = \frac{\mu_0 I}{2\pi r} \frac{c^2 - r^2}{c^2 - b^2}$$

**(4) When $r > c$ (outside the cable):**
The loop encloses all the currents of the inner and outer conductors. Since the two are equal in magnitude and opposite in direction, they cancel completely.
$$\sum I_{\text{enclosed}} = I - I = 0$$
Hence the magnetic induction in this region is:
$$B = 0$$

---

### Solution walkthrough

This is a very classic physics model of the coaxial cable; it mainly tests the flexible application of Ampère's circuital law in four different regions.

1. **Region 1: inside the innermost solid cylinder ($r < a$)**
   * Here the current is uniformly distributed over the solid disk of radius $a$.
   * The Gaussian loop of radius $r$ encloses only the fraction of the current given by the area ratio $\frac{r^2}{a^2}$.
   * The enclosed current is $I \frac{r^2}{a^2}$. Substituting into the formula gives $B = \frac{\mu_0 I r}{2\pi a^2}$ (the field grows linearly with the radius).

2. **Region 2: the gap between the two conductors ($a < r < b$)**
   * In this gap, our Ampèrian loop wraps around the entire inner core (radius $a$), so the current it encloses is the full $I$.
   * The outer tube has not been touched yet, so it needs no consideration.
   * Applying the formula directly gives the classic field outside a straight wire: $B = \frac{\mu_0 I}{2\pi r}$.

3. **Region 3: within the metal thickness of the outer conductor tube ($b < r < c$)**
   * This region is more complicated; the loop encloses two things:
     1. The entire innermost core, with current $+I$ (assume upward).
     2. The layer of the outer tube from its inner wall $b$ to the current position $r$, which carries the reversed current (downward).
   * The enclosed area of the outer tube is $\pi(r^2 - b^2)$ and its total cross-sectional area is $\pi(c^2 - b^2)$. By proportion, the magnitude of the enclosed reversed current is $I \frac{r^2 - b^2}{c^2 - b^2}$.
   * Canceling the forward current against the reversed current gives the net current inside the loop: $I - I \frac{r^2 - b^2}{c^2 - b^2} = I \frac{c^2 - r^2}{c^2 - b^2}$.
   * Substituting into the formula gives $B = \frac{\mu_0 I}{2\pi r} \frac{c^2 - r^2}{c^2 - b^2}$.

4. **Region 4: the very outside of the cable ($r > c$)**
   * Here comes the most magical part — it is also the principle behind the interference immunity of coaxial cables.
   * Our loop encloses the whole cable (inner core and outer tube).
   * However much current flows out through the core, the same flows back through the outer tube: the two currents are equal and opposite, so the net macroscopic charge flow is $0$ (ΣI_enc = I − I = 0). <!-- CN formula preserved for parity: `$\sum I_{\text{内}} = I - I = 0$` -->
   * Therefore, the magnetic field outside the coaxial cable is $B = 0$. In other words, the cable produces no magnetic interference to the outside world, and the outside world cannot easily interfere with it either!
