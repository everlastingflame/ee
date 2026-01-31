[[Probability]]

Variance conceptually is just the spread of the values of a distribution from their mean. If $X$ is a random variable with mean $\mu$, then the variance $\text{Var}(X)$ is defined as:
$$
\text{Var}(X) = E[(X-\mu)^2]
$$
Variance can also be calculated as:
$$
\begin{align}
\text{Var}(X) &= E[(X-\mu)^2] \\
&= \sum_{x}(x-\mu)^2p(x) \\
&= \sum_{x} (x^2 - 2\mu x +\mu^2)p(x) \\
&= \sum_{x} x^2p(x) - 2\mu \sum_{x} xp(x) + \mu^2 \sum_{x}p(x) \\
&= E[X^2] - 2\mu^2 +\mu^2 \\
&= E[X^2] -\mu^2 \\
&= E[X^2] - (E[X])^2
\end{align}
$$

More operations with variance:
$\text{Var}(aX +b) = a^2\text{Var}(x)$

Proof:
$$
\begin{align}
\text{Var(aX +b)} &= E[(aX + b-a\mu +b)^2] \\
&=E[a^2(X-\mu)^2] \\
&=a^2E[(X-\mu)^2] \\
&=a^2 \text{Var}(x)
\end{align}
$$
The square root of the variance is the standard deviation. 

