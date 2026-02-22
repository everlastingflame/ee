
### Problem 1
Let $X_{1}, X_{2}, \dots , Xn$ be a random sample from the Poisson distribution. Find the likelihood ratio for testing $H_{0}: \lambda = \lambda_{0}$ versus $H_{1}: \lambda = \lambda_{1}$, where $\lambda_{1} > \lambda_{0}$. Use the fact that the sum of independent Poisson random variables follows a Poisson distribution to explain how to determine a rejection region for a test at level $\alpha$

$$
\begin{align}
P(X=x) &= \frac{e^{-\lambda}\lambda^x}{x!} \\
L(\lambda;x) &= \prod_{i=1}^n \frac{e^{-\lambda}\lambda^{x_{i}}}{x_{i}!} \\
L(\lambda;x) &= \left( e^{-n\lambda}\lambda^{\sum_{i=1}^n x_{i}} \right) \cdot \prod_{i=1}^n \frac{1}{x_{i}!} \\
\Lambda &=\frac{\left( e^{-n\lambda_{0}}\lambda_{0}^{\sum_{i=1}^n x_{i}} \right) \cdot \prod_{i=1}^n \frac{1}{x_{i}!}}{\left( e^{-n\lambda_{1}}\lambda_{1}^{\sum_{i=1}^n x_{i}} \right) \cdot \prod_{i=1}^n \frac{1}{x_{i}!}} \\
 &= \frac{e^{-n\lambda_{0}}\lambda_{0}^{\sum_{i=1}^nx_{i}}}{e^{-n\lambda_{1}}\lambda_{1}^{\sum_{i=1}^nx_{i}}} \\
 &= \frac{e^{-n\lambda_{0}}\lambda_{0}^{T(x)}}{e^{-n\lambda_{1}}\lambda_{1}^{T(x)}} \\
 &= e^{n(\lambda_{1}-\lambda_{0})}\lambda_{0}^{T(x)}\lambda_{1}^{-T(x)} \\
&=e^{n(\lambda_{1}-\lambda_{0})}\left( \frac{\lambda_{0}}{\lambda_{1}} \right)^{T(x)}
\end{align}
$$
Solving for the rejection region:
$$
\begin{align}
\Lambda &< c \\
e^{n(\lambda_{1}-\lambda_{0})}\left( \frac{\lambda_{0}}{\lambda_{1}} \right)^{T(x)} &< c \\
\ln\left( \exp\left( n(\lambda_{1}-\lambda_{0})\right) \left(\frac{\lambda_{0}}{\lambda_{1}} \right)^{T(x)} \right) &<\ln (c) \\
n(\lambda_{1}-\lambda_{0})+T(x)(\ln(\lambda_{0})-\ln(\lambda_1)) &< \ln(c) \\
T(x)(\ln(\lambda_{0})-\ln(\lambda_{1}))&< \ln(c) - n(\lambda_{1}-\lambda_{0}) \\
T(X) &> \frac{\ln(c) - n(\lambda_{1}-\lambda_{0})}{\ln(\lambda_{0})-\ln(\lambda_{1})} \text{ (Flips since } \lambda_{1} >\lambda_{0} \text{)}  \\
\text{RR: } (x: T(X) > k | \lambda = \lambda_{0}) &=\alpha, \, T(X) \sim \text{Poisson}(n\lambda_{0})
\end{align}
$$
### Problem 2
Currently, 20% of potential customers buy soap of brand A. To increase sales, the
company will conduct an extensive advertising campaign. At the end of the campaign, a
sample of 400 potential customers will be interviewed to determine whether the
campaign was successful.
a.) State $H_{0}$ and $H_{1}$ in terms of p, the probability that a customer prefers soap brand A.

$$
H_{0}=0.2, H_{1} >0.2
$$

b.) The company decides to conclude that the advertising campaign was a success if at
least 92 of the 400 customers interviewed prefer brand A. Find $\alpha$. (Use the normal
approximation to the binomial distribution to evaluate the desired probability.)

$$
\begin{align}
RR &= \left\{ x: \sum_{i=1}^{400} x_{i} >92 \right\} \\
X_{i} &\sim \text{ i.i.d. } B(0.2), i=1,2,\dots 400 \\
\alpha &= P\left( \sum_{i=1}^{400} x_{i} > 92 | p = 0.2 \right) \\
400(0.2) &= 80 > 10, x = \sum_{i=1}^{400}x_{i} \sim N(\mu, \sigma) \\
\text{where } \mu &= np, \sigma =\sqrt{ npq } \\
\mu &= 400(0.2) = 80 \\
\sigma &= \sqrt{ npq } = \sqrt{ 400(0.2)(1-0.2)} = 8 \\
x &\sim N(80, 8) \\
P(X  >92 | p = 0.2) &= P\left( Z > \frac{92-80}{8} \right) = P(Z > 1.5) \\
\alpha &=P(X > 92 | p = 0.2) = P(Z > 1.5) = 0.0668
\end{align}
$$
### Problem 3
Let $X$ be a binomial random variable with $n$ trials and probability $p$ of success. What is
the generalized likelihood ratio for testing $H_{0}: p = 0.5$ versus $H_{1}: p \neq 0.5$

$$
\begin{align}
L(p) &=  \begin{pmatrix} n \\ x \end{pmatrix}p^{x}(1-p)^{n-x} \\
\text{max}_{p=0.5 }\, L(p) &=  \begin{pmatrix} n \\ x \end{pmatrix}(0.5)^{x}(0.5)^{n-x} =  \begin{pmatrix} n \\ x \end{pmatrix} 0.5^n \\
\text{max}_{p \in [0,1]}\, L(\hat{p}_{\text{MLE}}) &=  \begin{pmatrix} n \\ x \end{pmatrix}\left( \frac{x}{n} \right)^{x}\left( 1- \frac{x}{n} \right)^{n-x} \\
\Lambda(p) &= \frac{(0.5)^n}{\left( \frac{x}{n} \right)^{x}\left( 1- \frac{x}{n} \right)^{n-x}}
\end{align}
$$
### Problem 4
A coin is thrown independently 10 times to test the hypothesis that the probability of
heads is 0.5 versus the alternative that the probability is not 0.5. The test rejects if either
0 or 10 heads are observed. What is the significance level of the test?

$$
\begin{align}
H_{0} &= 0.5, \, H_{1} \neq 0.5 \\
RR &= \{x: x \in \{0,10\} \} \\
\alpha &= P(x = 0 \text{ or } x= 10 | p = 0.5)=P(x=0|p=0.5)+P(x=10 | p=0.5) \\
\alpha &= \begin{pmatrix} 10 \\ 0\end{pmatrix}(0.5)^{0}(1-0.5)^{10} + \begin{pmatrix} 10 \\ 10 \end{pmatrix}(0.5)^{10}(1-0.5)^{0} \\
&=\begin{pmatrix} 10 \\ 0 \end{pmatrix}(0.5)^{10} + \begin{pmatrix} 10 \\ 10 \end{pmatrix}(0.5)^{10} = \frac{1}{512} \approx 0.00195

\end{align}
$$
### Problem 5

The intensity of light reflected by any object is measured. Suppose there are two types of possible objects, A and B. If the object is of type A, the measurement is normally distributed with mean 100 and standard deviation 25; if it is of type B, the measurement is normally distributed with mean 125 and standard deviation 25. A single measurement is taken with the value $X = 120$. Consider the test $H_{0}$: Item is of type A versus $H_{a}$: item is of type B.

a.) Calculate the likelihood ratio statistic of this test

$$
\begin{align}
L(x; \sigma, \mu) &= \prod_{i=1}^n \frac{1}{\sigma \sqrt{ 2\pi }}\exp\left( - \frac{(x_{i}-\mu)^2}{2\sigma^2} \right) \\
L(x; \sigma, \mu) &=\frac{1}{(\sigma \sqrt{2\pi })^n}\exp\left( \sum_{i=1}^n -\frac{(x_{i}-\mu)^2}{2\sigma^2} \right) \\
\Lambda &=\frac{\frac{1}{25 \sqrt{2\pi }}\exp\left( -\frac{(120-100)^2}{2(25)^2} \right)}{\frac{1}{25 \sqrt{2\pi }}\exp\left( -\frac{(120-125)^2}{2(25)^2} \right)} \\
&= \frac{\exp\left( -\frac{(120-100)^2}{2(25)^2}\right)}{\exp\left( -\frac{(120-125)^2}{2(25)^2} \right)} \approx 0.7408182
\end{align}
$$
b.) If the prior probabilities of A and B are equal (1/2 each), what is the posterior
probability that the item is of type B?

$$
\begin{align}
P(B|X=120) &= \frac{P(X=120|B)\cdot P(B)}{P(X=120)} \\
P(X=120)&= P(X=120|A)\cdot P(A) + P(X=120|B) \cdot P(B) \\
&= \frac{1}{25\sqrt{ 2\pi }}\exp\left( -\frac{(20)^2}{2(25)^2} \right)\cdot(0.5) + \frac{1}{25 \sqrt{ 2\pi }} \exp\left( - \frac{(-5)^2}{2(25)^2} \right) \cdot(0.5) \\
P(B|X=120) &= \frac{\frac{1}{25 \sqrt{ 2\pi }} \exp\left( - \frac{(-5)^2}{2(25)^2} \right) \cdot(0.5) }{ \frac{1}{25\sqrt{ 2\pi }}\exp\left( -\frac{(20)^2}{2(25)^2} \right)\cdot(0.5)+ \frac{1}{25 \sqrt{ 2\pi }} \exp\left( - \frac{(-5)^2}{2(25)^2} \right) \cdot(0.5) } \approx 0.574442516812
\end{align} 
$$

c.) Suppose that a decision rule has been formulated that declares the object to be of
type B if $X > 125$. What is the significance level of this test?

$$
\begin{align}
\alpha &= P(X > 125 | X \sim N(100,25)) \\
&= P\left( Z > \frac{125-100}{25} \right) = P(Z > 1) \approx 0.15866
\end{align}
$$
d.) What is the power of this test?

$$
\begin{align}
1-\beta &= P( X > 125 | X \sim N(125, 25)) \\
 &= P\left( Z > \frac{125-125}{25}\right) = P(Z >0) =0.5
\end{align}
$$
e.) What is the p-value when $X = 120$? 
$$
\text{p-value } = P(X=120 | N \sim (100,25)) = P\left( Z > \frac{120-100}{25} \right) =P(Z>0.8) \approx 0.21186
$$

















