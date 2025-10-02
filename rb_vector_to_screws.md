# Rigid Body Dynamics with Screw Theory

In vector dynamics the equations of motion have their simplest form when the center of mass is used as the reference point where linear velocity, acceleration, and angular momentum and torque is summed about. 

But in addition to the dynamics equations, the kinematics of a system of rigid bodies need to be considered which related the velocity and acceleration vectors of one body to another body, both in translational and rotational fashion. The simplest form of kinematics is when then joint positions are used as the reference point. 

When when describing a _system_ of rigid bodies that are connected with joint, it apparent that transformation equations need to be included to transfer the reference point from the joint to the center of mass and back in order to be able to combine all of the equations into a system.

When dealing with vector equations not only transormations need to be considered, but also both linear and angular vectors need to be included. So a lot of complexity arises from the cross terms that exist between linear and angular terms. 

The governing equations with *screw theory* have the advantage of being coordinate free and of combining both linear and angular components into one term. 

## Vcetor Form Definitions

### Kinematics

The simplest example is a system with a serial chain of rigid bodies, each connected to the previous body. Thus the motion of body _i_, depends on the motion of body _i_-1. And the first body is connected to the ground.

Each joint can be either a pin joint (revolute) or a slider joint (prismatic). But it turns out there is generalization in a screw joint which is defined by a rotation about an axis, and a simultaneous translation along the axis. If the screw pitch is zero it describes a revolute joint, and if the screw pitch approaches _infinite_ at the limit it describes a prismatic joint.

 - Vector Velocity Kinematics
    
    $$ \boldsymbol{\omega}_{i}=\boldsymbol{\omega}_{i-1}+\hat{\boldsymbol{z}}_{i}\dot{q}_{i} \tag{vec-vel-rot} $$
    $$ \boldsymbol{v}_{i}+\boldsymbol{r}_{i}\times\boldsymbol{\omega}_{i}=\boldsymbol{v}_{i-1}+\boldsymbol{r}_{i-1}\times\boldsymbol{\omega}_{i-1}+\boldsymbol{r}_{\boldsymbol{i}}\times\hat{\boldsymbol{z}}_{i}\dot{q}_{i}+h_{i}\hat{\boldsymbol{z}}_{i}\dot{q}_{i} \tag{vec-vel-lin}$$

 - Vector Acceleration Kinematics
  
    $$ \boldsymbol{\alpha}_{i}=\boldsymbol{\alpha}_{i-1}+\hat{\boldsymbol{z}}_{i}\ddot{q}_{i}+\boldsymbol{\omega}_{i}\times\hat{\boldsymbol{z}}_{i}\dot{q}_{i} \tag{vec-acc-rot}$$

    $$ \begin{aligned}\boldsymbol{\alpha}_{i}+\boldsymbol{r}_{i}\times\boldsymbol{\alpha}_{i}+\boldsymbol{v}_{i}\times\boldsymbol{\omega}_{i} & =\boldsymbol{a}_{i-1}+\boldsymbol{r}_{i-1}\times\boldsymbol{\alpha}_{i-1}+\boldsymbol{v}_{i-1}\times\boldsymbol{\omega}_{i-1}+\boldsymbol{r}_{i}\times\hat{\boldsymbol{z}}_{i}\ddot{q}_{i}+h_{i}\hat{\boldsymbol{z}}_{i}\ddot{q}_{i}\\
     & +\left(\boldsymbol{v}_{i}+\boldsymbol{r}_{i}\times\boldsymbol{\omega}_{i}\right)\times\hat{\boldsymbol{z}}_{i}\dot{q}_{i}+\boldsymbol{\omega}_{i}\times\left(\boldsymbol{r}_{i}\times\hat{\boldsymbol{z}}_{i}\dot{q}_{i}+h_{i}\hat{\boldsymbol{z}}_{i}\dot{q}_{i}\right)
    \end{aligned} \tag{vec-acc-lin}$$

    $$\begin{array}{r|l}

    \end{array}$$

### Dynamics

As mentioned before the governing equations for momentum and forces (dynamics) are best expressed around each center of mass. 

 - Vector Momentum equations

    $$ \boldsymbol{p}_{i}=m_{i}\left(\boldsymbol{v}_{i}+\boldsymbol{\omega}_{i}\times\boldsymbol{c}_{i}\right) \tag{vec-mom-lin}$$
    $$ \boldsymbol{L}_{i}=\mathcal{I}_{i}\boldsymbol{\omega}_{i}+\boldsymbol{c}_{i}\times\boldsymbol{p}_{i} $$

 - Vector Force equations
  
    $$ \boldsymbol{F}_i^\text{net} = m_i \left(\boldsymbol{a}_{i}+\boldsymbol{\alpha}_{i}\times\boldsymbol{c}_{i}+\boldsymbol{\omega}_{i}\times\left(\boldsymbol{\omega}_{i}\times\boldsymbol{c}_{i}\right)\right) \tag{vec-frc-lin}$$
    $$ \boldsymbol{\tau}_i^\text{net} = \mathcal{I}_{i} \boldsymbol{\alpha}_i + \boldsymbol{\omega}_i\times \mathcal{I}_{i} \boldsymbol{\omega}_i + \boldsymbol{c}_i \times \boldsymbol{F}_i^\text{net} \tag{vec-frc-ang}$$

The subscript _i_ in the equations below denotes quantities on body _i_, and the subscript _i_-1 denots quantities on the previous body (parent body) in a system of bodies.

$$\begin{array}{r|l}
\boldsymbol{c}_i & \text{vector connecting the center of mass to the joint}
m_i & \text{mass of body} \\
{\rm I}^C_i & \text{mass moment of inertia about center of mass} \\
\boldsymbol{v}_i & \text{linear velocity of the joint} \\
\boldsymbol{\omega}_i & \text{angular velocity of body} \\
\boldsymbol{a}_i & \text{linear acceleration of the joint} \\
\boldsymbol{\alpha}_i & \text{angular acceleration of body} \\
\boldsymbol{p}_i & \text{linear momentum vector of body} \\
\boldsymbol{L}_i & \text{angular momentum about the joint} \\
\boldsymbol{F}_i^\text{net} & \text{net force on body} \\
\boldsymbol{\tau}_i^\text{net} & \text{net torque on body about the joint} \\
\end{array}$$

### Joint Condition


