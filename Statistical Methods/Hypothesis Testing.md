[[Statistical Methods]]

An example:
John has two coins:
Coin 0 has P(heads) = $p_{0}$ = 0.5 <- fair
Coin 1 has P(heads) = $p_{1}$ = 0.7 <- unfair

John chooses a coin and tosses it $n=10$ times and tells mary the number of heads he got, not telling her whether or not it was coin 0 or coin 1. On the basis of the number of heads, what should Mary's decision rule be?

The sample space is $X \in S \{0,1,2,3,4,5,6,7,8,9,10 \}$ 
For each coin, the probability that John gets exactly $x$ heads is
$$
 P_{i}(X=x) = \begin{pmatrix}
n \\x
\end{pmatrix}p_{i}^x(1-p_{i})^x
$$
If we get two heads, we find that 
$$
\frac{P_{0}(X=2)}{P_{1}(X=2)} = 30
$$
Which means that coin 0 is 30 times as likely to produce two heads than coin 1. This is known as the likelihood ratio

Hypothesis testing is a technique for testing a claim about a population parameter using statistical principles.

The alternative hypothesis, denoted by $H_{\alpha}$ (or $H_{\alpha}$, $H_{1}$), is the hypothesis that the researcher is aiming to gather evidence in favor of; it is also referred to as the research hypothesis

The null hypothesis, denoted by $H_{0}$ , is the mathematical opposite of the alternative hypothesis; it will always include equality.

Determining the null and alternative hypotheses:

At Northwest Mississippi Community College, syllabi for online classes state that students should expect to spend 10 hours per week doing coursework for each three-credit-hour class. The director of eLearning for the community college is concerned that students are being required to spend more than 10 hours per week doing work for each three-credit course.

$H_{0}$ is believed to be true by everyone else
$H_{1}$ is the concern/belief of the researcher. 
$$
\begin{align}
H_{0} :\mu \leq 10 \\
H_{1} : \mu >10
\end{align}
$$
or
$$
\begin{align}
H_{0} : \mu = 10 \\
H_{1} : \mu > 10
\end{align}
$$


The best way to go about solving hypothesis testing problems is to first understand what the baseline value is, what everyone already believes, this is usually the null hypothesis. When the question is asking "different from" it is a two-tailed test, where the null hypothesis is either $=$ or $\neq$ to the value we're searching for. When it's greater than, we have a one tailed test, and likewise for the less than. 

Significance or, $\alpha$ is the probability of rejecting our null hypothesis $H_{0}$ when it is true. This is known as **type 1 error**. The formal definition is:
$$
\alpha = P(\text{reject } H_{0} | H_{0})
$$
Accepting the null hypothesis when it is false is called **type 2 error**, the probability of this is denoted as 
$$
\beta = P(\text{Accept } H_{0} |H_{1})
$$
We can find the **power** of the test by subtracting the type 2 error from 1, which can alternatively be written as rejecting the null hypothesis given the alternative hypothesis. The higher this value is, the better the test is. We can write this as:
$$
\text{power} = 1-\beta = 1-(\text{Accept } H_{0}| H_{1}) =P( \text{Reject } H_{0}| H_{1})
$$
An important thing to note is that $\alpha + \beta \neq 1$
Another thing to note is the probability distribution of the statistic when the null hypothesis is true is known as the **null distribution**

Rejecting $H_{0}$ or accepting $H_{0}$ does not really tell us a lot, and does not tell us the strength of evidence against $H_{0}$. We can summarize this evidence in terms of $p$. For every $\alpha  \in (0,1)$, we have a test of significance level $\alpha$ with a rejection region $RR_{\alpha}$. The p-value is the smallest significance level at which we can reject $H_{0}$. 
$$
\text{p-value} = \text{inf}\{\alpha: X \in RR_{\alpha} \}
$$
It can also be said that the p-value is the probability of obtaining a sample statistic as extreme or more extreme than the observed data, when the null hypothesis, $H_{0}$ is assumed to be true. A smaller p-value is stronger evidence against $H_{0}$. 

