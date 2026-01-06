When solving [[Differential Equations]] we also might seek particular conditions that satisfies $y(x)$, these conditions imposing some value onto the original, unknown equation and its derivatives at a number $x_{0}$. The following is an $n$-th order IVP. 

$$
\begin{align}
\text{solve: } &\frac{d''}{dx^n}=f(x,y,y',\dots,y^{n-1}) \\
\text{subject to: } &y(x_{0}) = y_{0},y'(x_{0}), \dots, y^{n-1}(x_{0}) = y_{n-1} 
\end{align}
$$
$y_{0}, y_{1},\dots ,y_{n-1}$ are all arbitrary constants. The values of $y(x)$ and its first $n-1$ derivatives at $x_{0},y(x_{0})=y_{0}, y'(x_{0}),y''(x_{0})\dots y^{n-1}(x_{0})$ are the **initial conditions** or ICs. 

Given a first-order diffeq, the IVP would look like:
$$
\begin{align}
\text{Solve: } &\frac{dy}{dx}=f(x,y) \\
\text{Subject to: } &y(x_{0})=y_{0}
\end{align}
$$
A second order IVP is:
$$
\begin{align}
\text{Solve: } &\frac{d^2y}{dx^2} =f(x,y,y') \\
\text{Subject to: } &y(x_{0})=y_{0},y'(x_{0})=y_{1}
\end{align}
$$

Examples:

$$
\begin{align}
\text{Solve: } &y'=y, y=ce^x \\
\text{Subject to: } &y(0) = 3 \\
&3= ce^0, 3=c, y=3e^x
\end{align}
$$


This example has a family of solutions, $c_{1} \cos(4t)+c_{2}\sin(4t)=x$
$$
\begin{align}
\text{Solve: } &x''+16x=0 \\
\text{Subject to: } &x\left( \frac{\pi}{2} \right)=-2, x'\left( \frac{\pi}{2} \right)=1 \\
c_{1}\cos(2\pi)+c_{2}\sin(2\pi) &=-2, c_{1}=-2 \\
x(t)&=-2\cos(4t)+c_{2}\sin(4t) \\
x'(t) &= 8\sin(4t) + 4c_{2}\cos(4t) \\
x'\left(\frac{\pi}{2} \right) &= 8\sin(2t)+4c_{2}\cos(2t) = 1, c=\frac{1}{4} \\
x&=-2\cos(4t)+ \frac{1}{4}\sin(4t)
\end{align}
$$
IVPs have unique solutions when the solutions themselves have only one solution curve passing through the same point. 

Question 15. 1.2 

Find Two solutions through inspection of the IVP. 

$$
\begin{align}
&y'=3y^{\frac{2}{3}}, y(0)=0 \\
&y'(0)=0, y(0) =0 \text{, trivial sol} \\
& \frac{dy}{dx}=3y^{\frac{2}{3}}, dy = 3y^{\frac{2}{3}}dx \\
& y^{-\frac{2}{3}}dy = 3dx, \int y^{-\frac{2}{3}}dy=\int 3dx \\
& 3y^{\frac{1}{3}} = 3x + C, y = (x+C)^3 \\
& y(0)=(0+C)^3, 0=C, y=x^3
\end{align}
$$
Question 16
$$
\begin{align}
&xy' = 2y, y(0)=0 \\
& x \frac{dy}{dx}=2y, \frac{dy}{dx}=\frac{2y}{x} \\
& \frac{dy}{dx} \frac{1}{2y}=\frac{1}{x}, \frac{1}{2y}dy=\frac{1}{x}dx \\
& \int \frac{1}{2y}dy=\int \frac{1}{x}dx \\
& \frac{\ln(y)}{2} = \ln(x) + C \\
& y = x^2e^C \\
& 0=0  \\
& y= x^2
\end{align}
$$



