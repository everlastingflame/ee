
## Problem 1
The results of a comparison of four popular minivans are reported in the following table. One of the features the researchers compared was the distance (in feet) required for the minivan to come to a complete stop when traveling at a speed of 60 miles per hour (braking distance). Suppose the braking distances were measured for five minivans of each type with the following results.
Braking Distances (Feet)

| Minivan A | Minivan B | Minivan C | Minivan D |
| --------- | --------- | --------- | --------- |
| 150       | 153       | 155       | 167       |
| 152       | 150       | 150       | 164       |
| 151       | 156       | 157       | 169       |
| 149       | 151       | 158       | 162       |
| 153       | 155       | 155       | 173       |
| Total     |           |           |           |
| 755       | 765       | 775       | 835       |
a.) The researcher wished to perform an F-test to compare the average braking distances for the four minivan models. What assumptions must the researcher make to apply this test? Do the data appear to satisfy these assumptions? Explain.

In order to perform an F-test, the researcher must assume that each of the populations are normally distributed with equal standard deviations, all of the samples being randomly and independently selected from the population. It is very clear that the actual tests being performed are independent, so it can be fairly assumed that each observation is also independent. Each observation also seems to have a close grouping, indicating that it is also normal too. 

b.) Using the F-test, can the researcher conclude at $\alpha =0.10$ that there is a difference among average braking distances for the four minivan models?

$$
\begin{align}
&H_{0}: \mu_{A}=\mu_{B}=\mu_{C}=\mu_{D} \\
&H_{a}: \text{At least one } \mu \text{ is different}
\end{align}
$$
$$
\begin{align}
I&=4 \\
J&=5 \\
\bar{Y}_{1} &= 151 \\
\bar{Y}_{2} &= 153 \\
\bar{Y}_{3} &= 155 \\
\bar{Y}_{4} &= 167 \\
\bar{Y}_{..} &=  \frac{755+765+775+835}{20}= 156.5\\
\text{SS}_{\text{B}} &= 5\sum_{i=1}^4 (\bar{Y}_{i}-\bar{Y}_{..})^2 \\
&= 5[(151-156.5)^2+(153-156.5)^2+(155-156.5)^2+ (167-156.5)^2] \\
&= 775 \\
\text{SS}_{\text{W}} &=\sum_{i=1}^4 \sum_{j=1}^5 (Y_{ij}- \bar{Y}_{i.})^2 \\
&=(150 - 151)^2+(152-150)^2+\dots+(173-167)^2 \\
&= 148 \\
F &= \frac{\frac{\text{SS}_{\text{B}}}{I-1}}{\frac{\text{SS}_{\text{W}}}{I(J-1)}} = \frac{\frac{775}{3}}{\frac{148}{16}}=27.9279 \\
\alpha &=0.10 \\
d_{1} &= I-1 = 3 \\
d_{2} &= I(J-1) =16 \\
F_{\alpha} &= F_{3,16}(0.10) =2.46 \\
F \not< F_{\alpha} \, &, \text{ We reject } H_{0}
\end{align}
$$
Yes, we can conclude that there is a difference in the average breaking distances.
## Problem 2
Solve Problem 1 using the Tukey’s method. Compare the results to the results obtained by using the F-test.
$$
\begin{align}
H_{0}: \mu_{l}-\mu_{k} =0 \\
H_{1}: \mu_{l}-\mu_{k} \neq 0
\end{align}
$$
For all pairs $(l,k), l\neq k$
(Note: I used a python script to calculate each pair, therefore $\mu_{0}$ is really $\mu_{1}$ and $\mu_{1}$ is $\mu_{2}$, etc.)
$$
\begin{align}
&s_{p}^2 = \frac{\text{SS}_{\text{W}}}{I(J-1)}= \frac{148}{16}= 9.25 \\
&s_{p} = 3.0414 \\
&q_{I,IJ-1}(\alpha)=q_{3,16}(0.10)=3.12 \\
&q_{3,16}(0.10)\cdot \frac{3.0414}{\sqrt{ 5 }}= 4.2437 \\
&(μ_0 - μ_1) \pm 4.2437 = (2.2435,-6.2437) \ni 0\\
&(μ_0 - μ_2) \pm 4.2437 = (0.2435,-8.2437)\ni 0\\
&(μ_0 - μ_3) \pm 4.2437 = (-11.7563,-20.2437)\not \ni  0\\
&(μ_1 - μ_0) \pm 4.2437 = (6.2437,-2.2437)\ni 0\\
&(μ_1 - μ_2) \pm 4.2437 = (2.2437,-6.2437) \ni 0\\
&(μ_1 - μ_3) \pm 4.2437 = (-9.7563,-18.2437)\not \ni 0 \\
&(μ_2 - μ_0) \pm 4.2437 = (8.2437,-0.2437) \ni 0\\
&(μ_2 - μ_1) \pm 4.2437 = (6.2437,-2.2437)  \ni 0\\
&(μ_2 - μ_3) \pm 4.2437 = (-7.7563,-16.2437)\not \ni  0 \\
&(μ_3 - μ_0) \pm 4.2437 = (20.2437,11.7563) \not \ni  0\\
&(μ_3 - μ_1) \pm 4.2437 = (18.2437,9.7563)\not \ni  0\\
&(μ_3 - μ_2) \pm 4.2437 = (16.2437,7.7563)\not \ni  0\\
\end{align}
$$
We reject the null hypothesis for any pair including Minivan D, as Minivan D has a significant difference in the average braking distances as opposed to the other pairs. This is very similar to what we have found when doing an F-test.

## Problem 3
Solve Problem 1 using the Bonferroni method. Compare the results to the results obtained by using the Tukey’s method. Solve Problem 1 using the Bonferroni method. Compare the results to the results obtained by using the Tukey’s method.

$$
\begin{align}
H_0: \mu_{l} -\mu_{k}=0 \\
H_{1}: \mu_{l}-\mu_{k} \neq 0
\end{align}
$$
For all pairs $(l,k): l\neq k$
Assuming a confidence interval of 95%
$$
\begin{align} 
m = C(2,4)= \frac{4!}{2(2)!}=6\\
CI: \mu_{l}-\mu_{k} \in (\bar{Y}_{l.}-\bar{Y}_{k.}) \pm t_{I(J-1)}\left( \frac{\alpha}{m} \right)S_{p} \sqrt{ \frac{2}{J} } \\
(\bar{Y}_{l.}-\bar{Y}_{k.}) \pm t_{16}\left( \frac{0.10}{6} \right)(3.0414)\sqrt{ \frac{2}{5} } \\
(\bar{Y}_{l.}-\bar{Y}_{k.})\pm (3.46 )(3.0414)\cdot \sqrt{ \frac{2}{5} } \\
(\bar{Y}_{l.}-\bar{Y}_{k.})\pm6.6555 \\
(μ_0 - μ_1) \pm 4.2437 = (4.65548388274,-8.65548388274)\\
(μ_0 - μ_2) \pm 4.2437 = (2.6554838827399996,-10.65548388274)\\
(μ_0 - μ_3) \pm 4.2437 = (-9.34451611726,-22.65548388274)\\
(μ_1 - μ_0) \pm 4.2437 = (8.65548388274,-4.65548388274)\\
(μ_1 - μ_2) \pm 4.2437 = (4.65548388274,-8.65548388274)\\
(μ_1 - μ_3) \pm 4.2437 = (-7.34451611726,-20.65548388274)\\
(μ_2 - μ_0) \pm 4.2437 = (10.65548388274,-2.6554838827399996)\\
(μ_2 - μ_1) \pm 4.2437 = (8.65548388274,-4.65548388274)\\
(μ_2 - μ_3) \pm 4.2437 = (-5.34451611726,-18.65548388274)\\
(μ_3 - μ_0) \pm 4.2437 = (22.65548388274,9.34451611726)\\
(μ_3 - μ_1) \pm 4.2437 = (20.65548388274,7.34451611726)\\
(μ_3 - μ_2) \pm 4.2437 = (18.65548388274,5.34451611726)\\
\end{align}
$$
We find that this produces the same result as Tukey's method, where the intervals involving Minivan D produce imbalanced intervals. 

## Problem 4
An Internet service provider is considering four different servers for purchase. Potentially, the company would be purchasing hundreds of these servers, so it wants to make sure it is making the best decision. Initially, five of each type of server are borrowed, and each is randomly assigned to one of the 20 technicians (all technicians are similar in skill). Each server is then put through a series of tasks and rated using a standardized test. The higher the score on the test, the better the performance of the server. The data are as follows.

Server test scores

| Server 1 | Server 2 | Server 3 | Server 4 |
| -------- | -------- | -------- | -------- |
| 48.5     | 56.4     | 52.1     | 64.3     |
| 46.5     | 68.2     | 56.3     | 68.3     |
| 52.4     | 68.5     | 48.3     | 72.2     |
| 54.1     | 64.2     | 52.2     | 70.6     |
| 58.9     | 60.1     | 54.8     | 56.5     |
Perform a Kruskal-Wallis test on these data using $\alpha=0.10$. Are there differences between the servers?
$$
\begin{align}
&H_{0}:F_{1}=F_{2}=F_{3}=F_{4} \\
&H_{1}: \text{Not } H_{0}
\end{align}
$$
$$
\begin{align} \\
\bar{R}_{1} &= 5.8 \\
\bar{R}_{2} &= 14.2 \\
\bar{R}_{3} &= 5.6 \\
\bar{R}_{4} &= 16.4\\
H&=\frac{12}{20(20+1)}\left( \sum_{i=1}^4 J_{i} \bar{R}_{i}^2\right)-3(20+1) \\
&=\frac{12}{420}(2678.0) - 33 = 13.5143 \\
\chi^2_{3}(0.10) &= 6.25 \\
&\text{We reject } H_{0} \text{ since } H >\chi^2_{3}(0.10)
\end{align}
$$















