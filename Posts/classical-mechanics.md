
# Pendulum System

### System Description and Objective

A bob with mass $m$ is attached to a massless, rigid string with length $l$. This string is attached to a pivot joint fixed to the ceiling. Acceleration due to gravity is purely in the vertical direction, perpendicular to the ceiling. The bob with mass $m$ is represented as a point mass and at times will be referred to as a point mass. 

From the given information the objective is to write a differential equation $F = ma$ and find the solution of this differential equation. This solution is the  position of the point mass as a function of time.
@@sidenote
@@label
Pendulum System
@@
![](/assets/pendulum-system.svg)

@@


@@sidenote
@@label
Circular Path & Polar Coordinates
@@
![](/assets/polar-coords.svg)

@@figcaption
If an object has circular motion with a constaint radius, the object will always move in the direction of $\hat{\theta}$, which is tangential to the circumference of the circle.
@@
@@

### Coordinate System
The path of the point mass is a circular arc with an invariant radius in a two dimensional plane. If the state of the system is represented by polar coordinates $(r, \theta)$ there is no calculation needed for $r$, it will always be $l$ the length of the string. With polar coordinates only one dynamical variable $\theta$ is needed to describe the state of the system. Where $\theta$ is the angle between the string and a vertical line parallel to the direction of gravitational acceleration.

### Graphical Representations of a Point in a Plane
@@row-objects
@@row-object
![](/assets/cartesian-coordinates.svg)
@@figcaption
Point represented in rectangular coordinates
@@
@@
@@row-object
![](/assets/polar-coordinates.svg)
@@figcaption
Point represented in polar coordinates
@@
@@
@@


@@sidenote
@@figcaption
The free body diagram, showing the forces acting on the bob of the pendulum.
@@
![](/assets/pendulum-free-body.svg)
@@figcaption
The force $mg \sin{\theta}$ is parallel to $\hat{\theta}$, the direction of motion of the mass.
@@
@@


### Writing expressions for $F$ and $ma$
The velocity and acceleration of the point mass are purely in the $\hat{\theta}$ direction which is tangent to the circular arc. During a small time interval $\Delta t$ the point mass travels a distance $l \Delta \theta$.

$$
l \Delta \theta = l \big [ \theta(t + \Delta t) - \theta(t) \big]
$$

If this small distance is divided by $\Delta t$ and $\Delta t \to 0$ then (2) is the expression for the velocity of the point mass, it can be stated more compactly as $l \dot{\theta}$.

$$
l \bigg [\lim_{\Delta t \to 0} \frac{\theta(t + \Delta t) - \theta(t)}{\Delta t} \bigg]
$$

To get an expression for acceleleration, take the time derivative of the velocity $l \dot{\theta}$. 

$$
\frac{d}{dt}\dot{l\theta} = l\ddot{\theta}
$$

The expression for $ma$ is
 
 $$m l \ddot{\theta}.$$

Half of the problem for setting up $F = ma$ is done, now the expression for $F$ needs to be found.
In the free body diagram the total force in the $\hat{\theta}$ direction is $-mg\sin{\theta}$ which is the expression for $F$. The differential equation $F = ma$ can now be written.

Forces in the $\hat{r}$ direction sum to zero, so the magnitude of the tension in the string is $mg\cos{\theta}$. However, this information is not needed for the equation of motion. 

##
$$
m l \ddot{\theta} = -m g \sin{\theta}
$$


\begin{align}
\ddot{\theta} = - \frac{g}{l} \sin{\theta}
\end{align}

For small angles $\theta$, $\sin{\theta}$ is approximated by $\theta$. Using this approximation the differential equation is now

$$
\ddot{\theta} = - \frac{g}{l} \theta.
$$

@@sidenote
Series representation of $\sin{\theta}$
\nonumber{
$$
\sin{\theta} = \theta - \frac{\theta^3}{3!} + \frac{\theta^5}{5!} - \frac{\theta^7}{7!} + \cdots
$$
}
@@



If $\omega = \sqrt{g/l}$, then equation (7) can be written as
$$
\ddot{\theta} = - \omega^2 \theta.
$$

### Qualitative Analysis
The differential equation (6) expresses that the acceleration of the point mass is proportional to the sine of the angle between the string and the vertical line. In a sense the mass is getting a stronger "push" as $\sin{\theta}$ increases. When $\theta = \pi/4$, $\sin{\theta}$ is at its maximum. At this angle the force due to gravity is completely lined up or parallel with the $\hat{\theta}$ direction. When $\theta = 0$, there is no force applied to the mass in the $\hat{theta}$ direction, all the force that was applied to the mass prior to this point accumulated into kinetic energy.
### Solving the Differential Equation
\begin{align}
\frac{d^2}{ dt^2} \cos{\omega t} &= - \omega^2 \cos{\omega t} \\\\
\frac{d^2}{ dt^2} \sin{\omega t} &= - \omega^2 \sin{\omega t}
\end{align}
There is a common pattern that (8) and (9) share, that indicates the solutions of (8).
The general form of the solution to (8) is
$$
\theta(t) =  A \cos{\sqrt{\frac{g}{l}} t} + B \sin{\sqrt{\frac{g}{l}} t}
$$

where $A$ and $B$ are dimensionless constants that are determined from $\theta(0)$ and $\dot{\theta}(0)$. If $\theta(0) = A$ and $\dot{\theta}(0) = 0$ then the particular solution is

$$
\theta(t) =  A \cos{\sqrt{\frac{g}{l}} t}.
$$



### Checking Dimensions

Verification of dimensions is a good way to check for errors. The arguments of the sine and cosine functions are radians a dimensionless quantity, which means $\sqrt{\frac{g}{l}}$ needs to have dimensions of $T^{-1}$.

$$
\bigg[\sqrt{\frac{g}{l}} \bigg] = [L^{1} T^{-2} L^{-1}]^{1/2} = T^{-1}
$$

### Lagrangian Method
Motion of the simple pendulum can also be derived using the Lagrangian method.
Once the Langrangian formula (13) is found, the Euler-Lagrange equation (14) can be written and solved. The solution of (14) will be equivalent to (10).

$$
\mathcal{L} = T - V
$$

$$
\frac{d}{dt}\frac{\partial{\mathcal{L}}}{\partial \dot{q}} = \frac{\partial{\mathcal{L}}}{\partial q}
$$

$\mathcal{L}$ is the kinetic energy $T$ minus the potential energy $V$.

\begin{align}
T &= \frac{1}{2}ml^2\dot{\theta}^2 \\
V &= -mgl\cos{\theta} \\ 
\mathcal{L} &= \frac{1}{2}ml^2\dot{\theta}^2 + mgl\cos{\theta} \\ 
\end{align}
This specific Lagrangian plugged into (14) yields the following differential equation, which is the same as equation (5).
$$
ml^2 \ddot{\theta} =  -mgl\sin{\theta}
$$





