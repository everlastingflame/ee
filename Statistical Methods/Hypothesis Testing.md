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


