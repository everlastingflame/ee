### Substitution overview

[[Ordinary Differential Equations]] sometimes cannot be solved with typical methods and require transforming through the substitution. An example of this is if we have an equation $\frac{dy}{dx} = f(x,y)$ where we substitute $y=g(x,u)$, $u$ being a function of variable x. If $u$ has partial derivatives, then we can find through chain rule that:
$$
\frac{dy}{dx}= \frac{\partial f}{\partial x} \frac{dx}{dx}+\frac{\partial g}{\partial u} \frac{du}{dx}= g_{x}(x,u)+g_{u}(x,u) \frac{du}{dx}
$$
We can then replace $\frac{dy}{dx}$ with the equation that we just found and also replace $f(x,y)$ with $f(x,g(x,u))$. 
$$
g_{x}{x,u}+g_{u}(x,u) \frac{du}{dx} = f(x,g(x,u))
$$
When solved has the form:
$$
\frac{du}{dx} = F(x,u)
$$
Finding a solution will yield $u=\phi(x)$ and to solve the original equation we can find that it will become $y = g(x,\phi (x))$

### Homogenous Equations

By definition a homogenous equation is one that exhibits the following property:
$$
f(tx,ty) = t^{\alpha}f(x,y)
$$
If an equation has this factorization for some real number $\alpha$, it is considered a homogenous equation. An example is the equation $f(x,y) = x^3+y^3$. It can be broken down:
$$
f(tx,ty) = (tx)^3+(ty)^3 = t^3(x^3+y^3) = t^3f(x,y)
$$
This equation is homogenous and of degree 3. A first order DE in differential form:
$$
M(x,y)dx + N(x,y)dy = 0
$$
Is considered homogenous if both $M$ and $N$ are homogenous with the same degree. It can also be shown that:
$$
\begin{align}
&M(tx,ty) = t^{\alpha}M(x,y)dx,\, N(tx,ty) = t^{\alpha}N(x,y) \\
&M(x,y) = x^{\alpha}M(1,u), \, N(x,y) = x^{\alpha}N(1,u), u =\frac{y}{x} \\
&M(x,y) = x^{\alpha}M(v,1), \, N(x,y) = x^{\alpha}N(v,1), v =\frac{x}{y}
\end{align}
$$
The substitutions where $y=ux$ or $x=vy$ that require $u,v$ to be independent variables allow the equations to reduce to first-order separable differential equations. 

Example:

$$
\begin{align}

\text{Solve } (x^2+y^2)\,dx + (x^2-xy)\, dy = 0 \\
M(x,y)=x^2+y^2, \, N(x,y) = x^2-xy \\
y=ux, dy = udx+xdu \\
(x^2+(u^2x^2))\,dx+(x^2-x^2u)[udx+xdu] = 0 \\
x^2(1+u)dx+x^3(1-u)du=0 \\
\frac{1-u}{1+u}du + \frac{dx}{x}=0 \\
\left[ -1+ \frac{2}{1+u}\right]du +\frac{dx}{x}=0  \\
-u+2\ln|1+u|+\ln|x|=\ln|c| \\
-\frac{y}{x}+2\ln|1+ \frac{y}{x}| + \ln|x| = \ln|c| \\
\ln| \frac{(x+y)^2}{cx}| = \frac{y}{x}, (x+y)^2=c\exp\left( \frac{y}{x} \right)
\end{align}
$$
### Bernoulli's Equation
The differential equation
$$
\frac{dy}{dx}+P(x)y = f(x)y^n
$$
Where $n$ is any real number is called Bernoulli's Equation. $n=1,0$makes the equation linear, and for any other number the substitution $u = y^{1-n}$ reduces any equation into a linear one.

Example:
$$
\begin{align}
\text{Solve } \, x \frac{dy}{dx} +y = x^2y^2 \\
\frac{dy}{dx} + \frac{1}{x}y = xy^2 \\
u = y^{1-2} = y^{-1}, y = u^{-1} \\
\frac{dy}{dx} = \frac{dy}{du} \frac{du}{dx}=-u^{-2} \frac{du}{dx} \\
\frac{du}{dx} -\frac{1}{x}u=-x \\
\exp\left( -\int \frac{dx}{x} \right) = \exp(-\ln x)=\exp (x^{-1})=x^{-1} \\
\frac{d}{dx}[x^{-1}u]=-1 \\
x^{-1}u = -x+c, u=-x^2 + cx, y = \frac{1}{(-x^2+cx)}
\end{align}
$$
