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
