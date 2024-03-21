### Programming Modes:
- **Physical Setup**: An operator sets up switches and hard stops that control the motions of the robot. Usually used along with other devices like P.L.Cs
- **Lead-Through or Teach Mode**: Robot's joints are moved with a teach pendant. When desired location and orientation is achieved, the location is entered into controller. During playback, controller moves the joints to same locations and orientations
- **Continuous walk-through Mode**: All robot joints are moved simultaneously, while the motion is continuously sampled and recorded by controller. Motions are taught by an operator, either through a model, by physically moving the end effector, or by "wearing" a robot arm and moving it through its workspace
- **Software Mode**: A program is written offline or online and is expected by controller to control the motions. It is the most sophisticated and versatile mode and can include sensory information, etc.

### Robot Languages:
- They range from machine level to a proposed human intelligence level. High-level languages are either interpreter-based or compiler-based
- **Interpreter-Based Languages**:
	1. Execute one line at a time
	2. Example: OMRON Adept V
- **Compiler-Based Languages**:
	1. Compiler translates whole program into machine language
	2. Faster and Efficient
- **Micro controller Machine Level Language**: Programs in machine language
- **Point-to-point**: Coordinates of points are entered sequentially, and robot follows points as specified
- **Primitive Motion Level**: Possible to develop more-sophisticated programs. Most languages are interpreter-based
- **Structured programming level**: Most languages are compiler-based, powerful and allow more sophisticated programming
- **Task Oriented Level**: Allow user to command desired sub-goals of task directly, rather than specify details of every action the robot is to take. User is able to include instructions in application program at a significantly higher level than in an explicit robot programming language
