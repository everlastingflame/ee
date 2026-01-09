By definition, [[Differential Equations]] are just equations in which we have derivatives of unknown functions with respect to independent variables. 

An Ordinary Differential Equation (ODE) is a diffeq that contains "ordinary" derivatives, or derivatives that are w.r.t a single variable. 

A partial differential equation (PDE) is a diffeq that contains partial derivatives with respect to two or more independent variables

Examples of ODEs:
$$
\begin{align}
\frac{dy}{dx}+5y &= e^x \\
\frac{d^2x}{dy^2}-\frac{dy}{dx}+6y &= 0 \\
\frac{dy}{dt}+\frac{dy}{dx} &= 2x+y
\end{align}
$$
Examples of PDEs:
$$
\begin{align}
\frac{\partial ^2u}{\partial x^2}+\frac{\partial^2u}{\partial y^2} =0 \\
\frac{\partial^2u}{\partial x^2}=\frac{\partial^2u}{\partial t^2} - 2 \frac{\partial u}{\partial t}
\end{align}
$$

The order of differential equations is just the order of the highest derivative in the problem. For example, $\frac{d^2y}{dx^2}+5\left(\frac{dy}{dx}\right)^3-4y=e^x$ is second order, because the order of the highest derivative is 2

Sometimes differential equations are written in what's called differential form. It looks like the following:
$$
M(x,y)dx + N(x,y)dy = 0
$$
We can manipulate equations to achieve this. Example below:
$$
\begin{align}
(y-x)dx+4xdy = 0\\
y-x+4x \frac{dy}{dx}=0 \\
4x \frac{dy}{dx}+y=x
\end{align}
$$
Conversely, we can do:
$$
\begin{align}
6xy \frac{dy}{dx}+x^2+y^2=0 \\
(x^2+y^2)dx+6xy\,dy=0
\end{align}

$$

**Normal Form**
We can solve for $\frac{dy}{dx}$ only if we are in normal form. It is simple algebra.

$$
\begin{align}
4x \frac{dy}{dx} + y = x \\
\frac{dy}{dx}=\frac{x-y}{4x}
\end{align}
$$
The idea of normal form is to solve for the highest order differential. Here is another example
$$
\begin{align}
y''-y'+6=0 \\
y''=y'-6
\end{align}
$$

**Linear ODE**
A linear ODE only exists when:
- A dependent variable y and all of its derivatives have degree 1, i.e. the power cannot be greater than 1
- The coefficients are dependent on the independent variable x

The following equations are not linear ODEs:
$$
\begin{align} 
(1-y)y'+2y=e^x \\
\frac{d^2y}{dx^2}+\sin y=0 \\
\frac{d^4y}{dx^4}+y^2=0
\end{align}
$$
The first equation depends on y, violating the second principle. The second equation has a nonlinear function of y. The third equation again has a nonlinear function of y as well. 

**Solutions to ODEs**
Any function $\phi$ defined and continuous on an interval $I$ and containing $n$ derivatives is a solution when substituted into an $n$-th order differential equation results in an identity. It is important to note that it is only a solution on the interval $I$

Example:
$$
\begin{align}
\frac{dy}{dx}=xy^{\frac{1}{2}} \\
y=\frac{1}{16}x^4 \\
\frac{dy}{dx}=x\left(\frac{1}{16}x^4\right)^{\frac{1}{2}}=\frac{x^3}{4} \\
y'= \frac{x^3}{4}
\end{align}
$$

A solution to a differential equation that is identically 0 on an interval $I$ is a trivial solution


**Explicit and Implicit solutions**
An **Explicit** solution is a solution in which the dependent variables are expressed in terms of the independent variables and its constants


**Families of Solutions**
When solving first order diffeqs, we are left with a constant or parameter C as a result of integration. The constant provides what's called a one-parameter family of solutions. If we were solving a $n$-th order diffeq, then we would be left with an n-parameter family of solutions. A single differential equation can have an infinite number of solutions When we substitute a value in for C, this becomes a particular solution. A singular solution arises when a parameter cannot be specialized to provide this solution. 