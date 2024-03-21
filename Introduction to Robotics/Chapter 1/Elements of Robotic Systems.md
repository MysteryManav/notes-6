- **Manipulator or Rover**: This is the main body of the robot, which consists of the links, joints, and other structural elements of the robot. Without other elements, the manipulator alone is not a robot
- **End Effector**: The part that is connected to the last joint (hand) of a manipulator and that generally handles objects, makes connection to other machines, or performs required tasks
- **Actuators**: They are the muscles of the manipulators. The controller sends the signals to the actuators, which in turn move the robot's joints and links. Example: Servo Motors, Stepper Motors, Pneumatic and Hydraulic Actuators, etc.
- **Sensors**: They are used to collect information about the internal state of the robot or to communicate with the outside environment. Example: Light, Sound, Temperature, Pressure, etc.
- **Controller**: The controller is like cerebellum, although it does not have power of the brain, it *controls the motions*. The controller receives data from processor, controls the motions of the actuators, and co-ordinates the motions with the sensory feedback information
- **Processor**: It is the brain of the robot. It calculates the motions of the robots joints based on the program it runs, determines, how much and how fast each joint must move to achieve the desired location and speeds, and oversees the coordinated actions of the controller and the sensors
- **Software**: Three groups of software programs are used in robot:
	1. *Operating System*: Operates the processor
	2. *Robotic Software*: Calculates necessary motions of each joint based on kinematic equations of robot. This information is sent to controller
	3. *Collection of Application Oriented Routines and programs*: It is developed in order to use the robot or its peripherals for specific tasks, like assembly, machine loading, material handling, etc.
