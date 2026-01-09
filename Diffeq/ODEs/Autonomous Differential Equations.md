Autonomous Differential Equations are a set [[Ordinary Differential Equations]] that do not contain an explicit independent variable. For example, if we have an ODE with a differential with respect to time $t$, the ODE will not contain this variable anywhere in the system. This creates [[Solution curves]] that are constant along the independent axis, but change along the dependent axis. only changing based on the current state of the dependent variable. An example of an ADE is as follows:
$$
\frac{dy}{dx}=f(y)
$$
The equation reads as the instantaneous rate of change of the function $f(y)$ with respect to $x$, but as there is no $x$, the diffeq can be determined as being autonomous. 

It is important to note when ADEs reach their equilibrium points, or points at which the rate of change is zero. Defined formally, an equilibrium point $f(c)$, $c$ being a real number occurs when $f(c) = 0$. An equilibrium solution to a differential equation occurs when $y(x) = c$. We can visually describe phase portraits and direction fields of ADEs by finding their equilibrium points and observing the change above and below them. 

Example:
$$
\frac{dP}{dt}=P(a-bP), \, \text{$a$ and $b$ are constants}
$$
If we set the equation equal to 0, this would indicate we are looking for points at which the rate of change is stationary. 
$$
0=P(a-bP),\, P=0, \, P= \frac{a}{b}
$$

```tikz
\begin{document}
\begin{tikzpicture}[scale=1.2]
    % Define regions with colors

    
    % Axes
    \draw[->] (-3,0) -- (3.5,0) node[right] {$t$};
    \draw[->] (0,-2) -- (0,4.5) node[above] {$P$};
    
    % Horizontal dashed line at a/b
    \draw[dashed, cyan] (-3,2) -- (3,2) node[left, pos=0, black] {$\frac{a}{b}$};
    
    % Vertical line at t=0 (phase line)
    \draw[thick] (-2.5,-2) -- (-2.5,4.5);
    \node[below] at (-2.5,-2) {phase line};
    
    % Vertical line at P0
    \draw[dashed] (0,-2) -- (0,4);
    
    % Point P0 on phase line
    \fill (-2.5,2) circle (2pt) node[right] {$P_0$};
    
    % Solution curves
    % Upper decreasing curve (starting from P above a/b)
    \draw[red, thick, ->] (0,3.5) to[out=0, in=150] (2.5,2.2);
    \fill (0,3.5) circle (1.5pt) node[left] {$P_0$};
    
    % Middle increasing curve (starting from P below a/b)
    \draw[blue, thick, ->] (0,1) to[out=0, in=210] (2.5,1.8);
    \fill (0,1) circle (1.5pt) node[right] {$P_0$};
    
    % Lower decreasing curve (starting from P in lower region)
    \draw[red, thick, ->] (0,-0.5) to[out=0, in=150] (2.5,-1.2);
    \fill (0,-0.5) circle (1.5pt) node[right] {$P_0$};
    
    % Arrows on phase line
    \draw[->, very thick, red] (-2.2,3.5) -- (-2.2,2.8);
    \draw[->, very thick, blue] (-2.2,1.2) -- (-2.2,1.8);
    \draw[->, very thick, red] (-2.2,-0.5) -- (-2.2,-1.2);
    
    % Region labels
    \node at (2,3) {$R_3$};
    \node at (2,1) {$R_2$};
    \node at (2,-1) {$R_1$};
    
    % Labels for behavior
    \node at (-1.5,3) {decreasing};
    \node at (-1.5,1) {increasing};
    \node at (-1.5,-1) {decreasing};
    
    % Label for tP-plane
    \node at (1,-2.3) {$tP$-plane};
    
    % Arrow labels on phase line
    \node[right] at (-2.2,3.5) {$P$};
    
    % Zero label
    \node[left] at (0,0) {$0$};
\end{tikzpicture}
\end{document}
```

| Interval                           | Sign $f(P)$ | $P(t)$ | Arrow |
| ---------------------------------- | ----------- | ------ | ----- |
| $\left(\frac{a}{b} ,\infty\right)$ | -           | Dec    | Down  |
| $\left( 0, \frac{a}{b} \right)$    | +           | Inc    | Up    |
| $(-\infty, 0)$                     | -           | Dec    | Down  |
At each critical point, we can describe the stability of the line. When the solution curves align at the same asymptote, this is known as a stable solution (i.e., the upper region has a decreasing slope and the lower region below the asymptote is increasing). When it is semi stable, the directions are pointing the same way, and when it is unstable, they are pointing opposite directions. So in this example, $\frac{a}{b}$ is a stable solution, and $0$ is unstable. 