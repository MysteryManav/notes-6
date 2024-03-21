### Definition:
- Actuators are generators of forces that robots employ to move themselves and other objects. All actuators are energy consuming mechanisms that convert various forms of stored energy into mechanical work
- Some of the commonly used types of actuators are:
	1. *Electric Motors*: Most Commonly used Robotic Actuators, especially Servo Motors
		- Servo Motors: Serve or Slave Motor, adjusts through feedback
		- Stepper Motors: Uses Digital Pulse as an input
		- Direct-Drive Electric Motors: Transmits torque directly
	2. Hydraulic Actuators: Very popular for large robots, but are no longer popular, except for specific applications
	3. Pneumatic Actuators: Used for robots with half degree of freedom or on-off joints, as well as insertion purposes
	4. Novelty Actuators: Mostly used in research and development work or as speciality items for specific purposes. Examples: Direct-Drive Electric motors, Piezo-electric motors

### Characteristics of Actuating Systems:
- Actuator must have enough power to accelerate and decelerate the links and carry the loads
- It must be light, economical, accurate, responsive, reliable, easy to maintain
- Nominal Characteristics are important and should be considered: Weight, Power, Power-to-Weight Ratio, Operating Pressure, Operating Voltage, Temperatures, etc.
- Hydraulic systems have *highest* power-to-weight ratio
- Electric systems have *average* power-to-weight ratio
- Pneumatic Systems deliver *lowest* power-to-weight ratio
- Stepper motors are generally heavier than servo motors for same power and therefore, have a lower power-to-weight ratio
- Hydraulic Systems deliver very high range powers: 50-5000 psi (0.345 to 34.5 MPa); due to high operating pressure
- Pneumatic Cylinders operate around 100-120 psi (0.69 to 0.83 MPa)
- Electric motors operate at high voltage for a better power-to-weight ratio

### Stiffness vs. Compliance:
- **Stiffness**: It is the resistance of a material against deformation
- A stiffer system requires a larger load to deform. Conversely, a more compliant system requires a smaller load to deform
- It is directly related to bulk modulus of elasticity of the material
- There has to be a balance between stiffness and compliance

### Reduction Gear:
- Most motors have fixed range of rotational speed and torque that is most efficient for operation
- However, the work that needs to be done generally requires much lower speeds and higher torque
- A reduction gear can be used to reduce the speed and increase the torque of motor output
- **Key Terms**: Power, Torque, Angular Speed, Gears
- Reduction Gear is an arrangement of gears that reduce the no. of rotations of a power source such as a motor. The arrangement also has the effect of increasing the amount of torque
- The simplest reduction gear arrangement is a combination of two gears: One on input and other on output
- The ratio of number of teeth is called reduction ratio

### Reduction Gear - Brief Analysis:
- Effective inertia of load felt by motor is conversely proportional to square of reduction gear ratio

### Electric Motors:
- When a conductor carrying a current is placed within a magnetic field, it experiences an emf normal to plane formed by magnetic field and current
- Each side of wire experiences a force, and continually passing the current through each conductor can force them to rotate
- Either the direction of current or magnetic poles need to switch or interchange for continuous motion, hence, a *split ring commutator* is used

### Fundamental Difference Between A.C. and D.C. Motors:
- **Control on Speed**:
	- AC: Speed of an AC motor is a function of frequency of supplied AC power. Since frequency of AC power is constant, Speed of a synchronous A.C. motor is generally constant
	- DC: Speed of a DC motor can be controlled by changing the current of windings. As the current increases or decreases, the speed increases or decreases
- **Brush vs. Brushless**:
	- All AC motors are brushless
	- DC motors are both brush and brushless
- **Heat Dissipation**:
	- Heat is generated primarily from resistance of wiring to electric current, and also includes heat due to iron losses, eddy current losses, hysteresis losses, etc.
	- In motors with winding within the rotor, heat is generated in rotor. This heat must travel from rotor, through air gap, through permanent magnets, through motor's body and be dissipated
	- On other hand, motors where winding is withing the stator, the heat is dissipated to air by conduction through motor's body. Hence, the heat-transfer coefficient is relatively high
	- AC: AC motors, stepper motors and brushless DC motors have windings in their stator
	- Overheating may be most common cause of failure of electric motors:
		- Failure of winding isolation: Causing shorts or burnouts
		- Failure of bearings: Jamming the rotor
		- Degradation of magnets: Permanently reducing motor's torque
	- Heat generated in a motor is:$$P_{electric} = i^2R = \frac{T^2}{K^2_t}R_t$$ $K_t$ is the torque constant at temperature t and is a function of magnetic field, no. of turns, effective area of air gap, radius of rotor, material properties, etc. T is torque, t is temperature
	- Variations in winding electrical resistance can be described by:$$R_t = R_{ref}[1 + (t_{winding} - t_{ref})\cdot \alpha]$$
	- Torque constant representing the magnetic field of motor varies with temperature as:$$K_t = K_{ref}[1 + (t_{magnet} - t_{ref})\cdot \beta]$$
	- A simplified model for final temperature of model:$$t_{motor} = (P_{electric} + P_{friction})R_{thermal} + t_{ref}$$
	- **Conclusion**: Motor construction with windings in stator is preferable

### DC Motors:
- Very common
- Sturdy, reliable, relatively powerful
- Mainly consist of *permanent magnet stators*, fixed flux/windings that carry a current and can create a variable flux, rotor that has winding coils that carry current
- If a rotor is forced to rotate within magnetic field, a DC current develops and motor acts as generator (Output is DC, but not constant)

### Back EMF and Power Characteristics:
- When armature of a DC motors rotates under influence of driving torque, armature conductors move through magnetic field and hence EMF is induced in them as in a generator
- The induced EMF acts in opposite direction to applied Voltage and is known as *Back* or *Counter EMF*
- Torque and Angular Velocity is related as:$$T = \frac{k_t}{R}V = \frac{k_t^2}{R}\omega$$

### Brushless DC Motors:
- Brushes have to continuously changed and the commutator resurfaced, hence brushless motors are designed
- They consist of a **coiled stator** and a **permanent magnet rotor**
- They have many advantage over conventional DC motors:
	1. Better heat dissipation
	2. Reduced rotor inertia due to less weight and low mass
	3. More durable and longer life
	4. Low maintenance and related costs
	5. Improved Safety
	6. Quieter Operation

### AC Motors:
- Use Alternating nature of AC power to switch the direction of flux,  hence all commutaors and brushes are unnecessary
- In *synchronous* AC motors, rotor is permanent magnet
- In *induction* AC motor, rotor is a matrix of conductors, either in shape of a cage or a ferric rotor that carries no current
- Since AC motors can dissipate heat more favourably than DC motors, they can be more powerful
- Principles of Back-EMF hold for AC motors as well
- **Single-Phase Squirrel-Cage Induction Motor**:
	- Consists of a squirrel-cage rotor
	- Copper or aluminium bars
	- No external electrical connections to rotor
	- When an alternating current passes through stator windings, an alternative magnetic field is produced, which appears like a rotating magnetic field
	- Rotating field in stator intercepts rotating windings, thereby generating an induced current due to mutual induction
	- Once driven, rotor tries to behave independently, and its rotation rate can be less than rate of rotation of magnetic field in stator, hence, the **slip** caused is given by:$$S = \frac{\omega_f - \omega_m}{\omega_f}$$ $\omega_f$ and  $\omega_m$ are speed of field and rotor, respectively
- **Synchronous Motor** has a stator similar to those described for induction motors, but a rotor is a permanent magnet. The magnetic field produced by stator rotates and so magnet rotates with it
- **Synchronous Motor** are used when a precise speed is required

### AC Motors: Advantages:
- Cheaper
- Convenient power supply
- No commutator and brush mechanism
- Low power dissipation
- Low rotor inertia
- High reliability, robustness
- Easy maintenance
- Long life

### AC Motors: Disadvantages:
- Low starting torque
- Need auxiliary devices to start the motor
- Difficulty of variable-speed control

### Self-Starting:
- **For single phase supply**: When rotor is stationary initially, forces on conductor or rotor in magnetic field of stator are such that no net torque is present, hence it is not self-starting
- To provide starting torque, a main and auxiliary winding is used
- DC Motors are always self starting
- AC Motors are not, except for 3-phase motors

### Stepper Motors:
- Use magnetic pulses emanating from stator to make the rotor spin
- Versatile
- Robust
- Can be used in many applications
- The rate at which pulses are applied determines the motor speed
- Total no. of pulses determines, the angular displacement
- Order of energising of coils determines direction of rotation
- Classified into:
	1. Variable reluctance type
	2. Permanent Magnet
	3. Hybrid Type

### Servo Motors:
- Motors with motion feedback control
- Able to follow a specified motion trajectory
- Feedback allows us to adjust input voltage and current so as to compensate the Back-EMF
- A servo motor is a DC, AC or even a stepper motor with feedback that can be controlled to move at a desired speed and torque for a desired angle of rotation
- Feedback device sends signals to servo-controller circuit reporting its angular position and velocity

### Hydraulic and Pneumatic Actuators:
- **Hydraulic Actuators**: Utilise high-pressure fluid to transmit to the point of application desired
- Designed to operate at much higher pressures (70 to 170 bar)
- Suitable for high power applications
- **Pneumatic Actuators**: Utilise compressed air for the actuation of cylinders

### Comparison: TODO Later
