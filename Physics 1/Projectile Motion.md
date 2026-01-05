**Initial Conditions**
The initial conditions of a [[2D Kinematics]] problem will usually decompose into the following vectors
$$
\vec{v_{0}}=\vec{v_{x,0}}\hat{i}+\vec{v_{y,0}}\hat{j}
$$
Projectile flight tends to be described as "a body is projected with the initial speed $v_{0}$at an angle with $\theta_{0}$ with respect to the horizontal". The components of initial velocity with respect to initial speed and angle 
$$
\begin{align}
v_{x,0}=v_{0}\cos \theta_{0} \\
v_{y,0} = v_{0}\cos \theta_{0}
\end{align}
$$
The magnitude of the initial velocity is
$$
v_{0}=(v^2_{x,0}+v^2_{y,0})^{\frac{1}{2}}
$$
The angle of a vector in 2d space is:
$$
\theta_{0}=\tan^{-1}\left( \frac{v_{y,0}}{v_{x,0}} \right)
$$
The initial position of a vector usually is given by
$$
\vec{r_{0}}=x_{0}\hat{i}+y_{0}\hat{j}
$$

For a free body diagram:
```tikz
\begin{document}
\begin{tikzpicture}[scale=1.5]
    % Axes
    \draw[->] (-0.5,0) -- (3,0) node[right] {$x$};
    \draw[->] (0,-0.5) -- (0,2.5) node[above] {$y$};
    
    % Origin label
    \node[below left] at (0,0) {$O$};
    
    % Curve (smooth path through points)
    \draw[thick] (0,0) .. controls (0.5,1.5) and (1,2.2) .. (1.5,2) 
                          .. controls (2,1.9) and (2.5,2) .. (3,2.2);
    
    % Point on curve
    \coordinate (P) at (1.5,2);
    \fill (P) circle (1pt);
    
    % Unit vectors at the point
    \draw[->,thick] (P) -- ++(0.4,0) node[above] {$\mathbf{\hat{i}}$};
    \draw[->,thick] (P) -- ++(0,0.4) node[left] {$\mathbf{\hat{j}}$};
    
    % Force vector
    \draw[->,thick] (P) -- ++(0,-0.5) node[right] {$\mathbf{\hat{F}}^{\varepsilon}$};
\end{tikzpicture}
\end{document}
```

The vector decomposition of force for a 2D free body diagram with only gravity acting on it is:
$$
{\vec{F}}^g=-mg \hat{j}
$$
Newton's second law states that the sum of the force $\vec{F}$ is equal to the product of the mass of the object and its acceleration. This can be defined with vectors like so:

$$
\vec{F}^{\text{total}} = m\vec{a}
$$
If we model an equation with only one force, that would imply for our system that $\vec{F}^{\text{total}}=\vec{F}^{g}$, so our force vectors with respect to y and x and would be:
$$
\begin{align}
-mg=ma_{y} \\
0=ma_{x}
\end{align}
$$
Which would make the y component just be $a_{y}=-g$




