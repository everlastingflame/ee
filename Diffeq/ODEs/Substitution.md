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

