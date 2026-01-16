If we look at the equation $y\,dx +x\,dy=0$ we can see that it is a separable and one of many first-order [[Ordinary Differential Equations]]. We can see that this equation is very similar to the differential of the function $f(x,y) = xy$, which is $d(xy) = y\,dx +x\,dy$. We can construct an apply a simple test known as the exact equation or exact differential $M(x,y)\,dx+N(x,y)\,dy=0$. If we can prove that this equation is the differential of the function $f(x,y)$ then we can construct $f$ through partial integration. 

If $z = f(x,y)$, where $f$ is a function of two variables with continuous derivatives, then we know that its differential is just $dz=\frac{\partial f}{\partial x}\,dx+ \frac{\partial f}{\partial y}dy$. 

If $f(x,y) =c$, then: $\frac{\partial f}{\partial x}\,dx+ \frac{\partial f}{\partial y}dy=0$. 

Example:
$$
\begin{align}
&x^2-5xy+y^3=c\\
&(2x-5y)\,dx+(-5x+3y^2)\,dy=0
\end{align}
$$
We can say that $x^2y^3\,dx +x^3y^2\,dy=0$ is exact because the left hand side is an exact differential 
$$
\begin{align}
d\left( \frac{1}{3} x^3y^3\right) = x^2y^3\,dx+x^3y^2\,dy 
 \\
M(x,y) = x^2y^3, N(x,y)=x^3y^2 \\
\frac{\partial M}{\partial y} = 3x^2y^2= \frac{\partial N}{\partial x}
\end{align}
$$
The last part of this equation is most important because it brings up a necessary and sufficient condition that tells us that in order for the exact equation to hold, besides being continuous on a rectangular region $R$, $a<x<b, c<y<d$, the partial derivative of $M$ in terms of $y$ and $N$ in terms of $x$ must be equal. 

Proof:
$$
\begin{align}
M(x,y) \,dx + N(x,y)\,dy = \frac{\partial f}{\partial x} dx+\frac{\partial f}{\partial y} dy
 \\
M(x,y)=\frac{\partial f}{\partial x}, \, N(x,y) = \frac{\partial f}{\partial y}\ \\
\frac{\partial M}{\partial y}=\frac{\partial}{\partial y}\left( \frac{\partial f}{\partial x} \right)= \frac{\partial^2f}{\partial x\partial y} = \frac{\partial}{\partial x} \left( \frac{\partial f}{\partial y} \right) = \frac{\partial N}{\partial x}
\end{align}
$$
If this equality holds, then the method of solution becomes the following if we're given an equation where  $M(x,y)\,dx +N(x,y)\,dy = 0$
$$
\begin{align}
&\frac{\partial f}{\partial x} = M(x,y) \\
&f(x,y)=\int M(x,y)\,dx +g(y) \\
&\frac{\partial f}{\partial y} = \frac{\partial}{\partial y} \int M(x,y) \, dx+g'(y) =N(x,y) \\
&g'(y) =N(x,y) - \frac{\partial}{\partial y} \int M(x,y)\,dx
\end{align}
$$
$g(y)$ is the constant of integration. 

Another example of a DE:
$$
\begin{align}
\text{Solve } 2xy\, dx+(x^2-1)\,dy=0 \\
M(x,y)=2xy, N(x,y)=(x^2-1), \\
\frac{\partial M}{\partial y} = 2x=\frac{\partial N}{\partial x} \\
\frac{\partial f}{\partial x}=2xy, \frac{\partial f}{\partial y}= x^2-1 \\
f(x,y)=\int M(x,y)\,dx = x^2y+g(y) \\
\frac{\partial f}{\partial y}=x^2+g'(y) = x^2-1 = N(x,y) \\
g'(y)= -1 \\
g(y)=-y \\
f(x,y)=x^2y-y, \, \, x^2y-y=c,y=\frac{c}{x^2-1}
\end{align}
$$

Sometimes it is possible to find an integrating factor in terms of $\mu(x,y)$ for non-exact differential equations, in the format $\mu(x,y)\,M(x,y)\,dx+\mu(x,y)\,N(x,y)\,dy=0$. If we want to find this $\mu(x,y)$ then the qualifier for exactness is such that: $(\mu M)_{y}=(\mu N)_{x}$. This can be expanded through product rule: 
$$
\begin{align}
\mu_{y}M+\mu M_{y}=\mu_{x}N+\mu N_{x} \\
\mu_{y}M-\mu_{x}N = (N_{x}-M_{y})\mu  \\
\mu_{x}N-\mu_{y}M = (M_{y} - N_{x})\mu
\end{align}
$$
Without using PDEs, we can solve the equation by assuming that $\mu$ only relies on one variable, so to proceed, we can have $\mu_{x}= \frac{d\mu}{dx}, \mu_{y}=0$
$$
\frac{d\mu}{dx} = \frac{M_{y}-N_{x}}{N}\mu
$$
If $\mu$ solely relies on $y$, then we can write:
$$
\frac{d\mu}{dy}=\frac{N_{x}-M_{y}}{M}\mu
$$
 Both of these equations are linear and separable if we find that this solely depends on either $x$ or $y$. If that is the case, then we can proceed with the integrating factor method, where the integrating factor for both cases respectively will be:
$$
\begin{align}
\mu(x) = \exp \int\left(\frac{M_{y}-N_{x}}{N} \right)\,dx \\
\mu(y) = \exp \int\left(\frac{N_{x}-M_{y}}{M} \right)\,dy
\end{align}
$$
Example: Non-exact DE made exact:

The equation $xy\, dx +(2x^2+3y^2-20)\,dy = 0$ is not exact, but we can recognize that $M = xy, N= 2x^2+3y^2-20$. We find that the partial derivatives $M_{y} = x, N_{x} = 4x$. If we try to use the quotient where our solution is in terms of x, we get 
$$
\frac{M_{y}-N_{x}}{N} = \frac{x-4x}{2x^2+3y^2-20}= \frac{-3x}{2x^2+3y^2-20}
$$
This is not helpful, since we want it to only rely on x. However using the other quotient is helpful:
$$
\frac{N_{x}-M_{y}}{N} = \frac{4x-x}{xy}= \frac{3x}{xy}=\frac{3}{y}
$$
The integrating factor then becomes: $\exp \int\frac{3}{y}\,dy = \exp(\ln y^3)=y^3$
After multiplying both sides by the integrating factor, we now have an exact equation:
$$
xy^4\,dx + (2x^2y^3+3y^5-20y^3)\,dy=0
$$
We can verify that this is an exact equation now and solve for a family of solutions. 
$$
\begin{align}
&M(x,y)=xy^4, \, N(x,y)=2x^2y^3+3y^5-20y^3 \\
&M_{y} = 4xy^3 = N_{x} \\
&\frac{\partial f}{\partial x} = xy^4, \frac{\partial f}{\partial y}=2x^2y^3+3y^5-20y^3 \\
&f(x,y)=\int xy^4 \, dx = \frac{x^2y^4}{2} +g(y) \\
& \frac{\partial f}{\partial y} = {2x^2y^3}+g'(y) \\
&g'(y) = 2x^2y^3+3y^5-20y^3 -{2x^2y^3} \\
&g'(y) = 3y^5-20y^3 \\
&g(y) = \int 3y^5-20y^3 \, dy \\
&g(y) = \frac{y^6}{2}-5y^4 \\
& \frac{1}{2}x^2y^4+\frac{1}{2}y^6-5y^4=C
\end{align}
$$


Question 4:
$$
\begin{align}
\text{Solve: } \, (\sin y-y\sin x)dx+(\cos x+x\cos y)\,dy=0 \\
M=\sin y-\sin x, \, N=\cos x+x\cos y -y \\
\frac{\partial f}{\partial x} = \sin y-\sin x \\
f(x,y)=\int \sin y-\sin x\, dx = x\sin y+y\cos x+g(y) \\
\frac{\partial f}{\partial y} = x\cos y+\cos x+g'(y) \\
g'(y)=\cos x+x\cos y-x\cos y-\cos x -y \\
g'(y)=-y, g(y) = \int-y \, dy = -\frac{y^2}{2} \\
x\sin y+y\cos x-\frac{1}{2}y^2=C
\end{align}
$$
