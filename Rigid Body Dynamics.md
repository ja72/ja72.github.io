
# Angular Momentum and Torque on a Rigid Body

Angular momentum of a rigid body varies as the point of summation varies. Also, equipollent torque varies as the point of summation varies also. This posts examines the relationship between change in angular momentum and equipollent torque in the context of Newton's 2nd law.  It is <strike>expected</strike> required that at the center of mass equipollent torque and change in angular momentum at simply equal to each other. But what about when measured at an arbitrary point **A** not at the center of mass **C**.

<sub>Note that all quantities are expressed on the same basis vectors, and only reference point being **C** or **A** or **O** the origin describing the properties of whichever particles happens to be passing under this reference point.</sub>

### Particle Forces & Torques

The combined loading on the rigid body can be reduced down to an equipollent system of forces $\boldsymbol{F}$ and torques $\boldsymbol{\tau}_A$ at the reference point **A**. In dynamics it is important to consider the combined torque about the center of mass which is evaluated with the transformation law(s)

$$ \begin{aligned} 
\boldsymbol{\tau}_C &= \boldsymbol{\tau}_A + (\boldsymbol{r}_A - \boldsymbol{r}_C) \times \boldsymbol{F} \\ \boldsymbol{\tau}_A& = \boldsymbol{\tau}_C + (\boldsymbol{r}_C - \boldsymbol{r}_A) \times \boldsymbol{F}
\end{aligned} \tag{1} $$

| _quantity_ | _description_ |
|---:|:---|
| $\boldsymbol{F}$ | combined of forces applied on body. | 
| $\boldsymbol{\tau}_A$ | combined torque applied on body about point **A**.
| $\boldsymbol{\tau}_C$ | combined torque applied on body about center of mass **C**.
| $\boldsymbol{r}_A$ | location of point **A** from the origin.
| $\boldsymbol{r}_C$ | location of point **C** from the origin.

### Center of mass

It is important to define the center of mass not only as the weighted sum of the particle locations

$$ \boldsymbol{r}_C = \frac{1}{m} \sum_i m_i \boldsymbol{r}_i \tag{3} $$

but also as the relative location of each particle being zero

$$ \sum_i m_i ( \boldsymbol{r}_i - \boldsymbol{r}_C) =  \boldsymbol{0} \tag{4} $$

These two expressions are equivalent to each other. For simplicity you can define the relative position of each particle as $\boldsymbol{d}_{Ci}$, but at this stage I want to keep things as explicit as possible.

| quantity | description | definition |
| ---: | :--- | :--- |
| $m$ | combined masss | $\sum_i m_i$
| $\boldsymbol{d}_{Ci}$ | relative position of particle | $\boldsymbol{d}_{Ci} = \boldsymbol{r}_i - \boldsymbol{r}_C$

### Momenta Definitions

Momenta are _defined_ by summing up the following contributions of all the particles that move together on a rigid body. This summation happens an at arbitrary location **A** in space _at every instance_ in time.

$$ \begin{aligned}
\boldsymbol{p} & = \sum_i m_i \boldsymbol{v}_i \\
\boldsymbol{L}_A & = \sum_i (\boldsymbol{r}_i - \boldsymbol{r}_A) \times m_i \boldsymbol{v}_i
\end{aligned} \tag{2} $$

where:
| _quantity_ | _description_ |
|---:|---|
| $\boldsymbol{p}$ | <strike>linear</strike> translational momentum vector. |
| $\boldsymbol{L}_A$ | <strike>angular</strike> rotational momentum vector of the body measured at **A**. |
| $m_i$ | infinitesimal mass of each particle such that the total mass is $m = \sum_i m_i$. |
| $\boldsymbol{r}_i$ | position vector of the particle from the origin. |
| $\boldsymbol{v}_i$ | velocity vector of the particle. |
| $\boldsymbol{r}_A$ | position vector of arbitrary point **A** from the origin. |

Note that the point **A** might be fixed in space over time, or moving with constant velocity or riding on the body. At any time frame it might have non-zero velocity $\boldsymbol{v}_A$ with respect to the origin. 

### Kinematics

The motion of each particle can be decomposed into the motion of the center of mass and a rotation about the center of mass (Chasle's Theorem).

$$ \boldsymbol{v}_i = \boldsymbol{v}_C + \boldsymbol{\omega} \times (\boldsymbol{r}_i - \boldsymbol{r}_C) \tag{3} $$

Additionally the combined motion of the center of mass point **C** is expressed on the reference point **A** using the following transformation law(s)

$$ \begin{aligned} \boldsymbol{v}_C &= \boldsymbol{v}_A + (\boldsymbol{r}_A - \boldsymbol{r}_C) \times \boldsymbol{\omega} \\  \boldsymbol{v}_A &= \boldsymbol{v}_C + (\boldsymbol{r}_C - \boldsymbol{r}_A) \times \boldsymbol{\omega}
 \end{aligned} \tag{4} $$

Any resemblence of the above to (1) is not coincidence. 

### Translational Momentum

Translational momentum is the easiest to evaluate from (2) and (3). Center of mass expression (4) is used for simplification below

$$ \begin{aligned}
\boldsymbol{p} & = \sum_i m_i ( \boldsymbol{v}_C + \boldsymbol{\omega} \times ( \boldsymbol{r}_i - \boldsymbol{r}_C)) \\
& = (\sum_i m_i) \boldsymbol{v}_C + \boldsymbol{\omega} \times  \cancel{ \sum_i m_i (\boldsymbol{r}_i - \boldsymbol{r}_C) } 
\end{aligned}   $$

$$ \boldsymbol{p} = m\,\boldsymbol{v}_C \tag{5} $$

The is a well known result, undesputed as long as $\boldsymbol{p}$ and $\boldsymbol{v}_C$ are measued form _the same coordinate frame_. Again, $\boldsymbol{v}_C$ is the velocity vector of the center of mass, as in

$$ \boldsymbol{v}_C = \tfrac{\mathrm{d}} {\mathrm{d}t} \boldsymbol{r}_C $$

### Rotational Momentum about Center of Mass

Rotational momentum is also  evaluated from (2) and (3) but we start with summing about the center of mass first

$$ \begin{aligned} \boldsymbol{L}_C & = \sum_i (\boldsymbol{r}_i - \boldsymbol{r}_C) \times m_i v_i \\
& = \sum_i m_i ( \boldsymbol{r}_i - \boldsymbol{r}_C) \times ( \boldsymbol{v}_C + \boldsymbol{\omega} \times ( \boldsymbol{r}_i - \boldsymbol{r}_C)) \\
 & = \cancel{ \sum_i m_i (\boldsymbol{r}_i - \boldsymbol{r}_C) } \times \boldsymbol{v}_C + \sum_i m_i \boldsymbol{d}_{Ci} \times ( \boldsymbol{\omega} \times \boldsymbol{d}_{Ci} ) \\
& = \sum_i \left[ - m_i \boldsymbol{d}_{Ci} \times (  \boldsymbol{d}_{Ci} \times \boldsymbol{\omega}) \right]  \end{aligned} $$

$$ \boldsymbol{L}_C = \mathbf{I}_C \boldsymbol{\omega} \tag{6} $$

where $\mathbf{I}_C$ is the 3×3 mass moment of inertia tensor (inertia dyatic) derived from factoring $\boldsymbol{\omega}$ from the rotational inertia expression above.

Practically this is done by evaluating the following sum. For simplicity consider each relative position vector having components $\boldsymbol{d}_{Ci} = \begin{pmatrix} x_i \\ y_i \\ z_i \end{pmatrix}$ and evaluate

$$ \mathbf{I}_C = \sum_i m_i \begin{bmatrix} y_i^2 + z_i^2 & -x_i y_i & -x_i z_i \\ -x_i y_i & x_i^2+z_i^2 & -y_i z_i \\ -x_i z_i & -y_i z_i & x_i^2+y_i^2
\end{bmatrix} \tag{7} $$

Another common alterative to the above is to declare the 3×3 cross product matrix as $$ [\boldsymbol{d}_{Ci} \times] \equiv \begin{bmatrix} 0 & -z_i & y_i \\ z_i & 0 & -x_i \\ -y_i & x_i & 0 \end{bmatrix} $$ and evaluating

$$ \mathbf{I}_C = \sum_i \left( -m_i [\boldsymbol{d}_{Ci} \times][\boldsymbol{d}_{Ci} \times] \right) \tag{8} $$

### Rotational Momentum about Arbitrary Point

Rotational momentum is also  evaluated from (2) and (3) but we sum about the arbitrary point **A**. 

$$ \begin{aligned} \boldsymbol{L}_A & = \sum_i (\boldsymbol{r}_i - \boldsymbol{r}_A) \times m_i v_i \\
& =  \sum_i (\boldsymbol{r}_i - \boldsymbol{r}_C) \times m_i v_i + \sum_i (\boldsymbol{r}_C - \boldsymbol{r}_A) \times m_i v_i \\
& = \boldsymbol{L}_C + (\boldsymbol{r}_C-\boldsymbol{r}_A) \times \sum_i m_i v_i
\end{aligned} $$

Which leads the the following transformation law(s)

$$ \begin{aligned} \boldsymbol{L}_A & = \boldsymbol{L}_C + (\boldsymbol{r}_C-\boldsymbol{r}_A) \times \boldsymbol{p} \\ \boldsymbol{L}_C & = \boldsymbol{L}_A + (\boldsymbol{r}_A-\boldsymbol{r}_C) \times \boldsymbol{p}
\end{aligned} \tag{9} $$

Again, any resemblance to (1) and (4) is not a coincidence. This is because these are Plücker coordinates of different lines in space. The force line is called the _line of action_. The motion line is called the _rotation axis_. And the momentum line is called _axis of percussion_.

In spatial form the above is 

$$\begin{bmatrix}\boldsymbol{p}\\
\boldsymbol{L}_{A}
\end{bmatrix}=\begin{bmatrix}m & -m\boldsymbol{c}\times\\
m\boldsymbol{c}\times & \boldsymbol{I}_{A}
\end{bmatrix}\begin{bmatrix}\boldsymbol{v}_{A}\\
\boldsymbol{\omega}
\end{bmatrix}$$

where $\boldsymbol{c} = \boldsymbol{r}_C - \boldsymbol{r}_A$ and $\boldsymbol{I}_A = 

## Dynamics

We establish Newton's second law about the center of mass **C** relating forces/torques to rate of change of momenta

$$ \begin{aligned}
\boldsymbol{F} & = \tfrac{\mathrm{d}}{\mathrm{d}t} \boldsymbol{p} \\
\boldsymbol{\tau}_C & = \tfrac{\mathrm{d}}{\mathrm{d}t} \boldsymbol{L}_C
\end{aligned} \tag{10} $$

Using the definitions above from particle summation the expression of equations of motion are straigtforward when using rhe center of mass as a reference point.

$$ \begin{aligned}
\boldsymbol{F} & = m \boldsymbol{a}_C \\
 \boldsymbol{\tau}_C & = \mathbf{I}_C \boldsymbol{\alpha} + \boldsymbol{\omega} \times \boldsymbol{L}_C
 \end{aligned} \tag{11} $$
where 
| quantity | description | definition |
| ---: | :--- | :--- |
| $\boldsymbol{a}_C$ | translational acceleration of the center of mass | $\tfrac{\mathrm{d}}{\mathrm{d}t} \boldsymbol{v}_C$ 
| $\boldsymbol{\alpha}$ | rotational acceleration of the body | $\tfrac{\mathrm{d}}{\mathrm{d}t} \boldsymbol{\omega}$ |

### Arbitrary Point

The question is can the equations of motion above can be derived from Newton's 2nd law _at an arbitrary location_?

**Is the following valid?**

$$ \boldsymbol{\tau}_A = \tfrac{\mathrm{d}}{{\mathrm{d}}t} \boldsymbol{L}_A \tag{12} $$

We can use the transformation laws (1) and (9) described above to see if (12) can lead to (11) which we know is correct.

$$ \begin{aligned} 
\boldsymbol{\tau}_C + (\boldsymbol{r}_C - \boldsymbol{r}_A) \times \boldsymbol{F}  & = \tfrac{\mathrm{d}}{\mathrm{d}t} ( \boldsymbol{L}_C + (\boldsymbol{r}_C-\boldsymbol{r}_A) \times \boldsymbol{p} ) \\
 & = \tfrac{\mathrm{d}}{\mathrm{d}t}  \boldsymbol{L}_C +  \tfrac{\mathrm{d}}{{\mathrm{d}}t} \left( (\boldsymbol{r}_C-\boldsymbol{r}_A)  \times \boldsymbol{p} \right) \\
\cancel{\boldsymbol{\tau}_C} + (\boldsymbol{r}_C - \boldsymbol{r}_A) \times \boldsymbol{F} & = \cancel{\boldsymbol{\tau}_C} + \tfrac{\mathrm{d}}{{\mathrm{d}}t} (\boldsymbol{r}_C-\boldsymbol{r}_A)  \times \boldsymbol{p} +  (\boldsymbol{r}_C-\boldsymbol{r}_A)  \times \tfrac{\mathrm{d}}{{\mathrm{d}}t} \boldsymbol{p} \\
\cancel{(\boldsymbol{r}_C - \boldsymbol{r}_A) \times \boldsymbol{F}}  &=  ( \boldsymbol{v}_C - \boldsymbol{v}_A)\times \boldsymbol{p} + \cancel{ (\boldsymbol{r}_C - \boldsymbol{r}_A) \times \boldsymbol{F}} \\ \boldsymbol{0} & = 
\boldsymbol{p} \times ( \boldsymbol{v}_A - \boldsymbol{v}_C) \\
\boldsymbol{0} & = m\,\boldsymbol{v}_C \times \boldsymbol{v}_A
\end{aligned} $$

The _necessary_ condition(s) for (12) to be correct are as follows

 - Reference point **A** is fixed in space.
 - Reference point **A** is co-moving with the center of mass.
 - Center of mass **C** is fixed in space.

The general rule connecting equipollent torque to change in rotational momentum is thus

$$ \boldsymbol{\tau}_A = \tfrac{\mathrm{d}}{\mathrm{d}t} \boldsymbol{L}_A + \boldsymbol{v}_A \times \boldsymbol{p} \tag{13} $$

where 

| quantity | description |
| ---: | :--- |
| $\boldsymbol{\tau}_A$ | equipollent torque acting on the body (instanteneously) summed on the reference point **A**.
| $\boldsymbol{L}_A$ | rotational momentum of rigid body summed on the reference point **A**. |
| $\boldsymbol{p}$ | translational momentum of the rigid body. |
| $\boldsymbol{v}_A$ | instanteneous velocity of reference point **A**.

In spatial form the above is

$$\begin{bmatrix}
\boldsymbol{F} \\ \boldsymbol{\tau}_A \end{bmatrix} =  \frac{\mathrm{d}}{\mathrm{d}t}
\begin{bmatrix} \boldsymbol{p} \\ \boldsymbol{L}_A \end{bmatrix} + \begin{bmatrix} 0  \\ \boldsymbol{v}_A \times \boldsymbol{p} \end{bmatrix} $$

### Example

Consider a rod sliding vertically along a rail with speed $v_A$ and pivoting with rotational speed $\omega$ about a point **A** away from the center of mass **C**.  A force of magnitude $F_B$ is applied horizontally at another point **B**.
![sliding rod](https://i.imgur.com/JwNY2Oa.png)

The variable $c$ is the distance between the pivot and the center of mass, and $\ell$ the distance between the pivot and the force application point.

**Can (12) produce the correct equation of motion?**

First we develop the equations of motion about the center of mass

 1. **Kinematics** the center of mass **C** moves under two degrees of freedom, the sliding velocity $v_A$ and the rotation $\omega$
	 - $\boldsymbol{v}_C = v_A\, \boldsymbol{\hat{j}} + \omega \boldsymbol{\hat{k}} \times c \boldsymbol{\hat{j}} = \begin{pmatrix} -c\, \omega \\ v_A \\ 0\end{pmatrix}$
	 - $\boldsymbol{a}_C =\dot{v}_A \boldsymbol{\hat{j}} + \dot{\omega}\boldsymbol{\hat{k}}\times c \boldsymbol{\hat{j}} + \omega \boldsymbol{\hat{k}} \times \boldsymbol{v}_C = \begin{pmatrix} -c\,\dot{\omega} - \omega\, v_A  \\ \dot{v}_A - c\, \omega^2 \\ 0  \end{pmatrix}$
 2. **Momenta** directly calculated from the motion of the center of mass
     - $\boldsymbol{p} = m \boldsymbol{v}_C = \begin{pmatrix} -m \,c\,\omega \\ m\,v_A \\ 0 \end{pmatrix}$
     - $\boldsymbol{L}_C = \mathbf{I}_C \boldsymbol{\omega} = \begin{pmatrix} 0 \\ 0 \\ I_C \omega \end{pmatrix}$
 4. **Equipollent forces and moments** at the center of mass **C** are a combination of the appled force $F_B$ and the pin reaction force $A_x$.
    - $\boldsymbol{F} = \begin{pmatrix} F_B+A_x \\ 0 \\ 0 \end{pmatrix}$
    - $\boldsymbol{\tau}_C = \begin{pmatrix} 0 \\ 0 \\ c A_x -(\ell-c) F_B \end{pmatrix}$
3. **Equations of motion** 
    - $\begin{pmatrix} F_B+A_x \\ 0 \\ 0 \end{pmatrix} = m \begin{pmatrix} -c\,\dot{\omega} - \omega\, v_A  \\ \dot{v}_A - c\, \omega^2 \\ 0  \end{pmatrix}$ 
    - $\begin{pmatrix} 0 \\ 0 \\ c A_x -(\ell-c) F_B \end{pmatrix} = I_C \begin{pmatrix} 0 \\ 0 \\ \dot{\omega} \end{pmatrix}$
  4. **Solution**
      - $\dot{\omega} = - \dfrac{\ell F_B + m\,c\,\omega\,v_A}{I_C + m c^2}$
      - $\dot{v}_A = c\,\omega^2$
      - $A_x = -\left( 1-\dfrac{m\,c\,\ell}{I_C + m c^2} \right) F_B - \dfrac{\omega\,v_A}{ \tfrac{1}{m} + \tfrac{c^2}{I_C}}$
      
Now we apply equation (12) directly after the rotational momentum about **A** is calculated from (9). 
    - $\boldsymbol{L}_A = \begin{pmatrix} 0 \\ 0 \\ (I_C + m c^2) \omega \end{pmatrix}$
    - $\boldsymbol{\tau}_A = \begin{pmatrix} 0 \\ 0 \\ -\ell F_B \end{pmatrix}$
    - $\tfrac{\mathrm{d}}{\mathrm{d}t}\boldsymbol{L}_A = \begin{pmatrix} 0 \\ 0 \\ (I_C + m c^2) \dot{\omega} \end{pmatrix}$
    - $\boldsymbol{v}_A \times \boldsymbol{p} = \begin{pmatrix} 0 \\ 0 \\ m\,c\,\omega\,v_A \end{pmatrix}$

All together equation (12) is

$$ -\ell F_B = (I_C + m c^2) \dot{\omega} + m c \omega v_A $$

which is solved for $\dot{\omega}$ to produce **the exact same same solution as above**

$$\dot{\omega} = - \dfrac{\ell F_B + m\,c\,\omega\,v_A}{I_C + m c^2}\;\;\checkmark$$


<!--stackedit_data:
eyJwcm9wZXJ0aWVzIjoiYXV0aG9yOiBKb2huIEFsZXhpb3Vcbn
N0YXR1czogZHJhZnRcbmRhdGU6ICcyMDIxLTAzLTAxJ1xudGl0
bGU6IEFuZ3VsYXIgTW9tZW50dW0gYW5kIFRvcnF1ZSBvbiBhIF
JpZ2lkIEJvZHlcbnRhZ3M6ICdwaHlzaWNzLGR5bmFtaWNzLHJp
Z2lkLWJvZHkscm90YXRpb25zJ1xuIiwiaGlzdG9yeSI6WzE4NT
YxNzY1OTUsLTEyMDE4OTc4NzUsLTE4MDc3MzgwODNdfQ==
-->