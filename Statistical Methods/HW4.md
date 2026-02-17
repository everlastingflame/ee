### Problem 1

Suppose that $X$ follows a geometric distribution $P(X=k) = p(1-p)^{k-1}$ and assume that an i.i.d sample $X_{1},X_{2},\dots,X_{n}$

a.) Find the Method of moments estimate $p$

$$
\begin{align}
E(X) &= \frac{1}{n}\sum_{i=1}^n x_{i} \\
E(X) &= \frac{1}{p} \\
\frac{1}{p} &= \bar{x} \\
\hat{p}_{\text{MME}} &= \frac{1}{\bar{x}} 
\end{align}
$$
b.) Find the MLE of p

$$
\begin{align}
L(p) &= \prod_{i=1}^n p(1-p)^{k_{i}-1} \\
L(p) &= p^n(1-p)^{\sum_{i=1}^nk_{i}-1} \\
l(p) &=n\log(p)+\log(1-p)\sum_{i=1}^{n}k_{i}-n\\
l'(p) &= \frac{n}{p}+\left(\frac{-1}{1-p} \right)\cdot\sum_{i=1}^n(k_{i}-n) \\
\frac{n}{p}&= \left( \frac{1}{1-p}\right) \cdot\sum_{i=1}^nk_{i}-n \\
\frac{n(1-p)}{p} &= \sum_{i=1}^n (k_{i}) -n \\
n-np &= p \sum_{i=1}^n k_{i}-np \\
n&=p\sum_{i=1}^n k_{i} \\
\hat{p}_{\text{MLE}} &=\frac{n}{\sum_{i=1}^n k_{i}} \\
\hat{p}_{\text{MLE}} &= \frac{1}{\bar{k}}=\frac{1}{\bar{x}}
\end{align}
$$
c.) Let $p$ have a uniform prior distribution on [0, 1]. What is the posterior distribution
of $p$? 

$$
\begin{align}
&\text{Prior: } 0\leq p\leq 1 \text{, 0 otherwise} \\
&\text{Likelihood: } L(p) = p^n(1-p)^{\sum_{i=1}^nk_{i}-1} \\
&\text{Posterior: } \propto 0\leq p^n(1-p)^{\sum_{i=1}^n k_{i}-1}\leq 1 \\
&\text{Posterior Mean: } \text{Beta}\left( n+1, \sum_{i=1}^nk_{i} \right) \\
&E(X) = \frac{\alpha}{\alpha + \beta} \\
&E(X) = \frac{n+1}{n+1 +\sum_{i=1}^k k_{i}} \\
&E(X) = \frac{n+1}{(1+\bar{k})n+1}
\end{align}
$$

### Problem 2
Let $X_{1}, X_{2}, \dots , X_{n}$ be an i.i.d sample from the Poisson distribution with mean $\lambda$, and let $T = \sum_{i=1}^n X_{i}$

a.) Use the definition of sufficiency to show that $T$ is sufficient for $\lambda$

$$
\begin{align}
&P(X_{1}=x_{1}, X_{2}=x_{2},\dots, X_{n}=x_{n} | T=x_{1}+x_{2}+\dots+x_{n}) \\
&= \frac{P\left( X_{1}=x_{1}\dots X_{n}=x_{n}|T=\sum_{i=1}^n x_{i}= T \right)}{P(T=x_{1}+x_{2}+\dots +x_{n})} \\
&= \frac{P(X_{1}=x_{1}, X_{2}=x_{2},\dots, X_{n}=x_{n})}{\frac{1}{t!}\lambda^{t}e^{-n\lambda}} \\
&= \frac{P(X_{1}=x_{1}) P(X_{2}=x_{2})\dots P(X_{n}=x_{n})}{\frac{1}{t!}\lambda^{t}e^{-n\lambda}} \\
&=\frac{\frac{1}{x_{1}!}\lambda^{x_{1}}e^{-\lambda} \cdot \frac{1}{x_{2}!}\lambda^{x_{2}}e^{-\lambda}\dots \cdot \frac{1}{x_{n}!}\lambda^{x_{n}}e^{-\lambda}}{\frac{1}{t!}\lambda^{t}e^{-n\lambda}} \\
&= \frac{\frac{1}{x_{1}!x_{2}!\dots x_{n}!}\lambda^{\sum_{i=1}^n x_{i}}e^{-n\lambda}}{\frac{1}{t!}\lambda^{t}e^{-n\lambda}} \\
&=\frac{\frac{1}{x_{1}!x_{2}!\dots x_{n}!}\lambda^{t}e^{-n\lambda}}{\frac{1}{t!}\lambda^te^{-n \lambda  }} \\
&= \frac{t!}{x_{1}!x_{2}!\dots x_{n}!} \\
&= \begin{pmatrix}
 t  \\
x_{1},x_{2},\dots, x_{n}
\end{pmatrix}
\end{align}
$$

b.) Show that $X_{1}$ is not sufficient 
$$
\begin{align}
P(X_{2}=x_{2}|X_{1}=x_{1}) = \frac{P(X_{1}=x_{1})P(X_{2}=x_{2})}{P(X_{1}=x_{1})}=P(X_{2}=x_{2}) = \frac{e^{-\lambda}\lambda^{x_{2}}}{x_{2}!}
\end{align}
$$
Knowing $X_{1}$ is independent, the conditional distribution of the rest of the samples given $X_{1}$ retains $\lambda$, making it insufficient 

c.) Use factorization theorem to show that $T$ is sufficient. Identify a function $g$ and $h$ of that theorem
$$
\begin{align}
\text{PMF: } f(x) &= \frac{1}{x!}\lambda^{x}e^{-\lambda} \\
f(x_{1},x_{2},\dots x_{n}|\lambda) &= \prod_{i=1}^n \frac{1}{x_{i}}\lambda^{x_{i}}e^{-\lambda} \\
&=\lambda^{\sum x_{i}}e^{-n\lambda} \prod_{i=1}^n \frac{1}{x_{i}!} \\
g(T, \lambda)&=\lambda^te^{-n\lambda} \\
h(x_{1},x_{2},\dots, x_{n}) &= \prod_{i=1}^n \frac{1}{x_{i}!}
\end{align}
$$
### Problem 3

Let $X_{1}, X_{2},\dots X_{n}$ be an i.i.d sample from a distribution with the density function
$$
f(x|\theta) = \frac{\theta}{(1+x)^{\theta+1}},\, 0<\theta<\infty \text{ and } 0 \leq x< \infty
$$
Find a sufficient statistic for $\theta$

$$
\begin{align}
f(x_{i}|\theta) &= \prod_{i=1}^n \frac{\theta}{(1+x_{i})^{1+\theta}} \\
&= \frac{\theta}{(1+x_{1})^{\theta+1}} \cdot \frac{\theta}{(1+x_{2})^{\theta+1}}\cdot\dots \cdot \frac{\theta}{(1+x_{n})^{\theta+1}} \\
&= \frac{\theta^n}{\prod_{i=1}^n(1+x_{i})^{\theta +1}} \\
&=\frac{\theta^n}{\prod_{i=1}^n (1+x_{i})^{\theta} \cdot \prod_{i=1}^n(1+x_{i})} \\
&=\frac{\theta^n}{\exp\left( \theta\sum_{i=1}^n \ln(1+x_{i})\right)} \cdot \frac{1}{\prod_{i=1}^n (1+x_{i})} \\
T&=  \sum_{i=1}^n \ln(1+x_{i})\ \\
h&= \frac{1}{\prod_{i=1}^n (1+x_{i})}  \\
g(T,\theta) &= \theta^n \exp\left( -\theta \sum_{i=1}^n \ln(1+x_{i}) \right)
\end{align}
$$

### Problem 4:

Find a sufficient statistic for the Rayleigh density:
$$
f(x|\theta) = \frac{x}{\theta^2}\exp\left( -\frac{x^2}{2\theta^2} \right), \, x \geq 0
$$
$$
\begin{align}
f(x|\theta) &= \prod_{i=1}^n \frac{x_{i}}{\theta^2}\exp\left( \frac{-x_{i}^2}{2\theta^2} \right) \\
&= \frac{1}{\theta^{2n}}\exp\left( -\frac{1}{2\theta^2}\sum_{i=1}^n x_{i}^2\right)\cdot \prod_{i=1}^n x_{i} \\
T&=\sum_{i=1}^nx_{i}^2 \\
g(T,\theta) &= \frac{1}{\theta^{2n}}\exp\left( \frac{-T}{2\theta^2} \right) \\
h&= \prod_{i=1}^n x_{i}
\end{align}
$$



