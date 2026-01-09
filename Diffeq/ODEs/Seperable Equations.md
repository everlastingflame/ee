[[Ordinary Differential Equations]] that are defined as first order and have variables which can be separated algebraically. They can be solved further through integration. This is one of the most fundamental and basic ways of solving these equations. 

In normal form, a separable equation tends to look like:
$$
\frac{dy}{dx} = g(x)h(y)
$$
The process of solving these then turns into:

$$
\begin{align}
&\frac{dy}{dx}=g(x)h(y) \\
&\frac{1}{h(y)}dy=g(x)dx \\
&p(y)=\frac{1}{h(y)} \\
&p(y)\, dy = g(x)\, dx
\end{align}
$$
If $\phi(x)$ is a solution, then $p(\phi(x))\phi'(x) = g(x)$
$$
\begin{align}
\int p(\phi(x))\phi'(x)\, dy&=\int g(x)\, dx \\
\int p(y) \, dy &= \int g(x) \, dx \\
H(y)&= G(x) +C
\end{align}
$$
Where $H(y), G(x)$ are integrals of $\frac{1}{h(y)}, g(x)$

Examples:
$$
\begin{align}
\frac{dy}{dx}&=-\frac{y}{x}, \, \, y(4)= -3 \\
y\,dy &= -x \, dx \\
\int y \, dy&= -\int x \, dx \\
\frac{y^2}{2}&= -\frac{x^2}{2}+C \\
y^2+x^2 &= C^2  \\
(-3)^2+(4)^2 &= C^2 \\
C&= 5 &  \\
y&=\sqrt{25-x^2}
\end{align}
$$
![[Pasted image 20260108175617.png]]
