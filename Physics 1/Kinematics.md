**Position** is always denoted as $x(t)$, a function of time. The position of the object in reference to the origin can be referred to as the position vector, $\vec{r}(t)$, and when working on the x-axis in a 1D example, we have that $\vec{r}(t) = x(t)\hat{i}$

**Time interval** can be characterized, on a closed interval $[t_1,t_2]$ as $\Delta t = t_2 - t_1$, the SI units being Seconds $[s]$

**Displacement** of a body during a time interval $[t_1, t_2]$ is the change in position of the body, which is defined as $\Delta \vec{r} = \vec{r}(t_2)-\vec{r}(t_1) = (x(t_2)-x(t_1))\hat{i} = \Delta x(t)\hat{i}$

**Average Velocity** known as $v_{x,ave}$ for a time interval $\Delta t$ is defined as the displacement of the body $\Delta x$ over the time interval $\Delta t$, $v_{x, ave} = \frac{\Delta{x}}{\Delta{t}}$. This is only for 1 dimensional velocity. For two dimensional velocity, we can denote the average velocity as $v_{ave} = \frac{\Delta{x}}{\Delta{t}}\hat{i} = v_{ave}\hat{i}$ . The [[SI Units]] for velocity is meters per second, $m\cdot s^{-1}$
The average velocity is not necessarily equal to the distance traveled during a time interval, think about an object moving positively in a direction, and then returning to its initial condition. The average velocity is 0, but the distance traveled is not. 

**Instantaneous Velocity** is different from Average Velocity because we can define a way of finding the velocity for specific time on the curve rather than averaging the entire thing. For a time interval $[t, \Delta t]$, we can figure that the average velocity will be $v_ave = \frac{\Delta x}{\Delta t} = \frac{x(t + \Delta t)-x(t)}{\Delta t}$. If we choose to take the limit as $t=0$, or the lower bound of our interval, then we can figure out what the tangent line, i.e. the instantaneous velocity will be. As we can see, this limit mirrors the first derivative, which is defined as follows: $v(t) = \lim_{\Delta t \rightarrow 0}v_{ave} = \lim_{\Delta t \rightarrow 0} \frac{\Delta x}{\Delta t} = \lim_{\Delta t \rightarrow 0} \frac{x(t + \Delta t)-x(t)}{\Delta t} = \frac{dx}{dt}$. The vector representing this instantaneous velocity then becomes $\vec{v}(t) = v(t)\hat{i}$

An example of applying these formulas is by looking at a position function, and determining the the instantaneous velocity from it

Example 4.1: We have position function $x(t) = x_0 + \frac{1}{2}bt^2$, where $x_0$ is an initial condition. If we take the first derivative of this, we can find the instantaneous velocity of the function to be $v(t) = bt$. 

**Acceleration** is defined as the rate of change of velocity with respect to time. Once again this can be defined in two ways, instantaneous and average acceleration. 

**Average Acceleration** utilizes the velocity function found before, measuring the change in velocity of a specific time interval. The change in velocity can be found as:
$$
\Delta \vec{v} = \vec{v}(t+\Delta t) - \vec{v}
$$
For just the x component of velocity, this becomes:
$$
\Delta v = \Delta v(t+\Delta t) - v(t)
$$
Finally, defining the x-component of the average acceleration is:
$$
\vec{a}_{ave} = a_{ave} \hat{i} = \frac{\Delta v}{\Delta t} = \frac{(v(t+\Delta t) - v(t))}{\Delta t}\hat{i}
$$

With [[SI units]], meters per second squared, $[m\cdot s^{-2}]$

**Instantaneous Acceleration**

The x component of the acceleration is just the slope of the velocity at a particular time $t$. This would make the entire equation:

$$
a(t) \lim_{ \Delta t \to 0 } = \frac{\Delta v}{\Delta t} = \lim_{ \Delta t \to 0 } \frac{(v(\Delta t - t) - v(t))}{\Delta t}\  = \frac{dv}{dt} 
$$
The vector for acceleration then becomes:
$$
\vec{a}(t) = a(t)\hat{i}
$$

The velocity is the derivative of the time function, and since acceleration is the derivative of velocity, that would indicate instantaneous acceleration is the second derivative of the time function. This is as follows:

$$
a = \frac{dv}{dt} = \frac{d^2x}{dt^2}
$$

**Four fundamental kinematic equations** (velocity and acceleration are constant in these)
$v_f = v_0 + at$
$\Delta x = \frac{1}{2}(v_f+v_0)t$
$\Delta x = v_0 t + \frac{1}{2} at^2$
$v_f^2 = v_0^2 + 2a \Delta x$

**Integration with Velocity and Acceleration**

We know that the derivative of velocity is acceleration, $\frac{dv(t)}{dt} = a(t)$. The integral, or anti-derivative acts as a sort of 'inverse' that can be used to find the velocity from the acceleration formula. 
$$
v(t) +C = \int a(t)\, dt
$$
Alternatively, we can write this as the integrand, where $dv(t) = a(t)dt$
$$
v(t) + C = \int dv(t)
$$

**Example: Non-constant acceleration**
Let's say we have an object at rest at time $t =0$, an initial velocity $v_{o}=c$ of some non-zero constant, and acceleration $a(t) = bt^2$, $b$ being a constant also non-zero. This implies that $dv(t) = bt^2dt = d\left( \frac{bt^3}{3} \right)$. The velocity then becomes $v(t)+C = \int d\left( \frac{bt^3}{3} \right) = bt^3$. At time $t = 0, v_{0} +C = 0, C=-v_{0}$. Velocity as a function of time becomes: $v(t) = v_{0} + (\frac{bt^3}{3})$

**Change in velocity as the Definite Integral of acceleration**
$$
v(t)-v(t_{i})=\int_{t'=t_{i}}^{t'=t_{f}} a(t') \,dt'
$$
**Displacement as the Definite integral of velocity**
$$
x(t_{f})-x(t_{i}) = \int_{t'=t_{i}}^{t'=t_{f}} v(t')dt'
$$
