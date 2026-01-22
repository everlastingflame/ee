One of many [[Discrete Distributions]]
Accepts parameters $N,M, n$, where there are $M$ success among $N$ trials. The number $X$ of successes among the first $n$ trials has a hypergeometric distribution. 

$$
\begin{align}
f(x) = \frac{\begin{pmatrix} M \\ x\end{pmatrix} \begin{pmatrix}N-M  \\ n-x\end{pmatrix}}{\begin{pmatrix} N \\ n\end{pmatrix}} \\
\mu = np, \sigma^2 = \begin{pmatrix}
N - n \\ N-1
\end{pmatrix}npq
\end{align}
$$
