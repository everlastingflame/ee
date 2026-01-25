### Problem 1
Plot the empirical cumulative distribution function of the following batch of numbers:
5,7,1,15,2,9,12,9,5,5

$$
\begin{align}
&\{5,7,1,15,2,9,12,9,5,5 \} \\
&n=10 \\
&\{1,2,5,5,5,7,9,9,12,15\} \\
&\text{ECDF}(1) = \frac{1}{10}(1) = 0.1 \\
&\text{ECDF}(2) = \frac{1}{10}(2) = 0.2 \\
&\text{ECDF}(5) = \frac{1}{10}(5) = 0.5 \\
&\text{ECDF}(7) = \frac{1}{10}(6) = 0.6 \\
&\text{ECDF}(9) = \frac{1}{10}(8) = 0.8 \\
&\text{ECDF}(12) = \frac{1}{10}(9) = 0.9 \\
&\text{ECDF}(15) = \frac{1}{10}(10) = 1
\end{align}
$$

```tikz
\begin{document}
\begin{tikzpicture}[scale=1.7, xscale = 0.4, yscale = 1.6]
    % Axes
    \draw[->] (-0.5,0) -- (16.5,0) node[right] {$x$};
    \draw[->] (0,-0.2) -- (0,1.3) node[above] {ECDF$(x)$};
    
    % Grid (optional)
    \draw[gray!30, very thin] (0,0) grid[step=1] (16,1);
    
    % Y-axis labels
    \foreach \y in {0, 0.1, 0.2, 0.5, 0.6, 0.8, 0.9, 1.0} {
        \draw (0,\y) -- (-0.1,\y) node[left, font=\small] {$\y$};
    }
    
    % X-axis labels
    \foreach \x in {0,1,2,5,7,9,12,15} {
        \draw (\x,0) -- (\x,-0.05) node[below, font=\small] {$\x$};
    }
    
    % ECDF step function
    % Start at 0
    \draw[blue, thick] (0,0) -- (1,0);
    
    % Jump at x=1 to 0.1
    \draw[blue, thick, fill=blue] (1,0) circle (1.5pt);
    \draw[blue, thick, fill=white] (1,0.1) circle (1.5pt);
    \draw[blue, thick] (1,0.1) -- (2,0.1);
    
    % Jump at x=2 to 0.2
    \draw[blue, thick, fill=blue] (2,0.1) circle (1.5pt);
    \draw[blue, thick, fill=white] (2,0.2) circle (1.5pt);
    \draw[blue, thick] (2,0.2) -- (5,0.2);
    
    % Jump at x=5 to 0.5
    \draw[blue, thick, fill=blue] (5,0.2) circle (1.5pt);
    \draw[blue, thick, fill=white] (5,0.5) circle (1.5pt);
    \draw[blue, thick] (5,0.5) -- (7,0.5);
    
    % Jump at x=7 to 0.6
    \draw[blue, thick, fill=blue] (7,0.5) circle (1.5pt);
    \draw[blue, thick, fill=white] (7,0.6) circle (1.5pt);
    \draw[blue, thick] (7,0.6) -- (9,0.6);
    
    % Jump at x=9 to 0.8
    \draw[blue, thick, fill=blue] (9,0.6) circle (1.5pt);
    \draw[blue, thick, fill=white] (9,0.8) circle (1.5pt);
    \draw[blue, thick] (9,0.8) -- (12,0.8);
    
    % Jump at x=12 to 0.9
    \draw[blue, thick, fill=blue] (12,0.8) circle (1.5pt);
    \draw[blue, thick, fill=white] (12,0.9) circle (1.5pt);
    \draw[blue, thick] (12,0.9) -- (15,0.9);
    
    % Jump at x=15 to 1.0
    \draw[blue, thick, fill=blue] (15,0.9) circle (1.5pt);
    \draw[blue, thick, fill=white] (15,1) circle (1.5pt);
    \draw[blue, thick] (15,1) -- (16,1);
    \draw[blue, thick, fill=blue] (16,1) circle (1.5pt);
    
    % Data points (optional, for emphasis)
    \fill[red] (1,0.1) circle (1.5pt);
    \fill[red] (2,0.2) circle (1.5pt);
    \fill[red] (5,0.5) circle (1.5pt);
    \fill[red] (7,0.6) circle (1.5pt);
    \fill[red] (9,0.8) circle (1.5pt);
    \fill[red] (12,0.9) circle (1.5pt);
    \fill[red] (15,1) circle (1.5pt);
    
\end{tikzpicture}
\end{document}
```


### Problem 2

![[Pasted image 20260125170341.png]]

$$
\begin{align}
&\text{What is the percentile rank of the data value 3?}: 30 \\
&\text{What is the percentile rank of the data value 4.5?}: 95 \\
&\text{What is the data value of the 60th percentile?}: 3.7 \\
&\text{5 number summary}: \text{Min}=2, \text{Max}=5, \text{Q1,Q2,Q3} = \{3, 3.57, 4.14\} \\
&\text{Range of the dataset}: 3 \\
&\text{Mode of the dataset}: 3 \text{, since it has the biggest jump in the ECDF}
\end{align}
$$

### Problem 3
Consider the Rayleigh distribution with parameters $\theta_{0}$ and $\theta_{1}$

$$
F(t) = 1-\exp\left( -\theta_{0}t-\frac{1}{2} \theta_{1}t^2 \right)
$$
a.) Find the hazard function (failure rate) for $F$

$$
\begin{align}
&F(t) = 1- \exp\left( -\theta_{0}t - \frac{1}{2} \theta_{1}t^2 \right) \\
&f'(t) = (\theta_{0}+\theta_{1}t)\exp\left( -\theta_{0}t - \frac{1}{2} \theta_{1}t^2 \right) \\
&h(t) = \frac{f(t)}{1-F(t)} \\
&h(t) = \frac{(\theta_{0}+\theta_{1}t)\exp\left( -\theta_{0}t - \frac{1}{2} \theta_{1}t^2 \right) }{1-(1- \exp\left( -\theta_{0}t - \frac{1}{2} \theta_{1}t^2 \right))} \\
&h(t) = \frac{(\theta_{0}+\theta_{1}t)\exp\left( -\theta_{0}t - \frac{1}{2} \theta_{1}t^2 \right) }{\exp\left( -\theta_{0}t - \frac{1}{2} \theta_{1}t^2 \right))} \\
&h(t) = \theta_{0}+\theta_{1}t
\end{align}
$$
b.) What values of $\theta_{1}$ for $F$ have a failure rate that's positive, negative, or constant?
$$
\begin{align}
\text{Positive: } 0<\theta_{1} \\
\text{Negative: } \theta_{1} < 0 \\
\text{Constant: } \theta_{1} = 0
\end{align}
$$

### Problem 4
Given the following data: 
32.1 24.9 29.4 40.2 36.2 33.0 28.5 33.4 38.1

a.) Construct a normal probability plot
Data sorted:
24.9 28.5 29.4 32.1 33.0 33.4 36.2 38.1 40.2

Using formula
$$\begin{align}
&n=9 \\
&\frac{100(i-0.5)}{9}
\end{align}
$$

| Value      | 24.9  | 28.5  | 29.4  | 32.1  | 33.0 | 33.4  | 36.2  | 38.1  | 40.2  |
| ---------- | ----- | ----- | ----- | ----- | ---- | ----- | ----- | ----- | ----- |
| percentile | 5.55  | 16.66 | 27.77 | 38.88 | 50   | 61.11 | 72.22 | 83.88 | 94.44 |
| z-value    | -1.59 | -.97  | -.59  | -.42  | 0    | .28   | .59   | .99   | 1.59  |


b.) From the plot, determine if it follows a normal distribution

![[Pasted image 20260125175359.png]]

This seems to follow a light-tailed normal distribution. 