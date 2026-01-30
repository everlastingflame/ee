[[Statistical Methods]]
### Problem 1
Suppose that $X$ follows a geometric distribution: 
$$
P(X=k) = p(1-p)^{k-1}
$$
and assume a random sample $X_{1}, X_{2}, \dots ,X_{n}$

a.) Find the method of moments estimator of $p$
$$
\begin{align}
E(X) = \frac{1}{n}\sum_{i=1}^nX_{i}^k \\
E(X) = \frac{1}{p} \\
\frac{1}{p} = \frac{1}{n} \sum_{i=1}^n X_{i}^k \\
1=p\left( \bar{x}\right) \\
\hat{P}_{\text{MME}} = \frac{1}{\bar{x}}
\end{align}
$$
b.) Find the MLE of $p$
$$
\begin{align}
&L(p) = P(X_{1}=x_{1}) \cdot P(X_{2}=x_{2})\cdot\dots P(X_{n}=x_{n}) \\
&L(p) = p(1-p)^{x_{1}-1} \cdot p(1-p)^{x_{2}-1}\cdot\dots p(1-p)^{x_{n}-1} \\
&L(p) = \prod_{i=1}^n p(1-p)^{x_{i}-1} \\
&l(p) = \ln\left(\prod_{i=1}^n p(1-p)^{x_{i}-1}\right) \\
&l(p) = n\ln(p)+\ln(1-p)\sum_{i=1}^n(x_{i}-1) \\
&l(p) = n\ln(p)+\frac{n\ln(1-p)\sum_{i=1}^n(x_{i}-1)}{n} \\
&l(p) = n\ln(p) + n\ln(1-p)(\bar{x}-1) \\
&l'(p) = \frac{n}{p}-\frac{n(\bar{x}-1)}{1-p} \\
&\frac{n}{p}=  \frac{n(\bar{x}-1)}{(1-p)}\\
&n(1-p) = pn(\bar{x}-1)\\ 
&1-p = p(\bar{x}-1) \\
&1=\bar{x}p -p +p\\ 
&1=\bar{x}p\\
&\hat{P}_{\text{MLE}} = \frac{1}{\bar{x}}
\end{align}
$$
c.) Find the MLE estimate of $p$ if the dataset is $\{1, 5, 1, 2, 6, 2, 3, 7, 3, 8 \}$
$$
\begin{align}
&\hat{p}_{\text{MLE}} = \frac{1}{\bar{x}} \\
&\bar{x} = \frac{38}{10}=3.8 \\
&\hat{p}_{\text{MLE}} = \frac{1}{3.8} \approx 0.263
\end{align}
$$

### Problem 2
Suppose that $X_{1}, X_{2},\dots X_{n}$ are i.i.d. with density function:
$$
\begin{align}
&f(x|\theta) = e^{-(x-\theta)}, \, x \geq \theta \\
&\text{and } f(x|\theta) = 0, \, \text{Otherwise}
\end{align}
$$
a.) Find the method of moments estimator for $\theta$


$$
\begin{align}
E[X] &= \int_{\theta}^\infty xe^{-(x-\theta)} \, dx \\
&=\int_{\theta}^\infty \frac{xe^\theta}{e^x} \, dx \\
&= e^\theta \int_{\theta}^\infty \frac{x}{e^x} \\
&= e^\theta[-xe^{-x}-e^{-x}]_{\theta}^\infty \\
&=-\lim_{ x \to \infty }xe^{-x}-\lim_{ x \to \infty } e^{-x} - (-\theta e^{-\theta} -e^-{\theta})\\ 
&= \frac{\lim_{ x \to \infty }x}{\lim_{ x \to \infty }e^{x} } = \frac{\lim_{ x \to \infty }1}{\lim_{ x \to \infty } e^{x}} =0  \\
&= e^\theta[\theta e^{-\theta}+e^{-\theta}] \\
&= \theta+1
\end{align}
$$
$$
\begin{align}
E(X) &= \frac{1}{n}\sum_{i=1}^nX_{i}^k  \\
E(X) &= \theta+1 \\
\theta + 1 &= \bar{x} \\
\theta &= \bar{x}-1 \\
\bar{\theta}_{\text{MME}} &= \bar{x}-1
\end{align}
$$

b.) Find the MLE of $\theta$
$$
\begin{align}
L(f) &= \prod_{i=1}^n e^{-(x_{i}-\theta)} \\
l(f) &= \log\left( \prod e^{-(x_{i}-\theta)} \right) \\
l(f) &= \sum_{i = 1}^n \log(e^{-(x_{i}-\theta)}) \\
l(f) &= \sum_{i=1}^n \log\left(  \frac{e^\theta}{e^{x_{i}}}  \right) \\
&= \sum_{i=1}^n \log(e^\theta) - \log(e^{x_{i}}) \\ 
&=\sum_{i=1}^n \theta-x_{i}\\
&= n\theta - \sum_{i=1}^n x_{i} \\
&= n\theta - \bar{x} \\
 \frac{\partial f}{\partial \theta} &= n \\
\hat{\theta}_{\text{MLE}} &= \text{min}(x_{1},x_{2},\dots,x_{n})=x_{1}
\end{align}
$$

### Problem 3
Suppose that $X_{1},X_{2}, \dots , X_{n}$ are i.i.d. random variables on the interval $[0,1]$ with the density function
$$
f(x;a) = \frac{\Gamma(3\alpha)}{\Gamma(\alpha)\Gamma(2\alpha)}x^{\alpha-1}(1-x)^{2\alpha-1}
$$
where $\Gamma$ is the gamma function and where $\alpha > 0$ is a parameter to be estimated from the
sample. Given that
$$
\begin{align}
E(X) = \frac{1}{3} \\
Var(x) = \frac{2}{9(3\alpha+ 1) }
\end{align}
$$
a.) Find the method of moments estimator of $\alpha$ 
$$
\begin{align}
E(X) &= \frac{1}{n} \sum_{i=1}^n x_{i} \\
E(X^2) &= \frac{1}{n} \sum_{i=1}^n x_{i}^2 \\
E(X) &= \frac{1}{3} \\
E(X^2) &= Var(X) + E(X)^2 = \frac{2}{9(3\alpha+1)} +\frac{1}{9} \\
E(X^2) &= \frac{1}{n} \sum_{i=1}^n x_{i}^2 \\
\frac{2}{9(3\alpha+1)}+\frac{1}{9} &= \frac{1}{n} \sum_{i=1}^n x_{i}^2 \\
\dots \text{FUCK}
\end{align}
$$





