We know that the main way for solving Linear [[Ordinary Differential Equations]] follows the integrating factor method, as so:
$$
y = c_{1}e^{-\int P(x)\, dx}+e^{-\int P(x)\, dx} \int e^{\int P(x)\, dx}f(x) \, dx
$$
This method assumes that $P(x), f(x)$ are both continuous over interval $I$.

The next idea hinges upon this, and relies on an understanding of homogeneity within differential equations

The main principle of Homogeneous equations is that they have all non-zero terms that include a factor of y or one of its derivatives. 

If we have a linear differential equation with the form:
$$
\frac{dy}{dt} +f(t)y=g(t)
$$
In order for it to be homogeneous, we must get rid of $g(t)$ since it is not factorable or a derivative of y. This becomes:
$$
\frac{dy}{dt}+f(t)y=0
$$
If the above differential equation has a solution $u(t)$, then:
$$
\frac{du}{dt}+f(t)u(t)=0
$$
$Cu(t)$ is also a solution for any constant $C$. By definition of variation of parameters, we can allow $C$ to be a function. If we look back at our original function, we can apply this logic:
$$
\frac{dy}{dt}+f(t)y=g(t)
$$
We can say that $y(t) = C(t)u(t)$, where $u(t)$ solves $\frac{dy}{dt}+f(t)y=0$. The next step is just to solve for $C(t)$. 
$$
\begin{align}
&y(t) = C(t)u(t) \\
&\frac{dy}{dt}=c(t)u(t)'+c(t)'u(t) \\
&\text{We can sub in these values to our differential equation:} \\
&c(t)u'(t)+c'(t)u(t) + f(t)c(t)u(t)=g(t) \\
&u'(t) + f(t)u(t)=0, c(t)u'(t)+f(t)c(t)u(t) = 0 \\
&c'(t)u(t) =g(t) \\
&c'(t)= \frac{g(t)}{u(t)} \\
&c(t) = \int \frac{g(t)}{u(t)} \, dt \\
\end{align}
$$
Example:
$$
\begin{align}
&\frac{dy}{dt}+\frac{2}{t}y=\frac{\cos(t)}{t^2} \\
&f(x) = \frac{2}{t}, g(x)  =\frac{\cos(t)}{t^2} \\
&\frac{dy}{dt}+\frac{2}{t}y=0 \\
& \frac{dy}{dt}=-\frac{2}{t}y  \\
& \frac{1}{y}\,dy=-\frac{2}{t}\,dt  \\
& \int \frac{1}{y} \,dy = -2 \int \frac{1}{t}\,dt \\
& \ln(y) = -2\ln(t)+C \\
&\ln(y)= \ln\left(\frac{C}{-2t)}\right) \\
&y = \frac{C}{t^2}
\end{align}
$$
We now assume that $C$ is a function. 
$$
\begin{align}
&y = \frac{C(t)}{t^2} \\
&\frac{dy}{dt}= C(t)'(t^{-2})+ C(t)'(t^{-2})' \\
&C(t)'(t^{-2})+ C(t)(t^{-2})' + \frac{2}{t}\left( \frac{C(t)}{t^2}\right) = \frac{\cos(t)}{t^2}  \\
&t^2C'(t)-2tC(t)+2tC(t)=t^2\cos(t) \\
&t^2C'(t) = t^2\cos(t) \\
&C'(t) = \cos(t) \\
& \int C'(t)= \int \cos(t) \\
& C(t) = \sin(t) + C \\
& y= \frac{\sin(t)+C}{t^2}
\end{align}
$$


