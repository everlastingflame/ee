[[Statistical Methods]]
I pledge my honor that I have abided by the stevens honor system
Charles Booth
### Problem 1
Suppose that 100 items are sampled from a manufacturing process and 3 are found to be defective. A beta prior is used for the unknown proportion $\theta$ of defective items. Consider two cases
$$
\begin{align}
&\text{(1) } a = b = 1 \\
&\text{(2) } a = 0.5, \, b = 5 
\end{align}
$$
$$
\begin{align}
\text{Prior pdf : } f(\theta; \alpha,\beta) &= \frac{1}{B(\alpha,\beta)}\theta^{\alpha-1}(1-\theta)^{\beta-1} \\
\text{likelihood function: } f(x=3|\theta) &= \begin{pmatrix}100 \\ 3\end{pmatrix}\theta^{3}(1-\theta)^{97} \\
\text{Posterior function} &\propto \theta^{\alpha-1}(1-\theta)^{\beta-1}\cdot \theta^{3}(1-\theta)^{97} \\
&\propto \theta^{\alpha + 3 -1}(1-\theta)^{\beta+97-1} \\
&\propto \text{Beta}(\alpha+3, \beta+97)\\
\text{Posterior, } \alpha=\beta =1 &= \text{Beta}(4, 98) \\
\text{Posterior, } \alpha= 0.5, \beta = 5 &= \text{Beta}(3.5, 102) \\
\text{Posterior mean, } \alpha=1, \beta = 1 &= \frac{4}{98} \approx 0.0408163265 \\
\text{Posterior mean, } \alpha=0.5, \beta = 5 &= \frac{3.5}{102} \approx 0.0343137255
\end{align}
$$
The posterior mean for case 1 is greater than that of case 2, which makes sense considering the density of the distributions below are contained around those values.

Plot the two posterior distributions and compare them
(1)
![[Pasted image 20260210143643.png]]
(2)
![[Pasted image 20260210143716.png]]
The density for the second condition is a bit tighter than the first condition. 


### Problem 2

Let the unknown probability that a basketball player makes a shot successfully be 𝜃.
Suppose your prior on 𝜃 is uniform on $[0, 1]$ and that she then makes two shots
successfully in a row. Assume that the outcomes of the two shots are independent.

a) What is the posterior density of 𝜃?

$$
\begin{align} 
\text{Prior: } f(\theta) &= 1 \text{ if } 0 \leq \theta \leq 1, \text{0 otherwise}\\
\text{Likelihood: } L(\theta) &= \theta^2(1-\theta) \\
\text{Posterior function: } f(\theta | x) &\propto\theta^2(1-\theta) \text{ if } 0\leq \theta \leq 1 \\
\text{Posterior density} &= \frac{\theta^2(1-\theta)}{\int_{0}^1\theta^2(1-\theta) \, d\theta} \\
\int_{0}^1\theta^2(1-\theta) \,d\theta &= \frac{1}{12} \\
&=12\theta^2(1-\theta), \, 0\leq\theta\leq 1
\end{align}
$$
b) What would you estimate the probability that she makes a third shot successfully
to be?
$$
\begin{align}
P(3|2) &= \theta \cdot f(\theta| \text{Data}) \\
&=\int_{0}^1 12\theta^3(1-\theta) = \frac{3}{5}
\end{align}
$$

### Problem 3
Suppose that $X$ is a discrete random variable with
$$\begin{align}
P(X=0) &= \frac{2}{3}\theta \\
P(X=1) &= \frac{1}{3}\theta \\
P(X=2) &= \frac{2}{3}(1-\theta) \\
P(X=3) &= \frac{1}{3}(1-\theta)
\end{align}
$$
where $0 \leq \theta \leq 1$ is a parameter. The following 10 independent observations were taken from such a distribution: $(3, 0, 2, 1, 3, 2, 1, 0, 2, 1)$

a.) Find the MME of $\theta$
$$
\begin{align}
E(X) &= \frac{1}{n} \sum_{i=1}^n x_{i} \\
E(X) &= 0 \cdot\frac{2}{3}\theta + 1\cdot \frac{1}{3}\theta + 2 \cdot \frac{2}{3} (1-\theta) +3 \cdot \frac{1}{3}(1-\theta) \\
&=\frac{1}{3}\theta + \frac{7}{3}(1-\theta) \\
&=-2\theta +\frac{7}{3}\\
\frac{7}{3} -2\theta &= \bar{x} \\
\frac{7}{3} -2\theta&= \frac{15}{10} \\
2\theta &= \frac{5}{6} \\
\hat{\theta}_{\text{MME}} &= \frac{5}{12}
\end{align}
$$
b.) Find the MLE of $\theta$
$$
\begin{align}
L(\theta) &= \left( \frac{2}{3}\theta \right)^2\cdot\left( \frac{1}{3}\theta \right)^3\cdot\left( \frac{2}{3}(1-\theta) \right)^3\cdot \left( \frac{1}{3}(1-\theta) \right)^2 \\
&=\frac{32}{3^{10}}\theta^5(1-\theta)^5 \\
l(\theta) &= \ln\left( \frac{32}{3^{10}} \right)+5\ln(\theta)+5\ln(1-\theta) \\
l'(\theta) &= \frac{5}{\theta} - \frac{5}{1-\theta} \\
\frac{5}{\theta}&=\frac{5}{1-\theta} \\
5(\theta-1) &= 5\theta \\
10\theta  &=5 \\
\hat{\theta}_{MLE} &= \frac{1}{2}
\end{align}
$$
c.) If the prior distribution  of $\theta$ is uniform on $[0,1]$, what is the posterior density function? 
$$
f(\theta|x_{1},x_{2},\dots, x_{3}) = \theta^5(1-\theta)^5, \text{ for } 0\leq \theta\leq 1 
$$

d.) Find the Bayes Posterior Mean Estimate, the MAP estimate, the Posterior
Median Estimate, and a 90% Bayesian Confidence Interval for the parameter $\theta$.
**Baye's Posterior Mean Estimate:**
$$
\begin{align}  \\
\theta^5(1-\theta)^5 &= \text{Beta}(6,6) \\
E[\theta|x_{1},x_{2}\dots] &= \frac{6}{12} = \frac{1}{2}
\end{align}
$$
**MAP estimate**
$$
\begin{align}
f(\theta|x_{1},x_{2},\dots, x_{3}) &= \theta^5(1-\theta)^5 \\
f'(\theta | x_{1}, x_{2},\dots) &= 5\theta^4(1-\theta)^5+5\theta^5(1-\theta)^4(-1) \\
&= 5(\theta^4(1-\theta)^4(1-2\theta)) \\
&=\theta^4(1-\theta)^4(1-2\theta) = 0 \\
&=1-2\theta =0, \,\hat{\theta}_{\text{MAP}} = \frac{1}{2}
\end{align}
$$
**Posterior Median Estimate**
Since our Posterior function is just $\text{Beta}(6,6)$, the median will  be $\frac{1}{2}$

**90% Bayesian Confidence Interval**

I used R to find this. 
```
> qbeta(0.05, 6, 6)  
[1] 0.2712499
> qbeta(0.95, 6, 6)  
[1] 0.7287501
```

So our confidence interval would be $[0.2712499, 0.7287501]$

### Problem 4

Suppose that $Y$ follows a binomial distribution with parameters $n$ and $p$ so that pmf of $Y$ given $\theta$ is:
$$
g(y|\theta) = C(y,n)\theta^{y}(1-\theta)^{n-y}
$$
for $y = 0,1, \dots, n$,. Suppose that the prior pdf of the parameter $\theta$ is the Beta pdf, that is 
$$
h(\theta) = \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}\theta^{\alpha-1}(1-\theta)^{\beta -1}
$$
for $0< \theta<1$
**Find the posterior pdf of $\theta$ given that Y=y**

$$
\begin{align}
\text{Prior PDF: } h(\theta) &= \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}\theta^{\alpha-1}(1-\theta)^{\beta -1} \\
\text{Likelihood function: } L(\theta) &= \prod_{i=1}^n \begin{pmatrix}y  \\n\end{pmatrix}\theta^{y_{i}}(1-\theta)^{n-y_{i}} \\
&= \theta^{\sum_{i=1}^n y_{i}} (1-\theta)^{n^2-\sum_{i=1}^n y_{i}} \\
f(\theta|y_{1},y_{2},\dots,y_{n}) &\propto \theta^{\alpha -1}(1-\theta)^{\beta-1}\cdot\theta^{\sum_{i=1}^n y_{i}} (1-\theta)^{n^2-\sum_{i=1}^n y_{i}}  \\
&\propto \theta^{\alpha+\sum_{i=1}^n y_{i}-1}(1-\theta)^{\beta+n^2-\sum_{i=1}^ny_{i}-1} \\
&\propto \text{Beta}\left( \alpha + \sum_{i=1}^ny_{i}-1, \beta + n^2-\sum_{i=1}^n y_{i} -1\right)
\end{align}
$$
### Problem 5
A traffic control engineer believes that the cars passing through a particular intersection
arrive at a mean rate equal to either 3 or 5 for a given time interval. Prior to collecting
any data, the engineer believes that it is much more likely that the rate $\lambda = 3$ than $\lambda =5$. In fact, the engineer believes that the prior probabilities are: $P(\lambda = 3) = 0.7, \, P(\lambda = 5) = 0.3$. One day, during a randomly selected time interval, the engineer observes $x = 7$ cars pass through the intersection. In light of the engineer's observation, what is the probability $\lambda =3$? What is the probability that $\lambda =5$


$$
\begin{align}
 f(x | \lambda) &= \frac{\lambda^xe^{-\lambda}}{x!} \\
P(x=7 | \lambda = 3) & = \frac{3^7e^{-3}}{7!} \approx 0.021604031\\
P(x=7 | \lambda = 5) &= \frac{5^7e^{-5}}{7!} \approx 0.104444863\\
P(X=7) &= P(X=7 | \lambda = 3) \cdot P(\lambda=3) + P(X=7 | \lambda = 5)\cdot P(\lambda=5) \approx 0.046456 \\
&\text{Probability } \lambda = 3 \\
P(\lambda = 3 | X=7) &= \frac{P(x=7|\lambda=3)P(\lambda=3)}{P(x=7)} \approx 0.32552803889 \\&\text{Probability } \lambda = 5\\
P(\lambda = 5 | X=7) &= \frac{P(x=7|\lambda=5)P(\lambda=5)}{P(x=7)} \approx 0.67447196111
\end{align}
$$




