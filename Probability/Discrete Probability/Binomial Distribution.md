[[Discrete Distributions]]

Conceptually, the binomial distribution asks how many success in $n$ Bernoulli trials. Once again, a Bernoulli trial is just a trial where there is either a success with probability $p$ or failure $q$. In this distribution, $X$ is the sum of $n$ independent trials, $X=x$ indicates that there were $x$ success in $n$ trials. 

$$
\begin{align}
&f(x) = \begin{pmatrix} n \\ x\end{pmatrix} p^x(1-p)^{n-x}, \,\text{for} \, x=0,1,\dots n \\
&\mu = np, \sigma^2 = np(1-p) = npq \\
&m(t) = (pe^t+q)^n
\end{align}
$$
Sampling with replacement happens when we have a set of $N$ elements and along with this a set of $M$ preferred elements, or elements that when sampled would be a success. When we do this, the members of the set are put back into circulation, so the cardinality of the set remains the same. Selecting a preferred element ends up in a success with probability $\frac{M}{N}$, and a failure (not selecting the preferred element) has probability $q = 1-p = \frac{N-M}{N}$
