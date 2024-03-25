- **Machine**: A device for transferring and transforming motion and force or power from input (source) to output (load)
- **Kinematics**: Subject matter which deals with the geometric constraint of relative motion, without any reference to cause of motion (force)
- **Mechanism/Links**: Combination of interconnected rigid bodies capable of relative motion
- **Kinematic Pair**: A connection between two joints, links or elements that enables relative motion or constraint between them
- **Degree of Freedom**: Number of co-ordinates needed to describe the relative movement permitted in a kinematic pair. A completely free, unconnected rigid body in 3-D space, has **6** Degree of Freedom (DoF), three translational and three rotational
- **Pair Variable**: Coordinates used to describe the relative motion in a kinematic pair
- Kinematic pairs are classified into:
	1. **Lower Pair**: Area Contact
	2. **Higher Pair**: Point or Line Contact
	3. **Wrapping Pair**: One body completely wraps over the other
- Another Classification:
	1. Form Closed
	2. Forced Closed

### Types of Lower Pair:
- Revolute (R, 1, $\theta$)
	![[Pasted image 20240324174348.png]]
- Prismatic (P, 1, s)
	![[Pasted image 20240324174419.png]]
- Screw (H, 1, $\theta$)
- Cylindrical (C, 2, $\theta$ and s)
- Spherical or Globular (G or S, 3, $\theta_x, \theta_y, \theta_z$)
- Planar (F, 2, $s_x, s_y$ and $\theta_z$)

### Types of Mechanism:
- **Planar Mechanism**: All points of mechanism move in parallel planes and all these parallel planes can be represented by a single plane, which is called the plane of motion and a single view perpendicular to this plane of motion reveals true motion of all points of a mechanism. In a planar mechanism, all the axes of the pin joints are parallel. *Example*: 4-bar mechanism
- **Spherical Mechanism**: Pin-Jointed spatial linkages used to move an object along a 3-D path in space. A spherical mechanism differs from a planar mechanism in orientation of its axes of revolution *Example*: Hooke's Joint
- **Spatial Mechanism**: If there is any relative motion that is not in same plane or in parallel planes, the mechanism is called *spatial mechanism*. *Example*: Bennett's Linkage

### Types of Problems in Kinematics:
- **Kinematic Analysis**: A mechanism is given and task is to determine various relative motion that can take place in that mechanism. Kinematic Analysis problems can be classified into three headings:
	1. Displacement Analysis
	2. Velocity Analysis
	3. Acceleration Analysis
- **Kinematic Synthesis**: One has to come up with a design of mechanism to generate prescribed required relative motion characteristics

### Simple Planar Mechanisms:
- All points of mechanism move in parallel planes
- A single view along a direction perpendicular to these planes reveal the true motions of all the points of mechanism. All these parallel planes are projected on to a single plane which is called the **Plane Of Motion**
- Each rigid body, contributing elements to form kinematic pair is referred to as a **Link**
- **Kinematic Chain** is defined as a series of links connected by kinematic pairs
- If every link is connected to at least 2 other links, a **kinematic chain is said to be closed**
- If a particular link or some links are connected to only 1 other link, then the chain is said to be an **open** chain
- We call a link:
	- A **Singular Link**: Connected to only 1 other link
	- A **Binary Link**: Connected to 2 other links
	- A **Ternary Link**: Connected to 3 other links and so on
- **Linkage**: A mechanism consisting only of lower pairs
- If there is a higher pair, we rather call it **a mechanism**
- **Constrained Mechanism**: If degrees of freedom of mechanism equals number of independent input. Output can move in unique fashion
- **4R Simple Planar Mechanism**: 
		![[Pasted image 20240324180942.png]]
	- Link 1 => Fixed
	- Link 2 => Input Link
	- Link 4 => Output Link
	- Link 3 => Coupler
	- Joint O2 and Joint O4 => Fixed Pivots
	- Joint A and B => Moving Hinges

### Grashof and Non-Grashof Chains:
- If a chain satisfies Grashof's Criterion, then we call it a **Grashof Chain**, otherwise it is a **Non-Grashof Chain**
- **Grashof Criterion**: $$l_{min} + l_{max} \lt l' + l''$$
- In a Grashof chain, the shortest link can always make complete rotations with respect to all other links
- Hence, in a Grashof Chain, it is often the shortest link and its position in the arrangement that decides kinematic behaviour of the chain

### Kinematic Inversion:
- The process of fixing different links of same kinematic chain to produce distinct mechanism
- The most important thing about this process of kinematic inversion is that the relative motions between various links are independent of kinematic inversion
- Possible Inversion of a 4R Grashof Chain:
	1. If shortest link (crank) adjacent to frame: Crank-Rocker Linkage
	2. If shortest link is coupler: Double Rocker Mechanism
	3. If shortest link is the frame: Double Crank Linkage
	4. The position of longest link with respect to frame, decides the type of rocking movement

### Transition Linkage:
- In transition linkage, $$l_{min} + l_{max} = l' + l''$$
- In general, it behaves just like a Grashof Linkage
- In such linkages, it is obvious that there will be configurations when all the links become collinear, and this collinear configuration is called **Uncertainty Configuration**
- The linkage can move in a non-unique fashion
- Various cases:
	1. **Case 1**: Equal length links are *not adjacent*, it becomes a **parallelogram** chain. All 4 of its inversions are double-crank. With Uncertainty configuration, parallelogram linkage can flip into anti-parallelogram configuration
	2. **Case 2**: Equal length links are **adjacent**, it becomes a **Deltoid** or **Kite Configuration**. We get a crank-rocker if $l_{max}$ is fixed and double-crank if $l_{min}$ is fixed
	3. **Case 3**: If all links are of same length  we get a **Rhombus Linkage**, which is of double crank type

### Mobility Analysis:
- We obtain degrees of freedom of a given mechanism
- This is accomplished by counting number of links and number of different types of kinematic pairs those are used to connect these links
- **Grubler's Criterion**: $$F_{eff} = 3(n - 1) - 2(j - j_r) - h - F_r$$ where,
	- $n$ => Total number of links in mechanism
	- $j$ => Total number of kinematic pairs
	- $j_r$ => Total number of redundant kinematic pairs
	- $h$ => Total number of higher pairs
	- $F_r$ => Total number of redundant degrees of freedom
	- $F_{eff}$ => Effective Degrees of Freedom
- Cases where expression seems to be incorrect:
	1. *No distinction between a revolute pair and prismatic pair*
	2. *When an Extra link is added for better motion transmission*, *example*, adding an extra coupler to parallelogram configuration to avoid the flipping due to uncertainty configuration

### 3R-1P Simple Planar Mechanism
- Consists of: 3 Revolute and 1 Prismatic Pairs
- Common Examples: Offset Slider Crank Mechanism, **Quick Return Mechanism**
### 2R-2P Simple Planar Mechanism
- Consists of: 2 Revolute and 2 Prismatic Pairs
- Possible Sequences: RRPP or RPRP
- Common Examples: Scotch-Yoke Mechanism, **Oldham Coupling**

### Robot Joints
- Mainly two types:
	1. **Linear (Prismatic)**: No rotation involved. Either use hydraulic or pneumatic cylinders or linear electric actuators
	2. **Revolute (Rotary)**: Although Hydraulic and Pneumatic are common, most rotary joints are electrical

### Robot Coordinates
1. **Cartesian/Rectangular/Gantry (3P)**: Use 3 prismatic joints to position end effector
2. **Cylindrical (PRP)**: Consist of 2 prismatic joints and one revolute joint
3. **Spherical (P2R)**: Spherical coordinate robots follow a spherical coordinate system
4. **Articulated/Anthropomorphic (3R)**: All revolute joints, similar to a human arm. Most common configuration for industrial robots
5. **Selective Compliance Assembly Robot Arm (SCARA)**: Consist of 3 parallel revolute join for movement in horizontal plane, plus an additional prismatic joint for vertical movement
6. **Parallel Robots**: Differ in configuration from serial robots

### Robot Reference Frames
1. **World Reference Frames**: Universal coordinate frame, as defined by x-, y-, z-axes. Joints move simultaneously in a coordinated manner to create motions along three major axes
2. **Joint Reference Frames**: To specify movements of individual joints of robot. Each joint is accessed and moved individually, hence, only one joint moves at a time
3. **Tool Reference Frame**: This specifies movement of robot's hand relative to a frame attached to the hand, consequently, all motions are relative to this local n, o, a-frame. Unlike World Frame, Local Tool Frame moves with robot

### Robot Workspace:

| Coordinate System | Workspace   |
| ----------------- | ----------- |
| Cartesian         | Rectangular |
| Cylindrical       | Cylindrical |
| Sperhical         | Spherical   |

### Coordinate Transformation:
- 3D Translation: *Trans$(d_x, d_y, d_z)$* = $\begin{bmatrix}1 & 0 & 0 & d_x \\ 0 & 1 & 0 & d_y \\ 0 & 0 & 1 & d_z \\ 0 & 0 & 0 & 1\end{bmatrix}$
- 3D Rotation: *Rot$(z, \phi)$* = $\begin{bmatrix}C\phi & -S\phi & 0 \\ S\phi & C\phi & 0 \\ 0 & 0 & 1 \end{bmatrix}$
- 3D Rotation: *Rot$(x, \phi)$* = $\begin{bmatrix}1 & 0 & 0 \\ 0 & C\phi & -S\phi \\ 0 & S\phi & C\phi \end{bmatrix}$
- 3D Rotation: *Rot$(y, \phi)$* = $\begin{bmatrix}C\phi & 0 & S\phi \\ 0 & 1 & 0 \\ -S\phi & 0 & C\phi\end{bmatrix}$

### Forward and Inverse Kinematics of Robots
- Suppose we have a robot whose configuration is known. This means that all link lengths and joint angles are known. Calculating the position and orientation of hand of robot is called **Forward Kinematic Analysis**. In other words, if all robot joint variables are known, using forward kinematic equations, we can calculate where the robot is at any instant
- If we want to place the hand of robot at a desired location and orientation, we need to know how much each link length or joint angle must be such that at those values the hand will be at desired position and orientation. This is called **Inverse Kinematic Analysis**

### Forward and Inverse Kinematic Equations: Orientation
- Suppose the moving frame attached to the hand of robot has already moved to a desired position and is either parallel to reference frame or in an orientation other than what is desired
- Next we rotate the frame appropriately in order to achieve a desired orientation without changing its position. This can be accomplished by rotating about the current frame axes, rotations about the reference frame axes change the position
- We consider following three common configurations:
	1. Roll, Pitch and Yaw (RPY) angles
	2. Euler Angles

### Roll, Pitch and Yaw Angles
- RPY is a sequence of three orientations about the current a-, o-, n- axes, respectively, which orients the hand to a desired orientation
- **Important**: Assumption is that current frame is parallel to reference frame before application of RPY. Otherwise, the final orientation of the robot's hand is a combination of previous orientation, post-multiplied by the RPY
- Roll, Pitch and Yaw angles describe the orientation or rotation of a robot or any object in 3D space
- They are based on an imaginary fixed reference frame and the robot's body frame
- **Roll$(\phi)$**: Rotation around X-axis of robot's body frame
	1. Positive roll rotates the robot to the right, as if it were rolling on its wheels
	2. Negative roll rotates the robot to the left
- **Pitch$(\theta)$**: Rotation around Y-axis of the robot's body frame
	1. Positive pitch rotates the robot nose up, like tilting its head upwards
	2. Negative pitch rotates the robot nose down
- **Yaw $(\psi)$**: Rotation around Z-axis of robot's body frame
	1. Positive yaw rotates robot clockwise as if it were spinning on its spot
	2. Negative yaw rotates robot counter-clockwise

### Euler Angles
- They are very similar to RPY, except that the last rotation is also about current a-axis
- They are a way to represent the orientation or rotation of a rigid body in 3D space
- They describe the sequence of rotations applied around fixed axes to reach the final orientation from a reference position

### Denavit-Hartenberg Parameters
- Assign joint number $n$ to the first joint, $n + 1$ to the second joint and $n+2$ to the third joint and so on. Each link is also assigned a link number, link $n$ will be between joints $n$ and $n+1$, and link $n + 1$ is between joints $n+1$ and $n+2$
- All joints are represented by a $z$-axis. If the joint is revolute, the $z$-axis is in the direction of rotation as followed by the right-hand rule for rotations. If the joint is prismatic, the $z$-axis is along the direction of linear movement. In each case, the index number for the $z$-axis of joint $n$ is $n - 1$
- In general, joints may not necessarily be parallel or intersecting. As a result, the $z$-axes may be **skew lines**. There is always one line mutually perpendicular to any two skew lines, called the **common normal**, which is the shortest distance between them. We always assign the $x$-axis of local reference frame in the direction of the common normal between the previous and current axes
- If the two $z$-axes are parallel, there are an infinite number of common normals between them. We pick the **common normal that is collinear** with the common normal of the previous joint
- If the $z$-axes of two successive joints are **intersecting** there is no common normal between them. We assign the x-axis along a line perpendicular to the plane formed by two axes
- $\theta$ represents a rotation about the $z$-axis, *d* represents the distance on the $z$-axis between two successive common normals (*joint offset*), *a* represents the length of each common normal (*length of a link*) and $\alpha$ represents the angle between two successive $z$-axes (*twist angle*)
- For simple 2-axis, planar robot, assign the necessary coordinate systems based on the D-H representation, fill out the *parameters table* and derive the *forward kinematic equations* for the robot
