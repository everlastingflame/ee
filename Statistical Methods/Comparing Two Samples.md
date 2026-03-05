[[Statistical Methods]]

Usually comparing two different population datasets, like population of two cities, wanting to figure out the distribution of ages between cities. 

(Review elementary hypothesis testing)

Usually follows the hypothesis testing method where we see if a parameter of one population is greater than another one (example)

Need to consider all the factors to test appropriately. Looking at the sample size, distribution, if the data is independent or dependent, or if the population STD is known or not. An appropriate test can be decided from this. If so, we collect data and perform tests, then making a conclusion

The following is a hypothesis test for a population mean, given a large sample. 

$$
\begin{align}
+ \text{ If } \sigma \text{ is known: } z=\frac{\bar{x}-\mu}{\left( \frac{\sigma}{\sqrt{n }} \right)} \\
+ \text{ If } \sigma \text{ is unknown: } z=\frac{\bar{x}-\mu}{\left( \frac{s}{\sqrt{n }} \right)}
\end{align}
$$
$\bar{x}$ is the sample mean, $\mu$ is the presumed value of the population mean from the null hypothesis, $\sigma$ is the population standard deviation, and $s$ is the sample standard deviation. The test statistic has the standard deviation

If we have a $H_{a} < \text{value}$, it is a left tailed test. The opposite is a right tailed test. If $H_{a} \neq \text{value}$, it is a two tailed test. For a left tailed test, we reject the null hypothesis $H_{0}$ if $z < -z_{a}$, reject for a right tailed test when $z \geq z_{\alpha}$, and for a two tailed test, we reject when $|z| \geq z_{\frac{\alpha}{2}}$. 

For p-values, a left tailed and right tailed test has $p = P(Z  \geq z)$, for a two tailed test, $p = P(|Z| \geq |z|)$. We can make the conclusions with p-values if $p \leq\alpha$ we reject the null hypothesis, if $p \geq \alpha$ we fail to reject the null hypothesis 

Example problems:


Problem 1.) 
A cosmetic company fills its best-selling 8-ounce jars of facial cream by an automatic dispensing machine. The machine is set to dispense a mean of 8.1 ounces per jar. Uncontrollable factors in the process can shift the mean away from 8.1 and cause either underfill or overfill, both of which are undesirable. In such a case the dispensing machine is stopped recalibrated. Regardless of the mean amount dispensed, the standard deviation of the amount dispensed always has value 0.22 ounce. A quality control engineer routinely select 30 jars from the assembly line to check the amount filled. On one occasion, the sample mean is 8.2 ounces. Determine if there is sufficient evidence in the sample to indicate, at the 1% level of significance, that the machine should be recalibrated.

$\mu=8.1$, $\bar{x} =8.2$
$$
\begin{align}
H_{0}: \mu=8.1 \to \text{works well} \\
H_{1}: \mu \neq 8.1 \to \text{DN ww}
\end{align}
$$
Population mean, n = 30 (large). We know the population standard deviation is always $\sigma = 0.22$

$$
z = \frac{8.2-8.1}{\frac{0.22}{\sqrt{ 30 }}} \approx_{2}.49
$$
$$
p = P(|Z| \geq 2.49) = P(Z\leq -2.49) = 2(0.0065) = 0.0128
$$
$$
\alpha = 0.01, p>\alpha, \text{ fail to reject } H_{0}, \to \text{Accept } H_{0}
$$

What if we have a small sample size? $(n <30)$

$$
\begin{align}
+ \text{ if } \sigma \text{ is known: } z= \frac{\bar{x}-\mu}{\left( \frac{\sigma}{\sqrt{n }} \right)} \\
+ \text{ if } \sigma \text{ is unknown } t= \frac{\bar{x}-\mu}{\frac{s}{\sqrt{ n }}}
\end{align}
$$
where t is the student's t distribution with n-1 degrees of freedom (please learn this)

Problem 3:
The price of a popular tennis racket at a national chain store is $179. Portia bought five of the same racket at an online auction site for the following prices (in $): 155 179 175 175 161

Assuming that the auction prices of rackets are normally distributed, determine whether there is sufficient evidence in the sample, at the 5% level of significance, to conclude that the average price of the racket is less than $179 if purchased at an online auction. Assume that the standard deviation of prices for rackets purchased at an online auction is $10.

Problem 4:
A locally owned, independent department store has chosen its marketing strategies for many years under the assumption that the mean amount spent by each shopper in the store is no more than $100.00. A newly hired store manager claims that the current mean is higher and wants to change the markeXng scheme accordingly. A group of 27 shoppers is chosen at random and found to have spent a mean of $104.93 with a standard deviation of $9.07. Assume that the population distribution of amounts spent is approximately normal, and test the store manager’s claim at the 0.05 level of significance.

$n=27 \to \text{small}$, $H_{0} : \mu \leq 100, H_{1}> 100$

Hypothesis test for a population variance
$$
\chi^2 = \frac{(n-1)s^2}{\sigma^2}
$$

Problem 6.

A manufacturer of golf balls requires that the weights of its golf balls have a standard deviation that does not exceed 0.08 ounces. One of the quality control inspectors says that the machines need to be recalibrated because he believes the standard deviation of the weights of the golf balls is more than 0.08 ounces. To test the machines, he selects a simple random sample of 30 golf balls off the assembly line and finds that they have a mean weights of 1.6200 ounces and a standard deviation of 0.0804 ounces. Does this evidence support the need to recalibrate the machines, at the 0.05 level of significance? Assume that the weights of the golf balls are normally distributed.

$n=30$, $\bar{x}=1.6200$, $\alpha = 0.05$ 

$$
\begin{align}

H_{0}: \sigma^2 \leq (0.08)^2 \\
H_{1}: \sigma^2 >(0.08^2)
\end{align}
$$
hint $\to$ chi squared test


Non-parametric tests for comparing two samples: Mann-Whitney test (rank sum test), and the wilcoxon signed test. 

$$
\begin{align}
H_{0} : \mu \leq \mu_{2} \\
H_{1}: \mu_{0} > \mu_{2} \\
= \\
H_{0}: \mu_{1}-\mu_{2} \leq 0 \\
H_{1}: \mu_{1} - \mu_{2} > 0 \\
\end{align}
$$

If the two populations are normally distributed, we can perform a parametric method. If not, we perform a non-parametric method.

Parametric methods:
population mean
population porportion
...
population variance 


Non-parametric methods:
Rank sum test (comparing two samples) (Mann-Whitney test) (for indpt data)
Signed rank test (used for dpt data)

(review the examples in the slides)

Hypothesis test for two population means - independent samples $\sigma(s)$ known

$$
z = \frac{(\bar{x}_{1}-\bar{x}_{2})-(\mu_{1}-\mu_{2})}{\sqrt{ \frac{\sigma^2_{1}}{n_{1}} + \frac{\sigma^2_{2}}{n_{2}} }}
$$

independent data vs dependent data:

Collecting data from parents for children, parents and children share genes, so collecting data from parents and children will be dependent data. If we collect data from two restaurants, then it is also dependent if the owner is the same for both. 

Practice problem 7:

Two universities in the same state are bitter rivals. Each university believes that its students are more physically fit than the students at the other university. To test the claim that there is a difference in the average fitness levels of students at the two universities, 36 randomly selected students at the first university were surveyed and exercised for a mean of 2.9 hours per week. A random sample of 38 students at the second university was also surveyed, and exercised for a mean of 2.7 hours per week. Assume that the population standard deviation for hours of exercise at the first university is known to be 1.1 hours per week and the population standard deviation for the second university is known to be 1.0 hour per week. Use a 0.05 level of significance to perform a hypothesis test to determine if there is a difference in the average fitness levels of students at the two universities.

$H_{0} :\mu_{1} =\mu_{2}$, $H_{1}: \mu_{1} \neq \mu_{2}$ 
$$
\begin{align}
H_{0}: \mu_{1}-\mu_{2} =0 \\
H_{1} \mu_{1}-\mu_{2} \neq 0
\end{align}
$$
