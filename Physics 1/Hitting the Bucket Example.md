[[2D Kinematics]]

A person is holding a pail while standing on a ladder. The person releases the pail from
rest at a height $h_{1}$ above the ground. A second person, standing a horizontal distance $s$
from the pail, aims and throws a ball the instant the pail is released in order to hit the pail.
The person releases the ball at a height $h2$ above the ground, with an initial speed $v_{}0$ , and
at an angle $\theta_{0}$ with respect to the horizontal. Assume that $v_{0}$ is large enough so that the
stone will at least travel a horizontal distance $s$ before it hits the ground. You may ignore
air resistance.

a.) Find an expression for the angle $\theta_{0}$ that the person aims the ball in order to hit the
pail. Does the answer depend on the initial velocity?

There are two objects in free fall here, the pail and the ball. The ball is subject to 2D motion, whereas the pail is only subject to 1D motion. The parameters are $h_{1}$, $h_{2}$, $v_{0}$, and $s$, becoming their own functions. 

We can choose our ball initial position to be $h_{2}$ above the origin, released in y positive direction, and heading positively toward the x direction. 

The pail is $h_{1}$ above the x axis and has height position $y_{1}(t)$ 

The pail has only constant acceleration downward, $a_{1,y} = -g$.
The ball has constant acceleration downward $a_{2,y} = -g$ and horizontal acceleration $a_{2,x} = 0$

The initial conditions for the pail are:

$$
\begin{align}
v_{y,1}(t) &= -gt \\
y_{1}(t) &= h_{1}-\frac{1}{2}gt^2
\end{align}
$$

The initial conditions for the ball are:
$$
\begin{align}
v_{x,2}(t)&=v_{0,x} \cos \theta  \\
x_{2}(t) &= v_{0,x}\cos \theta t \\
v_{y,2}(t) &= v_{0,y}\sin \theta -gt \\
y_{2}(t) &=h_{2}+ v_{0,y}\sin \theta t_{0}- \frac{1}{2} gt^2
\end{align}
$$
To find the angle, we need to find the time, the location, and the initial angle, we can set the position of the ball and the pail equal to each other. This can be found through the following:
$$
\begin{align}
y_{1}(t_{a}) &= y_{2}(t_{a})  \\
x_{2}(t_{a})&=x_{1}=s
\end{align}
$$
this simplifies to 
$$
\begin{align}
h_{1}-\frac{1}{2}gt^2 &=h_{2}+v_{0,y}\sin \theta t_{0}-\frac{1}{2}gt^2 \\
v_{0}\cos \theta_{0} t &=s
\end{align}
$$
Simplifying further:
$$
\begin{align}
0&=h_{2}-h_{1}+v_{0}\sin \theta t \\
t&= \frac{h_{1}-h_{2}}{v_{0}\sin \theta} \\
s&=v_{0}\sin \theta\cdot \frac{h_{1}-h_{2}}{v_{0}\cos} \\
s&=\tan \theta(h_{1}-h_{2})  \\
\theta_{0} &= \tan^{-1}\left( \frac{h_{1}-h_{2}}{s}\right)
\end{align}
$$
The answer does not depend on initial velocity


