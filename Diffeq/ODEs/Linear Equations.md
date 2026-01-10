As we have seen before, first order [[Ordinary Differential Equations]] are in the form:
$$
a_{1}(x) \frac{dy}{dx} + a_{0}(x)y=g(x)
$$
We know this is linear since there is a linear equation in the variable $y$

We also have learned standard form too for [[Ordinary Differential Equations]], which can be expressed generally for linear equations 
$$
\frac{dy}{dx} +P(x)y=f(x)
$$
We solve these linear equations using separation of variables, looking for a solution on the interval $I$ where both $P$ and $f$ are continuous 

Two separable, linear equations:
$$
\frac{dy}{dx} + 2xy =0
$$
$$
\frac{dy}{dx} = y+5
$$
A non-separable linear equation:
$$
\frac{dy}{dx}+y=x
$$

Generally speaking, we can solve the general form of linear equations by multiplying both sides of the equation by a function $\mu(x)$

$$
\begin{align}
\frac{dy}{dx}+P(x)y=f(x) \\
\frac{d}{dx}[\mu(x)y] = \mu \frac{dy}{dx}+\frac{du}{dy} = \mu \frac{dy}{dx} + \mu Py \\ 
\frac{d\mu}{dx} = \mu p \\
\frac{1}{\mu} d\mu =P\,dx \\
\int \frac{1}{\mu} d \mu = \int P \,dx \\
\ln(\mu(x)) = \int P(x) \,dx \\
\mu(x) = e^{\int P(x) \,dx} \\
\end{align}
$$
This function is known as the integrating factor, and allows us to solve linear equations very easily. 

In general, to solve a first order equation, these steps must be followed:
1. Put the linear equation in standard form
2. Identify what $P(x)$ is, and then find the integrating factor $\mu(x) = e^{\int P(x) \, dx}$
3. Multiply both sides of the equation by the integrating factor, which causes the LHS to immediately follow the product rule and cancel out during separation of variables. 
4. Integrate both sides and solve for $y$

Putting all this together, generally this looks like the following:
$$
\begin{align}
\frac{dy}{dx} + P(x)y &= f(x) \\
e^{\int P(x) \, dx}  \frac{dy}{dx}+P(x)e^{\int P(x) \, dx}y &=f(x)e^{\int P(x) \, dx}\\
\frac{d}{dx}\left[ e^{\int P(x) \, dx} y\right] &= e^{\int P(x) \, dx} f(x) \\
e^{\int P(x) \, dx} &= \int e^{\int P(x) \, dx}f(x) \, dx
\end{align}
$$
Example:

Solve for $\frac{dy}{dx}-3y=0$
$$
\begin{align}
P(x) = -3, \, \mu(x) = e^{\int -3 \, dx} = e^{-3x} \\
e^{-3x} \frac{dy}{dx} -3e^{-3x}y=0 \\
\frac{d}{dx}[e^{-3x}y]=0 \\
\int \frac{d}{dx}[e^{-3x}y] \, dy= \int 0 \, dx \\
 e^{-3x}y=C, y = ce^{3x}
\end{align}
$$
IVP example:

Solve $\frac{dy}{dx}+y = x, \, y(0) = 4$
$$
\begin{align}
P(x)=1, \mu(x) = e^x \\
e^x \frac{dy}{dx}+e^xy=e^x x \\
\frac{d}{dx}[e^xy] = e^x x \\
\int \frac{d}{dx}[e^x]y \, dy= \int e^x x \, dx \\
e^xy= xe^x-e^x+C \\
y=x-1+Ce^{-x}, \\ 
4 = 0-1+Ce^{0} \\ 
C = 5 \\
y=xe^x-e^x+5e^{-x}
\end{align}
$$
Problem 23:
$$
\begin{align}
x \frac{dy}{dx}+(3x+1)y&=e^{-3x} \\
\frac{dy}{dx}+\frac{3x+1}{x}y &=\frac{1}{xe^{3x}} \\
P(x) &= \frac{3x+1}{x} \\
\mu(x) &= \exp\left( \int \frac{3x+1}{x} \, dx \right) \\
\mu(x) &= \exp(3x+\ln(x)) \\
\mu(x) &= xe^{3x} \\
xe^{3x} \frac{dy}{dx}+(3e^{3x}+e^{3x})y &= \frac{1}{x} \\
\frac{d}{dx}[xe^{3x}y]&=\frac{1}{x} \\
\int \frac{d}{dx}[xe^{3x}y] \, dx&= \int \frac{1}{x} \,dx \\
xe^{3x}y&= \ln(x) +C  \\
y&=\frac{\ln(x)+C}{x\exp(3x)}
\end{align}
$$
Interval: $(0, \infty)$


Problem 25:
$$
\begin{align}
\frac{dy}{dx}=x+5y, y(0)= 3 \\
\frac{dy}{dx}-5y = x \\
P(x) = -5, \mu(x) = e^{-5x} \\
e^{-5x} \frac{dy}{dx}-5e^{-5x}y=xe^{-5x} \\
\int\frac{d}{dx}[e^{-5x}y] =\int xe^{-5x} \, dx \\
e^{-5x}y = -\frac{1}{5}xe^{-5x}-\frac{1}{25}e^{-5x}+C \\
y=-\frac{1}{5}x-\frac{1}{25}+Ce^{5x} \\
3 = -\frac{1}{25} +C, \, C = \frac{76}{25}
\end{align}
$$
Problem 27:
$$
\begin{align}
xy'+y=e^x, \, y(1)=2 \\
y'+\frac{y}{x}=\frac{e^x}{x} \\
P(x) = \frac{1}{x}, \mu(x) = \exp(\ln(x))=x \\
xy'+y=e^x  \\
\int \frac{d}{dx}[xy] = \int e^x \, dx \\
xy = e^x+C, \, y = \frac{\exp(x)+C}{x} \\
C = 2-e, y = \frac{\exp(x) +2-e}{x}
\end{align}
$$
