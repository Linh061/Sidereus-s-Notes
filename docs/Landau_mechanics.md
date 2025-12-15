# EQUATIONS OF MOTION

### Generalized Coordinates
As one of the fundamental concepts of mechanics, the particle has been familiar to us since our middle school physics lectures. Nevertheless, it is worth pointing out that the particle in space is defined by its radius vector $\boxed{r}$, whose components are its Cartesian coordinates $(x, y, z)$.

However, in order to define the position of a system of $N$ particles in space, it is necessary to specify $N$ radius vectors, i.e. $3N$ coordinates. From this, we introduce the concept of degrees of freedom⁺, which refers to the set of independent quantities that must be specified to define the unique position of any system. It is not difficult to find that the degrees of freedom of the coordinate system mentioned above are exactly $3N$. It may render us some novel choices for defining a coordinate system in a more convenient way. Such any $s$ quantities $q_1, q_2, q_3, \dots, q_s$ which completely define the coordinates of a system with $s$ degrees of freedom are called generalized coordinates of the system, and the derivatives $\dot{q}_i$ are called its generalized velocities.

Nonetheless, we can neither determine the mechanical state of a system nor predict its position at subsequent instants solely from the specified values of the generalized coordinates. Because for given values of the coordinates, the system can have any velocities which affect its position after an infinitesimal time, i.e. $dt$.

If all the coordinates and velocities are simultaneously specified, it is known from experience that the state of the system is completely determined and that its subsequent motion can be calculated in principle. Mathematically, this means that, if all the coordinates $q$ and velocities $\dot{q}$ are given at some instant, the accelerations $\ddot{q}$ at that instant are uniquely defined. The relations between the coordinates, velocities and accelerations are called the equations of motion. They are second-order differential equations for the function $q(t)$. In principle, we can determine these functions by integrating these equations and thus determine the path of the system.

### The Principle of Least Action
The most general formulation of the law governing the motion of mechanical system is the principle of least action (or Hamilton's principle), according to which every mechanical system is characterized by a definite function $L = (q, \dot{q}, t)$.

And the motion of the system must satisfy a certain condition: let the system occupy, at the instants $t_1$ and $t_2$, positions defined by two sets of values of the coordinates, $q^{(1)}$ and $q^{(2)}$. Then the condition is that the system moves between these positions in such way that the integral $S = \int_{t_1}^{t_2} L(q, \dot{q}, t)dt$ takes the least possible value. The function $L$ is called the Lagrangian of the system concerned, and the integral is called the action.

Now we begin to derive the differential equations that solve the problem of minimizing the integral. For the sake of simplicity, we first suppose that the system has only one degree of freedom, so that one function $q(t)$ needs to be determined.

Let $q = q(t)$ be the function for which $S$ is minimum. This means that $\delta S$ is increased when $q(t)$ is replaced by any function of the form $q(t) + \delta q(t)$, where $\delta q(t)$ is called a variation of the function $q(t)$ and it is also a function which is infinitesimal everywhere in the interval of time from $t_1$ to $t_2$. Since, for $t = t_1$ and for $t = t_2$, all the functions must take the values $q^{(1)}$ and $q^{(2)}$ respectively, it follows that $\delta q(t_1) = \delta q(t_2) = 0$.

The change in $S$ when $q$ is replaced by $q + \delta q$ is:

$$
\int_{t_1}^{t_2} L(q + \delta q, \dot{q} + \delta \dot{q}, t)\,dt - \int_{t_1}^{t_2} L(q, \dot{q}, t)\,dt
$$

Now we begin to expand the first integrand in powers. Since the variations are extremely small, their higher order infinitesimals can be neglected. Based on this consideration, we only retain its first-order infinitesimal terms. So we obtain:

$$
L(q, \dot{q}, t) + \frac{\partial L}{\partial q}\, \delta q + \frac{\partial L}{\partial \dot{q}}\, \delta \dot{q}
$$

After substitution and simplification, the principle of least action can be written in the form:

$$
\delta S = \int_{t_1}^{t_2} \left(
\frac{\partial L}{\partial q}\, \delta q
+ \frac{\partial L}{\partial \dot{q}}\, \delta \dot{q}
\right) dt
$$

Since $\delta \dot{q} = \frac{d}{dt}\delta q$, namely, $\delta \dot{q}\, dt = d\delta q$, we can integrate the second term by parts.

Because

$$
u = \frac{\partial L}{\partial \dot{q}}, \quad du = \frac{d}{dt} \left( \frac{\partial L}{\partial \dot{q}} \right) dt
$$

$$
dv = \delta \dot{q}\, dt = d\delta q, \quad v = \delta q
$$

After substitution, we obtain:

$$
\left. \frac{\partial L}{\partial \dot{q}} \, \delta q \right|_{t_1}^{t_2} - \int_{t_1}^{t_2} \delta q \, \frac{d}{dt} \left( \frac{\partial L}{\partial \dot{q}} \right) dt
$$


After substitution, we obtain:

$$
\left. \frac{\partial L}{\partial \dot{q}} \delta q \right|_{t_1}^{t_2} - \int_{t_1}^{t_2} \delta q \frac{d}{dt} ( \frac{\partial L}{\partial \dot{q}} \right) dt
$$

Since $\delta q(t_1) = \delta q(t_2) = 0$, the first term vanishes. So for all values of $\delta q$ we obtain:

$$
\delta S = \int_{t_1}^{t_2} \left( 
\frac{\partial L}{\partial q} - \frac{d}{dt} \frac{\partial L}{\partial \dot{q}} 
\right) dt = 0
$$

A more concise form after rearranging the terms is:

$$
\frac{d}{dt} \left( \frac{\partial L}{\partial \dot{q}} \right) - 
\frac{\partial L}{\partial q} = 0
$$
