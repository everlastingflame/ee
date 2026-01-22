[[Continuous Distributions]]
Gives the time to the $r^{th}$ event, which indicates that $\text{Exponential}(\lambda) = \text{Gamma}(\lambda,1)$. The gamma distribution also applies in a different way when $r$ is not an integer. The factorial function is referred to below as $\Gamma(x)$. There is an alternate parameterization of the Gamma function in terms of parameters $\alpha$ and $\beta$, where $\alpha =r$ and $\beta = \frac{1}{\lambda}$ which is the expected time until the first event in a  Poisson process. 
$$
f(x) = \frac{1}{\Gamma(r)}\lambda^rx^{r-1}e^{-\lambda x} = \frac{x^{\alpha - 1}\exp\left( -\frac{x}{\beta} \right)}{\beta^\alpha \Gamma(\alpha)} , \text{for } x\in[0, \infty)
$$
$$
\begin{align}
\mu = \frac{r}{\lambda} = \alpha \beta, \sigma^2 = \frac{r}{\lambda^2} = \alpha \beta^2 \\
m(t) = \left( \frac{1-t}{\lambda} \right)^{-r} = (1-\beta t)^{-\alpha}
\end{align}
$$

