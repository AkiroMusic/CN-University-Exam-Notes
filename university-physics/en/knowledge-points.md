# Part One: Fundamentals of Mechanics (Chapters 1–3)

## Chapter 1 Kinematics of a Particle
> **Beginner's note**: Kinematics only cares about "how things move" (position, velocity, acceleration), not about "why they move" (forces are not considered). We simplify an object into a geometric point carrying mass — a "particle".

### 1-1 Description of Particle Motion
*   **Position vector** $\vec{r}$: the colored arrow pointing from the coordinate origin to the location of the particle.
    $$\vec{r} = x\vec{i} + y\vec{j} + z\vec{k}$$
*   **Displacement** $\Delta \vec{r}$: the change of position; note that it **does not equal** the path length $\Delta s$ (displacement is the straight segment between two points, while the path length is the actual length of the trajectory).
    $$\Delta \vec{r} = \vec{r}_2 - \vec{r}_1$$
*   **Velocity** $\vec{v}$: the rate of change of position with time (first derivative).
    *   Average velocity: $\bar{v} = \frac{\Delta \vec{r}}{\Delta t}$
    *   Instantaneous velocity (velocity for short): $\vec{v} = \frac{\mathrm{d}\vec{r}}{\mathrm{d}t}$
*   **Acceleration** $\vec{a}$: the rate of change of velocity with time (second derivative).
    $$\vec{a} = \frac{\mathrm{d}\vec{v}}{\mathrm{d}t} = \frac{\mathrm{d}^2\vec{r}}{\mathrm{d}t^2}$$

### 1-2 & 1-3 Rectilinear and Curvilinear Motion
*   **Rectilinear motion**: the direction does not change, so a scalar algebraic description suffices (note that the sign represents the direction).
*   **Curvilinear motion in the natural coordinate system**:
    Resolve the acceleration into two perpendicular components:
    $$\vec{a} = \vec{a}_t + \vec{a}_n$$
    *   **Tangential acceleration** $a_t = \frac{\mathrm{d}v}{\mathrm{d}t}$: changes the **magnitude** of the velocity.
    *   **Normal (centripetal) acceleration** $a_n = \frac{v^2}{\rho}$ ($\rho$ is the radius of curvature): changes the **direction** of the velocity (pointing toward the inside of the curve).
*   **Angular description of circular motion**:
    *   Angular position $\theta$, angular velocity $\omega = \frac{\mathrm{d}\theta}{\mathrm{d}t}$, angular acceleration $\alpha = \frac{\mathrm{d}\omega}{\mathrm{d}t}$.
    *   **The bridge that converts between linear and angular quantities**:
        $$v = R\omega, \quad a_t = R\alpha, \quad a_n = R\omega^2$$

### 1-4 & 1-5 The Two Types of Problems in Kinematics and Relative Motion
*   **Type-one problem**: given the position, find the velocity and acceleration (use **differentiation** $\frac{\mathrm{d}}{\mathrm{d}t}$).
*   **Type-two problem**: given the acceleration, find the velocity and position (use **integration** $\int \mathrm{d}t$; **never forget the initial-condition constants $C$**).
*   **Relative motion (Galilean transformation)**:
    $$\vec{v}_{\text{absolute}} = \vec{v}_{\text{relative}} + \vec{v}_{\text{transport}}$$
    *For example: you run forward inside a moving train (the moving frame); your velocity relative to the ground (absolute) = your velocity relative to the train (relative) + the velocity of the train relative to the ground (transport).*

---

## Chapter 2 Dynamics of a Particle
> **Beginner's note**: Dynamics begins to study the influence of "force" on the motion of objects. Newton's three laws are the absolute cornerstone of this chapter.

### 2-1 to 2-3 Newton's Laws of Motion, Their Applications, and Units
*   **Newton's first law**: the law of inertia. Without external force, an object stays at rest or keeps moving in a straight line at constant velocity.
*   **Newton's second law**:
    $$\vec{F} = \frac{\mathrm{d}\vec{p}}{\mathrm{d}t} = m\vec{a}$$ ($\vec{p}=m\vec{v}$ is the momentum)
    *Beginner's pitfall: this is a vector equation; when solving problems you must always write out the projected component equations (i.e. set up a Cartesian coordinate system and decompose into $F_x=ma_x, F_y=ma_y$).*
*   **Newton's third law**: action and reaction are equal in magnitude, opposite in direction, and act along the same straight line.

### 2-4 Inertial and Non-inertial Frames (Inertial Forces)
*   **Inertial frame**: a reference frame in which Newton's laws of motion hold (e.g. the ground can be regarded as an inertial frame to a good approximation).
*   **Non-inertial frame**: an accelerating reference frame (e.g. a bus braking hard, a rotating merry-go-round).
*   **Inertial force**: a fictitious force introduced so that Newton's laws can still be used inside a non-inertial frame.
    $$\vec{F}_{\text{inertial}} = -m\vec{a}_0$$ ($\vec{a}_0$ is the acceleration of the non-inertial frame relative to the inertial frame; the minus sign means the inertial force is opposite to the acceleration)

### 2-5 Momentum and the Law of Conservation of Momentum
*   **Impulse** $\vec{I}$: the accumulation of force over time.
    $$\vec{I} = \int_{t_1}^{t_2} \vec{F} \mathrm{d}t$$
*   **Impulse–momentum theorem**: the impulse of the net external force equals the increment of the particle's momentum.
    $$\vec{I} = \Delta \vec{p} = m\vec{v}_2 - m\vec{v}_1$$
*   **Law of conservation of momentum**: if the **net external force on a system is zero**, the total momentum of the system stays unchanged.
    $$\sum \vec{p}_{\text{initial}} = \sum \vec{p}_{\text{final}}$$

### 2-6 Work and Energy; the Law of Conservation of Mechanical Energy
*   **Work** $W$: the accumulation of force over space (a scalar).
    $$W = \int_{a}^{b} \vec{F} \cdot \mathrm{d}\vec{r}$$
*   **Work–energy theorem**: the work done by the net external force on a particle equals the increment of its kinetic energy.
    $$W_{\text{net}} = E_{k2} - E_{k1} = \frac{1}{2}mv_2^2 - \frac{1}{2}mv_1^2$$
*   **Conservative forces and potential energy**:
    *   **Conservative force**: a force whose work depends only on the initial and final positions and not on the path (e.g. gravity, spring force, Coulomb force).
    *   **Potential energy** $E_p$: the negative of the work done by the conservative force, i.e. W_in,cons = −ΔE_p. <!-- CN formula preserved for parity: `$W_{\text{内保}} = -\Delta E_p$` -->
*   **Work–energy principle**: the work done by the forces of the system other than the conservative forces (external forces and non-conservative internal forces, such as friction) equals the increment of the mechanical energy of the system.
    $$W_{\text{ext}} + W_{\text{int,non-cons}} = \Delta E_{\text{mech}}$$
*   **Law of conservation of mechanical energy**: when only conservative forces do work, the mechanical energy (kinetic + potential) of the system is conserved.
    $$E_{k1} + E_{p1} = E_{k2} + E_{p2}$$

### 2-7 Center of Mass and the Law of Motion of the Center of Mass
*   **Center of mass (mass center)**: an imaginary balance point representing the mass distribution of the whole system.
    $$\vec{r}_C = \frac{\sum m_i \vec{r}_i}{M}$$
*   **Law of motion of the center of mass**: the **sum of the external forces** on the system determines the acceleration of the center of mass, exactly as if all the mass were concentrated at the center of mass and all the external forces acted on it.
    $$\vec{F}_{\text{net,ext}} = M \vec{a}_C$$

---

## Chapter 3 Rigid-Body Mechanics
> **Beginner's note**: A rigid body is an object "that does not deform". It can not only translate but also "rotate" about an axis. **The trick for this chapter: map the formulas one-to-one onto particle dynamics (the analogy method)!**

### 3-1 to 3-3 Rigid-Body Motion, Moment of Inertia, and the Law of Rotation
*   **Moment of inertia** $I$ (analogous to mass $m$): the physical quantity measuring how hard it is to change the rotation of a rigid body.
    $$I = \int r^2 \mathrm{d}m$$
    *Note: for regular rigid bodies there are classic formulas, e.g. a disk $I = \frac{1}{2}MR^2$, a thin rod rotating about its end $I = \frac{1}{3}ML^2$.*
*   **Torque** $\vec{M}$ (analogous to force $\vec{F}$): the effect that makes a rigid body rotate.
    $$\vec{M} = \vec{r} \times \vec{F} \quad \text{magnitude:} M = rF\sin\theta$$ (moment arm $\times$ force)
*   **Law of rotation** (analogous to $\vec{F}=m\vec{a}$):
    $$M = I\alpha$$ (net external torque = moment of inertia $\times$ angular acceleration)

### 3-4 The Work–Energy Theorem for the Fixed-Axis Rotation of a Rigid Body
*   **Rotational kinetic energy**:
    $$E_{k\text{rot}} = \frac{1}{2}I\omega^2$$
*   **Work done by a torque**:
    $$W = \int_{\theta_1}^{\theta_2} M \mathrm{d}\theta$$
*   **Work–energy theorem for rotation**: the work done by the net external torque equals the increase of the rotational kinetic energy.
    $$W_{\text{net}} = \frac{1}{2}I\omega_2^2 - \frac{1}{2}I\omega_1^2$$

### 3-5 Angular Momentum and the Law of Conservation of Angular Momentum
*   **Angular momentum** $L$ (analogous to momentum $p=mv$):
    $$L = I\omega$$
*   **Angular momentum theorem**: the angular impulse equals the increment of the angular momentum.
    $$\int M \mathrm{d}t = I\omega_2 - I\omega_1$$
*   **Law of conservation of angular momentum**: if the **sum of the external torques on a system is zero**, the total angular momentum of the system stays unchanged.
    $$I_1\omega_1 = I_2\omega_2$$
    *(Classic example: when a figure skater pulls in her arms, the moment of inertia $I$ decreases and the angular velocity $\omega$ surges accordingly.)*

---

# Part Two: Relativity and Mechanical Waves (Chapters 4–6)

## Chapter 4 Special Relativity
> **Beginner's note**: When you move close to the speed of light, classical physics breaks down. Time slows down and space contracts. This is Einstein's wonderful world.

### 4-1 & 4-3 The Two Basic Postulates and the Lorentz Transformation
*   **The two cornerstones of special relativity**:
    1.  **Principle of relativity**: all laws of physics are exactly the same in every inertial frame.
    2.  **Postulate of the constancy of the speed of light**: the speed of light $c$ in vacuum is the same in every inertial frame, independent of the motion of the source and the observer (always $3\times 10^8 \text{ m/s}$).
*   **Lorentz transformation** (converting the spacetime coordinates $(x', y', z', t')$ inside a fast-flying spacecraft into ground coordinates $(x, y, z, t)$):
    $$x = \gamma(x' + vt'), \quad t = \gamma\left(t' + \frac{vx'}{c^2}\right)$$
    where the **Lorentz factor** is
    $$\gamma = \frac{1}{\sqrt{1 - \beta^2}}, \quad \beta = \frac{v}{c}$$ (since the speed $v < c$, we have $\gamma > 1$)

### 4-4 The Spacetime View of Special Relativity
*   **Relativity of simultaneity**: two events at different places that happen "simultaneously" in one inertial frame may "not be simultaneous" when viewed from another inertial frame.
*   **Time dilation (slowed clocks)**: a moving clock runs slower than a clock at rest.
    $$\Delta t = \gamma \Delta \tau = \frac{\Delta \tau}{\sqrt{1 - \frac{v^2}{c^2}}}$$
    *($\Delta \tau$ is the proper time, i.e. the time measured by a clock at rest relative to the place where the events occur.)*
*   **Length contraction (shortened rulers)**: the length of an object along the direction of motion is shortened.
    $$L = \frac{L_0}{\gamma} = L_0 \sqrt{1 - \frac{v^2}{c^2}}$$
    *($L_0$ is the proper length, i.e. the length measured at rest relative to the object. Lengths perpendicular to the direction of motion are unaffected.)*

### 4-5 Relativistic Mass, Momentum, and Energy
*   **Mass–speed relation**: the mass of an object increases as its speed increases.
    $$m = \gamma m_0 = \frac{m_0}{\sqrt{1 - \frac{v^2}{c^2}}}$$ ($m_0$ is the rest mass)
*   **Mass–energy relation**: energy and mass are two sides of the same thing.
    $$E = mc^2$$
*   **Relativistic kinetic energy** $E_k$:
    $$E_k = E - E_0 = mc^2 - m_0c^2 = (\gamma - 1)m_0c^2$$
*   **Momentum–energy relation**:
    $$E^2 = (pc)^2 + (m_0c^2)^2$$

---

## Chapter 5 Mechanical Oscillations
> **Beginner's note**: Oscillation is the back-and-forth motion of an object near its equilibrium position. The most basic, most perfect, and most central oscillation is "simple harmonic motion".

### 5-1 & 5-2 Simple Harmonic Motion and Its Energy
*   **Dynamic characteristic equation**: the force is proportional to the displacement and opposite in direction ($F = -kx$).
    $$\frac{\mathrm{d}^2x}{\mathrm{d}t^2} + \omega^2 x = 0$$
*   **Kinematic equation** (position as a function of time):
    $$x(t) = A\cos(\omega t + \phi)$$
    *   $A$: **amplitude** (the maximum distance from the equilibrium position).
    *   $\omega$: **angular frequency** (the number of oscillations per $2\pi$ seconds). $\omega = \sqrt{\frac{k}{m}}$ (spring oscillator) or $\omega = \sqrt{\frac{g}{L}}$ (simple pendulum).
    *   $\phi$: **initial phase** (determines where the oscillator is at $t=0$ and in which direction it is moving; determine it with the "rotating vector (phasor) method" — extremely useful!).
*   **Velocity and acceleration**:
    $$v(t) = -A\omega\sin(\omega t + \phi)$$
    $$a(t) = -A\omega^2\cos(\omega t + \phi) = -\omega^2 x$$
*   **Energy**: kinetic and potential energy keep converting into each other, but the mechanical energy is conserved.
    $$E = E_k + E_p = \frac{1}{2}mv^2 + \frac{1}{2}kx^2 = \frac{1}{2}kA^2$$ (the total energy is proportional to the square of the amplitude)

### 5-3 & 5-4 Composition of Simple Harmonic Motions
*   **Composition of two simple harmonic motions with the same direction and the same frequency**: the result is still a simple harmonic motion with the **same frequency**.
    *   New amplitude $A = \sqrt{A_1^2 + A_2^2 + 2A_1A_2\cos(\phi_2 - \phi_1)}$
    *   **The phase difference $\Delta \phi = \phi_2 - \phi_1$ is the soul of the problem**:
        *   When $\Delta \phi = 2k\pi$: the two reinforce each other (in phase), $A = A_1 + A_2$.
        *   When $\Delta \phi = (2k+1)\pi$: the two weaken each other (out of phase), $A = |A_1 - A_2|$.
*   **Composition of two perpendicular simple harmonic motions**: all kinds of closed, elegant trajectories appear, called **Lissajous figures**.

### 5-5 Damped Oscillation, Forced Oscillation, and Resonance
*   **Damped oscillation**: because of resistance, the amplitude keeps decaying with time.
*   **Forced oscillation**: the oscillation of a system under an applied periodic driving force $F = F_0\cos\omega_d t$.
*   **Resonance**: when the driving frequency $\omega_d$ is extremely close to the natural frequency $\omega_0$ of the system, the amplitude reaches a peak (e.g. a bridge swaying violently in the wind and collapsing).

---

## Chapter 6 Mechanical Waves
> **Beginner's note**: A wave is "the propagation of oscillation". The points of the medium themselves do not drift along with the wave; they only "oscillate in place" near their equilibrium positions, but they pass the energy and the waveform onward.

### 6-1 Generation and Propagation of Mechanical Waves
*   **Conditions for generation**: a wave source + an elastic medium.
*   **Transverse and longitudinal waves**:
    *   Transverse wave: the vibration direction of the medium particles is **perpendicular** to the propagation direction of the wave (e.g. a wave on a rope).
    *   Longitudinal wave: the vibration direction of the medium particles is **parallel** to the propagation direction of the wave (e.g. sound waves, spring waves).
*   **The universal formula for the wave speed $u$, wavelength $\lambda$, period $T$, and frequency $\nu$**:
    $$u = \frac{\lambda}{T} = \lambda \nu$$

### 6-2 The Wave Equation (Wave Function) of a Plane Simple Harmonic Wave
*   **Wave equation**: gives the displacement, at any time $t$, of the particle at any position $x$ in the medium.
    $$y(x,t) = A\cos\left[\omega\left(t - \frac{x}{u}\right) + \phi\right]$$
    *Beginner's way to understand it: keep the "wave equation" and the "oscillation equation" apart.*
    *   *Fix $x$: this is an ordinary simple harmonic motion (the oscillation equation).*
    *   *Fix $t$: this is a full-length snapshot of the wave at that instant (the waveform graph).*

### 6-3 Wave Energy and Energy Flux Density
*   **The process of wave propagation is precisely the process of energy transfer.**
*   **Energy density $w$**: the mechanical energy of the wave per unit volume of the medium (the kinetic and potential energies reach their maximum at the same time, and their minimum at the same time!).
*   **Energy flux density (intensity of the wave) $I$**: the energy passing per unit time through a unit area perpendicular to the wave speed.
    $$I = w u \propto A^2$$

### 6-4 & 6-5 Diffraction, Interference, and Standing Waves
*   **Diffraction**: the ability of a wave to bend around obstacles and keep propagating (the longer the wavelength, the more pronounced the diffraction).
*   **Interference**: when two coherent waves with the same frequency, the same vibration direction, and a constant phase difference meet, the vibration is permanently reinforced at some places and permanently weakened at others.
    *   **Judging by the path difference $\Delta r = r_2 - r_1$**:
        *   When $\Delta r = k\lambda$: interference maximum (reinforced).
        *   When $\Delta r = (2k+1)\frac{\lambda}{2}$: interference minimum (weakened).
*   **Standing wave**: the superposition of two coherent waves with the same amplitude, the same frequency, and opposite propagation directions. It looks like "a wave that stands still".
    *   **Antinode**: a point of maximum amplitude; **node**: a completely motionless point (zero amplitude).
    *   **Half-wave loss**: when a wave travels from a wave-rarer medium (e.g. air) toward a wave-denser medium (e.g. glass) and is reflected, the phase of the reflected wave jumps by $\pi$ (equivalent to losing half a wavelength $\frac{\lambda}{2}$ for nothing).

### 6-6 The Doppler Effect
*   **Core phenomenon**: when there is relative motion between the wave source and the observer, the frequency $\nu'$ received by the observer differs from the frequency $\nu$ emitted by the source.
    $$\nu' = \nu \left( \frac{u \pm v_0}{u \mp v_s} \right)$$
    *($v_0$ is the speed of the observer, $v_s$ the speed of the source. Remember the rule: **approaching each other — the received frequency rises (use "+" in the numerator, "-" in the denominator); moving apart — the received frequency falls (use "-" in the numerator, "+" in the denominator).**)*

---

# Part Three: Fundamentals of Thermal Physics (Chapters 7–8)

## Chapter 7 Kinetic Theory of Gases
> **Beginner's note**: At the microscopic level, thermal phenomena are extremely complicated. Since we cannot keep track of every moving molecule, we use **statistical methods** to link the microscopic motion (molecular speeds) with macroscopic quantities (temperature, pressure).

### 7-1 & 7-2 The Equation of State of an Ideal Gas and the Pressure Formula
*   **Equation of state** (describing the macroscopic state $P, V, T$):
    $$PV = N k_B T = n R T$$
    *($k_B$ is the Boltzmann constant, $R$ is the universal gas constant.)*
*   **The microscopic nature of pressure**: the average impact force produced by huge numbers of molecules bombarding the container walls.
    $$P = \frac{2}{3} n \bar{E}_k$$ ($n$ is the number density of molecules, $\bar{E}_k$ is the average translational kinetic energy of a molecule)

### 7-3 & 7-4 The Microscopic Nature of Temperature and the Equipartition Theorem
*   **The nature of temperature**: temperature is the unique measure of the average translational kinetic energy of molecules.
    $$\bar{E}_k = \frac{3}{2} k_B T$$ (the higher the temperature, the more violent the molecular motion)
*   **Degrees of freedom $i$**: the minimum number of independent coordinates needed to determine the spatial position of a molecule.
    *   Monatomic molecules (e.g. helium He): $i = 3$ (3 translational)
    *   Rigid diatomic molecules (e.g. oxygen $\text{O}_2$): $i = 5$ (3 translational + 2 rotational)
    *   Polyatomic molecules (e.g. water $\text{H}_2\text{O}$): $i = 6$ (3 translational + 3 rotational)
*   **Equipartition theorem of energy**: in equilibrium at temperature $T$, every degree of freedom of a molecule carries on average $\frac{1}{2}k_B T$ of energy.
    *   **Average total kinetic energy of one molecule**: $\bar{\varepsilon} = \frac{i}{2}k_B T$
    *   **Internal energy of an ideal gas** $E$ (1 mole):
        $$E = \frac{i}{2}RT$$

### 7-5 & 7-6 The Maxwell Speed Distribution of Gas Molecules
*   At a given temperature, the molecular speeds of a gas are not all the same; they follow a bell-shaped distribution that is "low at both ends and high in the middle".
*   **Three extremely important characteristic speeds** (in order of size: most probable < mean < root-mean-square):
    1.  **Most probable speed** $v_p$ (the value at the peak of the distribution curve):
        $$v_p = \sqrt{\frac{2RT}{M_{\text{mol}}}}$$
    2.  **Mean speed** $\bar{v}$:
        $$\bar{v} = \sqrt{\frac{8RT}{\pi M_{\text{mol}}}}$$
    3.  **Root-mean-square speed** $\sqrt{\bar{v}^2}$:
        $$\sqrt{\bar{v}^2} = \sqrt{\frac{3RT}{M_{\text{mol}}}}$$

### 7-7 & 7-8 Mean Collision Frequency, Mean Free Path, and Transport Phenomena
*   **Mean free path** $\bar{\lambda}$: the average distance a molecule travels between two consecutive collisions.
    $$\bar{\lambda} \propto \frac{1}{P}$$ (the higher the pressure and the denser the molecules, the more frequent the collisions and the shorter the free path)

---

## Chapter 8 Fundamentals of Thermodynamics
> **Beginner's note**: The kinetic theory of gases starts from the microscopic picture, whereas thermodynamics is macroscopic — a science built on energy conservation and directionality.

### 8-1 Quasi-static Processes
*   **Quasi-static process**: a process carried out so slowly that every intermediate state is extremely close to an equilibrium state. Only for a quasi-static process can we draw a complete, continuous process curve on a $P-V$ diagram.

### 8-2 The First Law of Thermodynamics (Energy Conservation)
*   **System form of the first law of thermodynamics**: of the heat absorbed by a system, one part is used to do work on the surroundings, and the remaining part increases the internal energy of the system itself.
    $$Q = \Delta E + W$$
*   **How to compute the three basic quantities**:
    1.  **Change of internal energy** (depends only on the initial and final temperatures, not on the process):
        $$\Delta E = \nu \frac{i}{2} R \Delta T$$
    2.  **Work** $W$ (just the area under the $P-V$ curve):
        $$W = \int_{V_1}^{V_2} P \mathrm{d}V$$
    3.  **Heat** $Q$: usually obtained backwards from the first law, $Q = \Delta E + W$.

*   **Four special thermodynamic processes**:
| Process | Feature | Work $W$ | First-law expression |
| :--- | :--- | :--- | :--- |
| **Isochoric process** | $V=\text{const}, \mathrm{d}V=0$ | $W = 0$ | $Q_V = \Delta E = \nu C_V \Delta T$ |
| **Isobaric process** | $P=\text{const}$ | $W = P(V_2 - V_1)$ | $Q_P = \Delta E + W = \nu C_P \Delta T$ |
| **Isothermal process** | $T=\text{const}, \Delta E=0$ | $W = \nu R T \ln\frac{V_2}{V_1}$ | $Q = W$ |
| **Adiabatic process** | $Q = 0$ (no heat exchange with the surroundings) | $W = -\Delta E$ | $\Delta E + W = 0$ and $P V^\gamma = \text{const}$ |
*(where $\gamma = \frac{C_P}{C_V} = \frac{i+2}{i}$ is the ratio of heat capacities)*

### 8-3 Cyclic Processes and the Carnot Cycle
*   **Cyclic process**: the system goes through a series of state changes and then returns to its initial state ($\Delta E = 0$).
    *   **Heat-engine cycle (clockwise)**: absorbs heat and converts it into mechanical energy, doing positive work on the outside.
        *   Efficiency: η = W/Q_in = (Q_in − Q_out)/Q_in = 1 − Q_out/Q_in <!-- CN formula preserved for parity: `$\eta = \frac{W}{Q_{\text{吸}}} = \frac{Q_{\text{吸}} - Q_{\text{放}}}{Q_{\text{吸}}} = 1 - \frac{Q_{\text{放}}}{Q_{\text{吸}}}$` -->
    *   **Refrigerator cycle (counterclockwise)**: consumes external work to move heat from a low-temperature place to a high-temperature place.
        *   Coefficient of performance: w = Q_out / W_ext <!-- CN formula preserved for parity: `$w = \frac{Q_{\text{放}}}{W_{\text{外界}}}$` -->
*   **Carnot cycle** (the most perfect, limiting cycle working between two temperatures $T_1$ and $T_2$, consisting of two isothermal and two adiabatic processes):
    $$\eta_{\text{Carnot}} = 1 - \frac{T_{\text{low}}}{T_{\text{high}}}$$

### 8-4 & 8-5 The Second Law of Thermodynamics and Entropy
*   **Classic statements of the second law of thermodynamics** (showing that thermal phenomena have a direction):
    *   **Kelvin statement**: it is impossible to extract heat from a single heat source and convert it completely into useful work without producing other effects (a perpetual-motion machine of the second kind cannot be built).
    *   **Clausius statement**: heat cannot spontaneously flow from a low-temperature body to a high-temperature body without causing changes elsewhere.
*   **Microscopic statistical meaning**: spontaneous processes in an isolated system always proceed from states of **low probability** (ordered) to states of **high probability** (disordered, chaotic).
*   **Entropy** $S$: the physical quantity measuring the degree of disorder (chaos) of a system.
    *   **Boltzmann's entropy formula**:
        $$S = k_B \ln \Omega$$ ($\Omega$ is the number of microstates)
    *   **Principle of entropy increase**: for any spontaneous process in an isolated system, the entropy of the system never decreases.
        $$\Delta S \ge 0$$

---

# Part Four: Fundamentals of Electromagnetism (Chapters 9–12)

## Chapter 9 Electrostatic Field
> **Beginner's note**: A charge creates an "electrostatic field" around itself. We will understand it from two angles: the **vector angle (electric field strength)** and the **scalar angle (electric potential)**.

### 9-1 Electric Field Strength
*   **Coulomb's law**:
    $$\vec{F} = \frac{1}{4\pi\varepsilon_0}\frac{q_1 q_2}{r^2}\vec{e}_r$$
*   **Electric field strength** $\vec{E}$ (the electric force on a test charge divided by its charge):
    $$\vec{E} = \frac{\vec{F}}{q_0}$$
*   **Summation method for continuously distributed charge**: cut the charged body into infinitely many charge elements $\mathrm{d}q$, and integrate (superpose) the field of every $\mathrm{d}q$.
    $$\vec{E} = \int \frac{\mathrm{d}q}{4\pi\varepsilon_0 r^2} \vec{e}_r$$

### 9-2 Gauss's Law
*   **Electric flux** $\Phi_e$ (the number of electric field lines passing through a given area):
    $$\Phi_e = \int_S \vec{E} \cdot \mathrm{d}\vec{S}$$
*   **Gauss's law (Maxwell's first equation)**: the electric flux through any closed surface depends only on the total charge enclosed **inside** that closed surface.
    $$\oint_{S} \vec{E} \cdot \mathrm{d}\vec{S} = \frac{\sum q_{\text{enclosed}}}{\varepsilon_0}$$
    *(Beginner's guide: Gauss's law is the magic weapon that makes short work of highly symmetric field problems, such as a uniformly charged sphere, an infinitely long charged line, or an infinite charged plane.)*

### 9-3 The Circuital Theorem of the Electrostatic Field and Electric Potential
*   **Circuital theorem of the electrostatic field**: moving a charge once around any closed path, the work done by the electric force is always zero (which shows that the electrostatic field is a **conservative/irrotational field**).
    $$\oint \vec{E} \cdot \mathrm{d}\vec{l} = 0$$
*   **Electric potential** $V$ (the ratio of the work done by the electric force to the charge, from a point to the zero-potential reference point):
    $$V_a = \int_{a}^{P_0(\text{reference point})} \vec{E} \cdot \mathrm{d}\vec{l}$$
*   **Differential relation between electric potential and field strength** (the field strength is the negative gradient of the potential):
    $$\vec{E} = -\nabla V$$

### 9-4 to 9-7 Conductors, Dielectrics, and Capacitors
*   **Properties of a conductor in electrostatic equilibrium**:
    1.  The electric field strength inside the conductor is zero everywhere (E_inside = 0). <!-- CN formula preserved for parity: `$\vec{E}_{\text{内}} = 0$` -->
    2.  The conductor is an equipotential body, and its surface is an equipotential surface.
    3.  There is no net charge inside the conductor; the net charge distributes only on the outer surface of the conductor (the charge density is largest at sharp protrusions — the "point discharge" effect).
*   **Polarization of dielectrics**: an applied electric field creates polarization charges (bound charges) inside the insulating medium; these polarization charges produce a reverse field, so the total field inside the medium is **weakened**.
*   **Capacitance** $C$ (the ability to hold charge):
    $$C = \frac{Q}{U}$$
    *(For a parallel-plate capacitor $C = \frac{\varepsilon_r \varepsilon_0 S}{d}$.)*

### 9-8 Energy of the Electrostatic Field
*   Energy is stored in the electric field.
*   **Energy density of the electric field** $w_e$:
    $$w_e = \frac{1}{2} D E = \frac{1}{2} \varepsilon E^2$$
*   **Total energy of the field**: integrate over the whole volume of the field:
    $$W_e = \int_V w_e \mathrm{d}V$$

---

## Chapter 10 Steady Magnetic Field
> **Beginner's note**: Moving charges (currents) create magnetic fields. The magnetic field has only a vector character (magnetic induction), and it is a **source-free, rotational** field.

### 10-1 & 10-2 Steady Current and Electromotive Force
*   **Current intensity** $I = \frac{\mathrm{d}q}{\mathrm{d}t}$; **current density** $\vec{j}$.
*   **Electromotive force** $\mathcal{E}$: the work done by the non-electrostatic force in moving a unit positive charge from the negative terminal to the positive terminal.

### 10-3 & 10-4 Magnetic Induction and the Biot–Savart Law
*   **Biot–Savart law** (computing the magnetic field produced by a small current element $\mathrm{d}l$):
    $$\mathrm{d}\vec{B} = \frac{\mu_0}{4\pi} \frac{I\mathrm{d}\vec{l} \times \vec{e}_r}{r^2}$$
    *(Two classic fields to master: the field of an infinitely long straight wire $B = \frac{\mu_0 I}{2\pi r}$; the field at the center of a circular current $B = \frac{\mu_0 I}{2 R}$.)*

### 10-5 & 10-6 Gauss's Law for Magnetism and Ampère's Circuital Law
*   **Gauss's law for magnetism**: since isolated magnetic charge (magnetic monopoles) does not exist in nature, the net magnetic flux through any closed surface must always be zero (which shows that the magnetic field is **source-free**).
    $$\oint_S \vec{B} \cdot \mathrm{d}\vec{S} = 0$$
*   **Ampère's circuital law**: the line integral of the magnetic field along any closed loop equals the algebraic sum of the currents passing through the surface bounded by that loop (which shows that the magnetic field is **rotational**).
    $$\oint_L \vec{B} \cdot \mathrm{d}\vec{l} = \mu_0 \sum I_{\text{enclosed}}$$
    *(Another magic weapon for making short work of highly symmetric fields, such as infinitely long solenoids and coaxial cables!)*

### 10-7 & 10-8 Magnetic Forces on Current-Carrying Wires and Moving Charges
*   **Lorentz force** (the force exerted by a magnetic field on a moving charge):
    $$\vec{F} = q\vec{v} \times \vec{B}$$ (the direction is determined by the left-hand rule or the cross product; since the force is always perpendicular to the velocity, **the Lorentz force never does work**!)
*   **Ampère force** (the force exerted by a magnetic field on a current-carrying wire; in essence the macroscopic manifestation of a huge number of Lorentz forces):
    $$\mathrm{d}\vec{F} = I\mathrm{d}\vec{l} \times \vec{B}$$

---

## Chapter 11 Electromagnetic Induction
> **Beginner's note**: The great discovery that "magnetism generates electricity". As long as the magnetic flux through a closed loop changes, an induced current appears in the loop.

### 11-1 The Law of Electromagnetic Induction
*   **Faraday's law of induction**: the magnitude of the induced emf is proportional to the rate of change of the magnetic flux through the loop.
    $$\mathcal{E} = -\frac{\mathrm{d}\Phi_m}{\mathrm{d}t}$$
    *(The minus sign in the formula is **Lenz's law**: the effect produced by the induced current always opposes the change of magnetic flux that causes it.)*

### 11-2 Motional emf and Induced emf
*   There are two possible ways for the magnetic flux to change, corresponding to two kinds of emf:
    1.  **Motional emf**: the magnetic field stays unchanged while the wire moves through it, cutting the field lines. It arises because the Lorentz force pushes the free charges inside the conductor.
        $$\mathcal{E}_{\text{motional}} = \int (\vec{v} \times \vec{B}) \cdot \mathrm{d}\vec{l}$$
    2.  **Induced emf**: the conductor stays still while the magnetic field changes. It drives the charges through a new kind of electric field excited by the changing magnetic field — the **induced electric field (vortex electric field)** $\vec{E}_g$.
        $$\oint \vec{E}_g \cdot \mathrm{d}\vec{l} = -\frac{\mathrm{d}}{\mathrm{d}t} \int_S \vec{B} \cdot \mathrm{d}\vec{S}$$

### 11-3 & 11-4 Self-Inductance, Mutual Inductance, and RL/RC Circuits
*   **Self-inductance** $L$: a changing current in a circuit induces an emf in the circuit itself.
    $$\mathcal{E}_L = -L \frac{\mathrm{d}I}{\mathrm{d}t}$$
*   **Magnetic field energy**: the magnetic energy stored in a self-inducting coil:
    $$W_m = \frac{1}{2} L I^2$$
*   **RL/RC circuits**: because a capacitor opposes sudden voltage changes and an inductor opposes sudden current changes, there is a transient charging/discharging process when a switch opens or closes, and the variation decays exponentially: $e^{-t/\tau}$ ($\tau$ is the time constant; for an RC circuit $\tau=RC$, for an RL circuit $\tau=L/R$).

---

## Chapter 12 Electromagnetic Fields and Electromagnetic Waves
> **Beginner's note**: Maxwell fused electricity and magnetism perfectly into one whole, predicting and confirming the existence of electromagnetic waves.

### 12-1 Maxwell's Equations
By introducing two brilliant corrections, Maxwell summarized the set of equations that governs the entire macroscopic electromagnetic world:
*   **Displacement current hypothesis**: a changing electric field (flux) also produces a magnetic field in an equivalent way, thereby correcting Ampère's circuital law.
    $$I_D = \varepsilon_0 \frac{\mathrm{d}\Phi_e}{\mathrm{d}t}$$
*   **Maxwell's equations (integral form)**:
    1.  $$\oint_S \vec{E} \cdot \mathrm{d}\vec{S} = \frac{\sum q}{\varepsilon_0}$$ (there are charge sources)
    2.  $$\oint_S \vec{B} \cdot \mathrm{d}\vec{S} = 0$$ (no magnetic monopoles)
    3.  $$\oint_L \vec{E} \cdot \mathrm{d}\vec{l} = -\frac{\partial \Phi_m}{\partial t}$$ (a changing magnetic field generates an electric field)
    4.  $$\oint_L \vec{B} \cdot \mathrm{d}\vec{l} = \mu_0 \left( I + \varepsilon_0 \frac{\partial \Phi_e}{\partial t} \right)$$ (changing electric fields and changing currents generate a magnetic field)

### 12-2 Electromagnetic Waves
*   The electromagnetic field alternately regenerates itself in space and propagates outward, forming an electromagnetic wave. Its propagation speed is exactly the speed of light:
    $$v = \frac{1}{\sqrt{\mu\varepsilon}} \implies c = \frac{1}{\sqrt{\mu_0\varepsilon_0}}$$ (revealing that **light is also an electromagnetic wave**).

---

# Part Five: Wave Optics (Chapter 13)

## Chapter 13 Optics
> **Beginner's note**: On the macroscopic scale light travels in straight lines, but on the microscopic scale it reveals the properties of a wave.

### 13-1 to 13-5 Interference of Light
*   **Young's double-slit interference**: coherent light passes through a double slit and meets on a screen, forming alternating bright and dark fringes.
    *   Center positions of the bright fringes: $x = \pm k \frac{D}{d}\lambda$
    *   Fringe spacing: $\Delta x = \frac{D}{d}\lambda$
*   **Thin-film interference**: a light beam reflected from the upper and lower surfaces of a thin film meets again and interferes (e.g. the colored patterns reflected by a soap bubble).
    *   **Don't forget the "half-wave loss"!** When a half-wave loss occurs, an extra $\frac{\lambda}{2}$ must be added to or subtracted from the optical path difference formula.
*   **Air-wedge interference and Newton's rings**: characteristic interference fringes produced by a film such as an air layer whose thickness increases linearly or along an arc.

### 13-6 to 13-9 Diffraction of Light
*   **Single-slit diffraction**: light bends around the edges of a narrow slit, spreads on the screen, and forms a very wide central fringe with extremely narrow side fringes.
    *   Analyze with the "**half-wave zone method**":
        *   Dark-fringe condition: $a\sin\theta = \pm k\lambda$
        *   Bright-fringe condition: $a\sin\theta = \pm (2k+1)\frac{\lambda}{2}$
*   **Grating diffraction**: a device made of a large number of parallel slits of equal width and equal spacing. Its fringes are extremely bright, extremely sharp, and widely separated.
    *   Grating equation: $(d+b)\sin\theta = \pm k\lambda$
*   **Resolution of optical instruments (Rayleigh criterion)**: limited by diffraction, two light points cannot be resolved if they are too close together. The minimum resolvable angle limited by circular-aperture diffraction:
    $$\theta_{\text{min}} = 1.22 \frac{\lambda}{D}$$ ($D$ is the aperture diameter. The larger the aperture, the higher the resolution)

### 13-11 to 13-13 Polarization of Light
*   **Natural light and polarized light**: the light vector of natural light vibrates uniformly in all directions; the light vector of polarized light (e.g. linearly polarized light) vibrates in only one direction.
*   **Malus's law** (the change of intensity when polarized light passes through a polarizer):
    $$I = I_0 \cos^2\alpha$$
*   **Polarization by reflection (Brewster's law)**: when natural light is incident on the surface of a medium at the special **Brewster angle** $i_0$, the reflected light becomes purely linearly polarized, with its vibration direction perpendicular to the plane of incidence.
    $$\tan i_0 = \frac{n_2}{n_1}$$

---

# Part Six: Fundamentals of Quantum Physics (Chapter 14)

## Chapter 14 Fundamentals of Quantum Physics
> **Beginner's note**: Deep in the microscopic world (atoms, electrons), neither energy nor states are continuous any more — they are quantized "packet by packet". Here, waves are particles and particles are waves.

### 14-1 Blackbody Radiation and Planck's Energy-Quantum Hypothesis
*   **The blackbody-radiation crisis**: classical physics fails completely when explaining the high-frequency part of blackbody radiation (the "ultraviolet catastrophe").
*   **Planck's hypothesis**: the energy of a charged harmonic oscillator in a radiating source cannot change continuously; it can only be an integer multiple of a smallest energy unit — the "energy quantum".
    $$E = h \nu$$ ($h$ is Planck's constant)

### 14-2 The Photoelectric Effect and Einstein's Photon Hypothesis
*   **Photoelectric effect**: light shining on a metal surface knocks electrons out. Classical physics cannot explain why "no electrons are emitted when the light is too weak, and the effect is independent of the illumination time".
*   **Einstein's photon hypothesis**: a beam of light is a stream of photons, each carrying the energy $E=h\nu$.
*   **Einstein's photoelectric equation**:
    $$h\nu = A_{\text{work function}} + \frac{1}{2}m v_{\text{max}}^2$$ (photon energy = work function + maximum initial kinetic energy of the electron)

### 14-3 The Compton Effect
*   **Experimental phenomenon**: when X-rays are scattered, their wavelength increases. This proves that **a photon has not only energy but also momentum, like a real particle**.
*   Photon momentum formula:
    $$p = \frac{h}{\lambda}$$

### 14-4 The Hydrogen Atomic Spectrum and Bohr's Theory
*   **The three postulates of Bohr's hydrogen model**:
    1.  **Stationary-state postulate**: an atom can only orbit on a series of stable tracks that do not radiate electromagnetic waves.
    2.  **Transition postulate**: when an atom transitions between stationary states on different tracks, the energy of the absorbed or emitted photon equals the difference between the two energy levels:
        $$h\nu = E_n - E_k$$
    3.  **Angular-momentum quantization postulate**:
        $$L = mvr = n \frac{h}{2\pi}$$ ($n=1,2,3...$ is called the principal quantum number)

### 14-5 & 14-6 de Broglie Waves and the Uncertainty Relation
*   **de Broglie waves (matter waves)**: not only light has wave–particle duality; all material particles (e.g. electrons, protons) also have wave nature.
    $$\lambda = \frac{h}{p}, \quad \nu = \frac{E}{h}$$
*   **Heisenberg's uncertainty relation**: you cannot measure the position $x$ and the momentum $p_x$ of a microscopic particle both with extreme precision at the same time.
    $$\Delta x \cdot \Delta p_x \ge \frac{h}{4\pi}$$ (this is dictated by the wave nature itself, not by the error of experimental apparatus)

### 14-7 to 14-10 The Wave Function, the Schrödinger Equation, and Atomic Energy Levels
*   **Wave function** $\Psi(x, y, z, t)$: describes the state of a microscopic particle. Because the particle has wave–particle duality, its position is a probability distribution.
    *   **Probability density** $|\Psi|^2$: how likely the particle is to appear at a given place.
*   **Schrödinger equation** (the core of quantum mechanics, analogous to Newton's second law):
    $$i\hbar \frac{\partial}{\partial t}\Psi = -\frac{\hbar^2}{2m}\nabla^2\Psi + U\Psi$$
*   The energy of a particle **in a one-dimensional potential well** is confined to discrete tracks, which explains the very origin of quantization.

---

### 💡 Universal Exam-Clearing Tips for Reviewing University Physics:
1.  **Calculus is the foundation**: whenever you meet a quantity that "varies with position/time", be sure to write out the infinitesimal expression (e.g. $\mathrm{d}W = \vec{F} \cdot \mathrm{d}\vec{r}$), set up the integration limits, and integrate — do not blindly reuse high-school physics formulas.
2.  **Vector nature comes first**: force, displacement, the electric field $\vec{E}$ and the magnetic field $\vec{B}$ all have directions; drawing diagrams with force analysis and setting up coordinate systems is the core of long-answer physics problems.
3.  **Mind the conditions of the conservation laws**: conservation of momentum (net external force zero), conservation of mechanical energy (only conservative forces do work), conservation of angular momentum (net external torque zero) — state your justification before starting a long problem, and you will earn the step marks!
