[[Discrete Distributions]]

$n$ independent trials are repeated with probability $p$ of success and $X$ is the trial number when $r$ successes are first achieved. Geometric$(p)$ = NegativeBinomial$(p,1)$

$$
\begin{align}
f(x) = \begin{pmatrix} x-1  \\ r-1\end{pmatrix}p^rq^{x-r}, \text{for } \, x=r, r+1 \\
\mu = \frac{r}{p}, \, \sigma^2 = \frac{rq}{p^2} \\
m(t) = \left( \frac{pe^t}{1-qe^t} \right)^r
\end{align}
$$
