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
E(x^2) = Var(X) + \mu^2 = \sigma^2 + \mu^2 \\
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

### Confidence Intervals from MLEs

Fisher information for $\theta$ for a random sample $x_{1},x_{2}\dots x_{n}$ is defined as:
$$
l(\theta) = -E\left(  \frac{\partial^2}{\partial \theta^2} l(\theta) \right)
$$

The second order derivative depends on one of the random variables, $x_{1},x_{2}\dots x_{n}$
You treat the parameter $\theta$ as a constant in the second order derivative, making the entire expression in terms of the random variables. 
Measures the amount of information that the random variables contain with regard to the parameter

MLEs can help find a confidence interval for the parameter $\theta$ The interval $(1-\alpha)100 \%$ is given by 
$$
\hat{\theta}_{\text{MLE}} = \pm \frac{z_{\frac{\alpha}{2}}}{\sqrt{ I_{n}(\hat{\theta}_{\text{MLE}}) }}
$$
Example: find the confidence interval for a parameter $\lambda$ for the Poisson distribution

$$
\begin{align}
x_{1},x_{2}\dots x_{n}, \, \text{i.i.d, follow poisson dis} \, P(\lambda), \text{CI} = (1-\alpha) \\
\hat{\lambda}_{\text{MLE}} =\bar{X} \\
\text{I}_{n}(\lambda) = -E\left( \frac{\partial^2}{\partial \theta^2}l(\lambda) \right) \\
L(\lambda) = \prod_{i=1}^n \frac{\lambda^{x_{i}}e^{-\lambda}}{x_{i}!} \\
L(\lambda) = \frac{\lambda^{x_{1}+x_{2}+\dots+x_{n}}(e^{-\lambda})^n}{x_{1!}x_{2!}+\dots+x_{n}!} \\
l(\lambda) = (x_1 +x_{2} +\dots)\ln \lambda - \lambda n - \ln(x_{1}!x_{2}!\dots) \\
\frac{\partial l}{\partial \lambda} = \sum_{i=1}^n x_{i} \cdot \frac{1}{\lambda} - n \\
\frac{\partial^2l}{\partial \lambda^2} = \sum_{i=1}^n x_{i} \cdot \left( -\frac{1}{\lambda^2} \right) = -\frac{\sum_{i=1}^n x_{i}}{\lambda^2} \\
E \left(-\frac{\sum_{i=1}^n x_{i}}{\lambda^2}\right) = E\left(  -\frac{x_{1}}{\lambda^2} - \frac{x_{2}}{\lambda^2} -\dots \right) \\
=E\left( -\frac{X_{1}}{\lambda^2} \right) + E\left( -\frac{X_{2}}{\lambda^2} \right) + \dots \\
=-\frac{1}{\lambda^2} E(X_{1})-\frac{1}{\lambda^2}E(X_{2}) \\
E\left( -\sum_{i=1}^n x_{i} \cdot \frac{1}{\lambda_{2}} \right) = -\frac{1}{\lambda^2} \cdot \lambda \cdot n = -\frac{n}{\lambda} \\
I_{n}(\lambda) = -E\left( \frac{\partial^2l}{\partial l^2} \right) = -\left( -\frac{n}{\lambda} \right) = \frac{n}{\lambda} \\
(1-\alpha)100\% = \bar{x}_{\text{MLE}} \pm \frac{z_{\frac{\alpha}{2}}}{\sqrt{ I_{n}(\hat{\theta}_{\text{MLE}}) }} \\
\bar{x} \pm \frac{z_{\frac{\alpha}{2}}}{\sqrt{ \frac{m}{\bar{x}} }} \\
\bar{x} \pm \text{didnt finish}
\end{align}
$$

Example 10: given a random sample $X_{1}\dots X_{36}$ with sample mean of 10. Assume they follow exp dis with param $\lambda$. Construct a conf interval with $95 \%$

$$
\begin{align} \\
\bar{x} =10, \, 95\% \text{ CI, } \alpha=5 \\
\hat{\lambda}_{\text{MLE}} \pm \frac{z_{\frac{\alpha}{2}}}{\sqrt{ I_{n}(\hat{\lambda}_{\text{MLE}}) }} \\
\alpha = 0.05 =\frac{\alpha}{2} = 0.025 \\
z_{\frac{\alpha}{2}} = 1.96, \text{ z table calc} \\
\hat{\lambda}_{\text{MLE}} = \frac{1}{\bar{x}} = \frac{1}{10} =0.1 \\
I_{n}(\lambda) -E\left( \frac{\partial^2l}{\partial \lambda^2} \right) \\
L_{\lambda} = \prod_{i=1}^{36} \lambda e^{-\lambda x_{i}} \\
L_{\lambda} = \lambda^{36}e^{-\lambda x_{1}-\lambda x_{2}-\dots} \\
L_{\lambda} = \lambda^{36} \exp\left( -\lambda \sum_{i=1}^{36}x_{i} \right) \\
l(\lambda) = 36 \ln(\lambda) + \left( -\lambda \sum_{i=1}^{36}x_{i} \right) \\
\frac{\partial l}{\partial \lambda} = \frac{36}{\lambda} - \sum_{i=1}^{36}x_{i} \\
\frac{\partial^2 l}{\partial \lambda^2} = -\frac{36}{\lambda^2} \\
=E\left( -\frac{36}{\lambda^2} \right) \\
I_{\lambda} = \frac{36}{\lambda^2} \\
I_{n}(\hat{\lambda}_{\text{MLE}}) = \frac{36}{0.1^2} = 3600 \\
\text{95\% CI :} \, \left( 0.1 \pm \frac{1.96}{\sqrt{ 3600 }} \right) =(0.0677, 0.133)
\end{align} 
$$
We are 95% confident that $\lambda$ is between these two values.
### Baye's Rule
$$
P(A|B) = \frac{P(B|A)P(A)}{P(B)}
$$
For random variables $X$ and $Y$
$$
f_{X|Y}(x|y) = \frac{f_{Y|X}(y|x)f_{X}(X)}{f_{Y}(Y)}
$$

MME/MLE -> $\theta$ exists already, but unknown, so we collect data to make a better guess about the true value of $\theta$ 

Bayesian method -> $\theta$ varies, $\theta$ is a r.v. The pdf of the prior function is updated when we see new data, allowing us to find an updated pdf and create what's called the posterior function. 

### Bayesian Estimators

To estimate the parameter, we can use the function:
$$
pdf(\theta|X_{1},\dots ,X_{n}) = \frac{pdf(X_{1},\dots,X_{n}|\theta)pdf(\theta)}{pdf(X_{1},\dots X_{n})}
$$

The prior is $pdf(\theta)$, the posterior is $pdf(\theta | X_{1},\dots ,X_{n})$, the likelihood function is $pdf(X_{1},\dots X_{N}|\theta)$, the joint pdf is $pdf(X_{1},\dots, X_{n})$

We can find that the posterior function is proportional to the product:
$$
f(\theta |X_{1},\dots,X_{n})\propto f(X_{1},\dots ,X_{n}|\theta)\cdot f(\theta)
$$

Example: Let $X_{1}, X_{2},\dots, X_{n}$ be a random sample from the Bernoulli distribution with parameter $p$ 
a.) Choose the prior function for $p$, and then find the posterior function of $p$ given the data

$$
\begin{align}
\text{Prior distribution : Choose }  \text{Beta}(\alpha,\beta) \text{ for parameter } p \\
\text{Prior pdf : } f(p; \alpha,\beta) = \frac{1}{B(\alpha,\beta)}p^{\alpha-1}(1-p)^{\beta-1} \\
\text{Likelihood function : } f(x,p) = p^{x}(1-p)^{1-x}, \, x=0,1 \\
f(x_{1},\dots , x_{n}|p) = \prod_{i=1}^n (p^{x_{i}}(1-p)^{1-x_{i}}) = p^{x_{1}+x_{2}+\dots}(1-p)^{1-x_{1} +1-x_{2}-\dots} \\
= p^{\sum^n_{i=1} x_{i}}\cdot(1-p)^{n-\sum_{i=1}^nx_{i}} \\
\text{Posterior Function: } f(p |x_{1},x_{2},\dots) \propto L(p)\cdot f(p;\alpha,\beta) \\
= \alpha p^{\sum x_{i}}(1-p)^{n-\sum x_{i}} \cdot \frac{1}{B(\alpha,\beta)}\cdot p^{\alpha-1}(1-p)^{\beta -1} \text{ , we can remove constants} \\
=\alpha p^{\sum x_{i} + \alpha-1} \cdot(1-p)^{n-\sum x_{i} + \beta -1}, \text{ our posterior function} \\
\text{Posterior PDF : } \text{Beta} \left( \sum x_{i}+\alpha , n-\sum x_{i} +\beta \right) \\
\text{Prior PDF : } \text{Beta} (\alpha, \beta)
\end{align}
$$

Q: Why did we use the beta distribution in particular here?

b.)Assume $n = 100$, and $\sum_{i=1}^n X_{i} =30$. If the prior function is Beta(10,10), what is the posterior function?


$$
\begin{align}
&n = 100, \sum x_{i} = 100,  \\
&\text{Prior dist: } \text{Beta}(10,10) \\
&\text{Posterior dist: } \text{Beta}(30 + 10, 100-30+10) = \text{Beta}(40,80) \\

\end{align}
$$

Example: Assume that $x_{i}$ follows geom distribution. The prior distribution is Beta with parameters $\alpha, \beta$

$$
\begin{align}
\text{Prior pdf : } f(p; \alpha,\beta) = \frac{1}{B(\alpha,\beta)}p^{\alpha-1}(1-p)^{\beta - 1} \\
L(P) = \prod_{i=1}^n (p(1-p)^{x_{i}-1}) = p^n(1-p)^{(x_{1}-1)+(x_{2}-1)+\dots} \\
= p^n(1-p)^{\sum x_{i}-n} \\
f(p | x_{1},x_{2},\dots ,x_{n}) \propto p^n(1-p)^{\sum x_{i}-n} \cdot \frac{1}{B(\alpha,\beta)} p^{\alpha - 1}(1-p)^{\beta - 1} \\
f(p | x_{1,\dots ,x_{n}}) \propto p^{n+\alpha-1}(1-p)^{\sum x_{i}-n + \beta-1} \\
= \text{Beta}\left( n+\alpha, \sum x_{i} -n +\beta \right) \\

\end{align}
$$

Means of past distributions = Bayes Posterior Mean Estimator 

Mode of posterior distributions = Max a posterior (MAP) estimator 

Median of posterior distribution = Posterior Median Estimator 


Example: Suppose that $X$ is a discrete random variable with $P(X=1) = \theta$ and $P(X=2) = 1-\theta$. Three independent observations of $X$ are made: $x_{1} = 1, x_{2} = 2, x_{3} = 2$

a.) Write out and simplify the likelihood function
b.) Assume the prior distribution is uniform $[0,1]$

$$
\begin{align}
n&=1 \\
L(\theta) &= P(X=x_{1})\cdot P(X=x_{2})\cdot P(X=x_{3}) \\
&= P(X=1)\cdot P(X=2) \cdot P(X=2) \\
&= \theta \cdot (1-\theta)^2 \\
& \text{Prior:} \, \text{Uniform } [0,1]: 1 \text{ if } 0 \leq \theta \leq 1, 0 \text{ otherwise} \\
&\text{Posterior: } f(\theta; x_{1},x_{2},\dots x_{n}) \propto L(\theta) \cdot f(\theta) \\
&\propto \theta(1-\theta)^2 \\
&\text{Posterior is: } \text{Beta}(2,3) \\
\text{Bayes Posterior Mean Estimate: } &= \text{Mean of post dist} = \frac{2}{2+3} = 0.4 \\
E(X) &= \int_{-\infty}^\infty {x}\cdot f(x) \, dx \\
E(\theta) &= \int_{-\infty}^\infty \theta \cdot f(\theta | x_{1},\dots x_{n}) \, d\theta \\
f(\theta | x_{1},x_{2},x_{3}) &= c \cdot\theta(1-\theta)^2, 0\leq \theta\leq 1 \\
\int_{-\infty}^\infty f(\theta |x_{1},x_{2},x_{3}) \, d\theta
 &= 1 \\
c \cdot\int_{0}^1 \theta(1-\theta)^2 \, d\theta &= c\cdot\frac{1}{12} =1, c=12 \\
f(\theta | x_{1},x_{2},x_{3}) &= 12\theta(1-\theta)^2, 0\leq \theta\leq 1 \\
E(\theta) &= \int_{-\infty}^{\infty} f(\theta | x_{1},x_{2},x_{3}) \, d\theta = \int_{0}^1 12\theta^2(1-\theta)^2\, d\theta = 0.4 \\
E(\theta) &= 0.4,\, \hat{{\theta}} = 0.4,\, \theta \approx 0.4 \\
\text{MAP estimate } &: \text{ Mode of posterior dist to estimate } \theta \\
& \text{Find maximal point of the posterior function} \\
f(\theta | x_{1}, x_{2}, x_{3}) &= 12\theta(1-\theta)^2, \, 0 \leq \theta \leq 1 \\
f'(\theta | x_{1}, x_{2}, x_{3}) &= 12(1-\theta)^2 - 12\theta \cdot 2(1-\theta) = 0 \\
\theta &= \frac{1}{3}, \text{ maximum point} \\
\text{Posterior Median Estimate } &: \text{ We use median of post dist to est. } \theta \\
\int_{-\infty}^{x_{0}}&= 0.5 \\
\int_{-\infty}^{\theta_{0}} f(\theta ; x_{1},x_{2}\dots)\, d\theta &= \int_{0}^{\theta_{0}} 12\theta(1-\theta)^2
\end{align}
$$


Confidence intervals for the above problem:

$$
\begin{align}
\text{95\% CI for } \theta: \alpha = 5\% = 0.05 \\
\theta_{1} = 0.025, \theta_{2} = 0.025 \\
\int_{-\infty}^{\theta_{1}} f(\theta; x_{1},x_{2},\dots) \, d\theta = 0.025 \\
\int_{0}^{\theta_{1}} 12\theta(1-\theta)^2 = 0.0676 \\
\int_{0}^{\theta_{0}} 12\theta(1-\theta)^2 = 0.975 =0.8059
\end{align}
$$

### Sufficiency 


