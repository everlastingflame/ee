[[Statistical Methods]]
What is a parameter: A fixed unknown numerical value that describes the characteristic of an entire population, usually the $\mu$ or $\sigma$. For example, the two previous parameters can estimate the normal distribution. For the Poisson distribution, this is usually $\lambda$

What's the difference between a parameter and a statistic:
The parameter of a population is a characteristic. A statistic is a measure of a sample, or sample statistic (sample mean). Parameters are calculated for all individuals in the population (unique) and statistics are only for a sample (not unique)

The random variables $X_{1}, X_{2},\dots ,X_{n}$ form a simple random sample of size $n$ if 
1.) The $X_{i}'s$ are independent
2.) Every $X_{i}$ has the same probability distribution 

What is a random variable? The numerical description of the outcome from a statistical experiment or random process. 

Population parameters can be described with the variable $\theta$ . Depending on the context, $\theta$ denotes $\mu$, $\sigma$, or $\lambda$ as an example. 

A point estimate is a single numerical value that can be regarded as the true value of the parameter $\theta$
Example: The true value of $\theta$ is 2, however from sample data collected from a sample, we can only get an estimate, where we find that the point estimate $\hat{\theta} \approx 2.1$.

Example 2:
We denote the population proportion with $p$. We draw a sample from a population, and then we calculate the sample proportion $\hat{p} = \frac{X}{n}$. 

Unbiased estimators: A point estimator $\hat{\theta}$ is an unbiased estimator of $\theta$ if $E(\hat{\theta})=\theta$ for every value of $\theta$. If there is a difference between the point estimator and the parameter, then the bias can be found through $E(\hat{\theta}) - \theta$

$\tilde{X}$ is notation for the median. 

The MVUE is the minimum variance unbiased estimator of $\theta$, the notation for  this is known as $\bar{X}$
The standard error of an estimator is $\sigma_{\hat{\theta}} = \sqrt{\text{Var}(\hat{\theta})}$

Example of a standard error:
(after class)

Bootstrap:
A way to guess the parameter $\theta$, known as a bootstrap estimate $\hat{\theta}$

First bootstrap sample= $x_{1}^*,x_{2}^*,\dots,x_{n}^*$ = $\theta_{1}^*$
Second bootstrap sample =$x_{1}^*,x_{2}^*,\dots,x_{n}^*$ = $\theta_{2}^*$
...
Bth bootstrap sample = $x_{1}^*,x_{2}^*,\dots,x_{n}^*$= $\hat{\theta_{B}^*}$

$$
s_{\hat{\theta}} = \sqrt{\frac{1}{B-1} \sum(\hat{\theta_{i}^*}- \bar{\theta}^*)^2 }
$$

Method: Draw a sample from a population, then use this sample data to estimate what $\theta$ is. 


### Method of Moments

If $X$ is a RV from a pmf or pdf, and $k=1,2,3,\dots ,$ then the population moment or the $k^{\text{th}}$ moment of the distribution $f(x)$ or $k^{\text{th}}$ moment of the probability is $E(X^k)$

the $k^{\text{th}}$ population moment is:
$$
\frac{1}{n} \sum_{i=1}^n X_{i}^k
$$

The method of moments estimators (MME) $\hat{\theta_{1}},\dots \hat{\theta}_{m}$ are obtained by equating the first $m$ sample moments to the corresponding first $m$ population moments and solving for $\theta_{1}, \dots \theta_{m}$
$$
\begin{align}
E(X) =\frac{1}{n} \sum_{i=1}^n X_{i}^k \\
E(X^2) =\frac{1}{n} \sum_{i=1}^n X_{i}^2 \\
E(X^3) =\frac{1}{n} \sum_{i=1}^n X_{i}^3 \\
\dots \\
E(X^m) =\frac{1}{n} \sum_{i=1}^n X_{i}^m
\end{align}
$$
Example 1, Find the MME for the poisson distribution with parameter $\lambda$
We have a random sample $x_{1},x_{2},\dots, x_{n}$ that is i.i.d from a poisson distribution with parameter $\lambda$ 

(1)
$$
\begin{align}
&E(X) = \frac{1}{n}(x_{1}+x_{2}+\dots+x_{n}) \\
&E(X) = \lambda  \\
&\lambda = \frac{1}{n}(x_{1}+x_{2}+\dots+x_{n}) \\
&\lambda = \bar{X}
\end{align}
$$
$\hat{\lambda}_{MME} = \bar{X}$

Application:
Dataset = ${5,3,1,4,3,2,5,6,4,1}$
$x_{1} = 5, x_{2} = 3\dots$

$\hat{\lambda}_{MME} = \bar{X} = \frac{x_{1}+\dots +x_{n}}{n}$


Example 3: Find the MME for for the normal distribution with parameters $u$ and $\sigma$.

Both $\sigma$ and $\mu$ are unknown 

$$
\begin{align}

E(X) = \frac{1}{n}(x_{1}+\dots+x_{n}) = \bar{X} \\
E(X) = \mu  \\
\mu = \bar{X} \\
\hat{\mu}_{MME} = \bar{X} \\
E(X^2) = \frac{1}{n}(x_{1}^2+x_{2}^2+\dots+X_{n}^2) \\
xE(x^2) = Var(X) + \mu^2 = \sigma^2 + \mu^2 \\
\sigma^2 + \mu^2 = \frac{1}{n}(x_{1}^2+ x_{2}^2+\dots x_{n}^2) \\
\sigma^2 + \bar{x}^2 = \frac{1}{n}(x_{1}^2+ x_{2}^2+\dots x_{n}^2) \\
\sigma^2 = \frac{1}{n}(x_{1}^2+ x_{2}^2+\dots x_{n}^2)-\bar{x}^2 \\
\sigma = \sqrt{\frac{1}{n}(x_{1}^2+ x_{2}^2+\dots x_{n}^2)-\bar{x}^2} = \bar{\sigma}_{MME}
\end{align}
$$

Example 4: We know the probability of tossing a coin is $p$, the coin is tossed twice and the number of heads, $Y$ is observed. Three independent observations of $Y$ are made: $y_{1} =1, y_{2} =2, y_{3} = 3$. Find the method of moment estimate of $p$

y = # of heads

Use the data to estimate the probability $p$ of getting heads

$$
\begin{align}
Y_{1},Y_{2}, Y_{3} \, \text{ are i.i.d}, p \text{ is unknown} \\
E(y) = \frac{1}{n}(y_{1}+y_{2}+y_{3}) \\
y = \text{number of heads}, \, 0,1,2 \\
P(y=0) = (1-p):(1-p) = (1-p)^2 \\
P(y=1) = 2p(1-p) \\
p(y=2) = p^2 \\
E(y) = 0\cdot (1-p)^2 + 1\cdot 2p(1-p)^2 + 2p^2 = 2p \\
2p = \frac{1}{3}(y_{1}+y_{2}+y_{3}) \\
\bar{P}_{MME} = \frac{1}{6}(y_{1}+y_{2}+y_{3}) \\
\bar{P}_{MME} = \frac{1}{6}(1+2+3)=0.833
\end{align}
$$

Find the MME for the exponential distribution with parameter $\lambda$

$$
\begin{align}
E(X) = \frac{1}{n}\sum_{i=1}^nX_{i}^k \\
E(X) = \frac{1}{\lambda} \\
\frac{1}{\lambda} = \frac{1}{n}\sum_{i=1}^nX_{i}^k \\
\hat{\lambda}_{MME} = \frac{n}{\sum_{i=1}^nX_{i}^k} 
\end{align}
$$


### Maximum Likelihood Estimation

A likelihood function has random variables $X_{1},X_{2},\dots , X_{n}$ and have a joint pmf or pdf $f(x_{1},x_{2}, \dots ,x_{n}; \theta_{1},\theta_{2}, \dots \theta_{n})$. The parameters $\theta$ have unknown values. When the variables $x_{1},x_{2}, \dots x_{n}$ are observed sample values, and $f$ is regarded as a function of the parameters, then it is called the likelihood function

If we let $X_{1},X_{2},\dots ,X_{n}$ is sampled from a continuous distribution with a pdf $f(x; \theta_{1},\theta_{2},\dots \theta_{m})$ with parameters $\theta$ unknown, then the likelihood function is:
$$
\begin{align}
L(\theta_{1},\dots \theta_{m}) = f(x_{1},\dots,x_{n};\theta_{1},\dots \theta_{m}) \\
=f(x_{1};\theta_{1},\theta_{2},\dots,\theta_{m})f(x_{2};;\theta_{1},\theta_{2},\dots,\theta_{m}) \\
= \prod_{i=1}^n  f(x_{i};\theta_{1}, \theta_{2}, \dots,\theta_{n})
\end{align}
$$
The maximum likelihood estimates are the values of $\theta_{i}$ that maximize the likelihood function:
$f(x_{1},..x_{n};\hat{\theta}_{1},\dots,\hat{\theta_{n}}) \geq$


Example 5: $x_{1},\dots ,x_{n}$ are all i.i.d and follow the poisson distribution with parameter $\lambda$ unknown

$$
\begin{align}
\text{Step 1.) Write out the likelihood function} \\
L(\lambda) = P(X_{1}=x_{2})\cdot P(X_{2}=x_{2})\cdot\dots P(X_{n}=x_{n}) \\
P(X=x) = \frac{\lambda^xe^\lambda}{x!} \\
L(\lambda) = \frac{\lambda^{x_{1}}e^{-\lambda}}{x_{1}!} \cdot \frac{\lambda^{x_{2}}e^{-\lambda}}{x_{2}!}\dots \\
L(\lambda) = \frac{\lambda^{x_{1}+x_{2}+\dots+x_{n}}e^{-\lambda^n}}{x_{1}!x_{2}!\dots x_{n}!} \\
\text{Step 2.) We maximize the likelihood function} \\
\text{Max } L(\lambda) = L'(\lambda)=0 \\
\text{Use log-likelihood function} \\
l(\lambda) = \ln (L(\lambda)) \\
l(\lambda) =  \ln\left(  \frac{\lambda^{x_{1}+x_{2}+\dots+x_{n}}e^{-n\lambda}}{x_{1}!x_{2}!\dots x_{n}!} \right) \\
=(x_{1}+x_{2}+\dots +x_{n})\log(\lambda) + (-\lambda)\log(e)-\log(x_{1}!x_{2}!\dots x_{n}!) \\
l(\lambda) = \sum_{i=1}^nx_{i} \log(\lambda) - n\lambda -\log(x_{1}!x_{2}!\dots x_{n}!) \\
l'(\lambda) = \sum_{i=1}^nx_{i} \cdot \frac{1}{\lambda}-n=0 \\
\lambda = \frac{\sum_{i=1}^nx_{i}}{n} \\
\hat{\lambda}_{MLE} = \frac{\sum_{i=1}^nX_{i}}{n} = \bar{X}
\end{align}
$$

Example 6: find MLE of normal distribution
$$
\begin{align}
L(\mu, \sigma) = f(x_{1};\mu,\sigma)\cdot f(x_{2};\mu,\sigma) \cdot f(x_{n};\mu,\sigma) \\
= \frac{1}{\sigma \sqrt{ 2\pi }}\exp\left( -\frac{(x_{1}-\mu)^2}{2\sigma^2} \right)\cdot\dots \\
= \prod_{i=1}^n \left(\frac{1}{\sigma \sqrt{ 2\pi }}\exp\left( -\frac{(x_{n}-\mu)^2}{2\sigma^2} \right)\right) \\
= \left( \frac{1}{\sigma \sqrt{ 2\pi }} \right)^n \cdot \exp\left( -\frac{(x_{1}-\mu)^2}{2\sigma^2} -\dots-\frac{(x_{1}-\mu)^2}{2\sigma^2}\right) \\
l(\mu,\sigma) = \log L(\mu,\sigma) = \log\left( \frac{1}{\sigma \sqrt{ 2\pi }} \right)+ \frac{1}{2\sigma^2} \sum_{i=1}^n (x_{i}-\mu)^2 \\
\text{Maximizing the parameters} \\
\frac{\partial l}{\partial \mu} = -\frac{1}{2\sigma^2} \sum_{i=1}^n [-2(x_{i}-\mu)] = \frac{\sum x_{i} - n \mu }{\sigma^2} \\
\sum x_{i} - n\mu = 0,  \\
\hat{\mu}_{MLE} = \frac{\sum  X_{i}}{n} \\
\frac{\partial l}{\partial \sigma} =\text{ okay now solve it idgaf}
\end{align}
$$
