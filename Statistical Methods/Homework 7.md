Charles Booth. I pledge my honor that I have abided by the stevens honor code.
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
## Problem 5
The following table gives the survival times (in hours) for animals in an experiment whose design consisted of three poisons, four treatments, and four observations per cell.
![[Pasted image 20260324102638.png]]
Conduct a two-way analysis of variance to test the effects of the two main factors and their interaction. Use $\alpha = 0.10$

| Source of Variation | SS       | df  | MS      | F       | P-value | F crit |
| ------------------- | -------- | --- | ------- | ------- | ------- | ------ |
| Poison              | 103.0429 | 2   | 51.5215 | 23.5700 | 0       | 2.4563 |
| Treatment           | 91.9040  | 3   | 30.6347 | 14.0146 | 0       | 2.2426 |
| Interaction         | 24.7454  | 6   | 4.1242  | 1.8867  | 0.1100  | 1.9446 |
| Within              | 78.6925  | 36  | 2.1859  |         |         |        |
|                     |          |     |         |         |         |        |
| Total               | 298.3848 | 47  |         |         |         |        |
For Poison
$$
\begin{align}
&H_{0}: \alpha_{k}=0 \\
&H_{1}: \text{Not } H_{0} \\
&F=23.5700 \geq F_{2,36}(0.10) =2.44 \\
&\text{Reject } H_{0}
\end{align}
$$
For Treatment
$$
\begin{align}
&H_{0}: \beta_{k}=0 \\
&H_{1}: \text{Not } H_{0} \\
&F=14.0146 \geq F_{3,36}(0.10) =2.23 \\
&\text{Reject } H_{0}
\end{align}
$$
For Interaction 
$$
\begin{align}
&H_{0}: \delta_{ij}=0 \\
&H_{1}: \text{Not } H_{0} \\
&F=1.8867 \not\geq F_{6,36}(0.10) =1.93 \\
&\text{Fail to reject } H_{0}
\end{align}
$$


## Problem 6
A banana grower has three fertilizers from which to choose. He would like to determine which fertilizer produces banana trees with the largest yield (measured in pounds of bananas produced). The banana grower has noticed that there is a difference in the average yields of the banana trees depending on which side of the farm they are planted (South Side, North Side, West Side, or East Side). Because of the variation in yields among the areas on the farm, the farmer has decided to randomly select three trees within each area and then randomly assign the fertilizers to the trees. After harvesting the bananas, he calculates the yields of the trees within each of the areas. The results are as follows.
![[Pasted image 20260324112940.png]]

a.) Do you think a randomized block design is appropriate for the banana grower’s study? What assumptions must the banana grower make to apply this test? Do the data appear to satisfy these assumptions? Explain.

I think that using randomized block design here would be appropriate considering that the assumption when using this test is that there is no interaction between the block and the treatment. In this example, the banana farmer is specifically trying to see what fertilizer provides the best yield independently of where the tree is. The data appears to satisfy this because of how the testing was done, as a random tree was selected from each region, along with a fertilizer also being selected randomly too. The data seems to have very little variance, but it is hard to tell without doing any statistical analysis. 

b.) Perform a two-way ANOVA using randomized block design. Use $\alpha =0.10$

| Source of variation | SS     | df  | MS      | F     | p-value | F crit |
| ------------------- | ------ | --- | ------- | ----- | ------- | ------ |
| Location            | 36.25  | 3   | 12.0833 | 36.25 | 0.0003  | 3.2888 |
| Fertilizer          | 104    | 2   | 52      | 156   | 0.0000  | 3.4633 |
| Error               | 2      | 6   | 0.3333  |       |         |        |
|                     |        |     |         |       |         |        |
| Total               | 142.25 | 11  |         |       |         |        |
|                     |        |     |         |       |         |        |
For location
$$
\begin{align}
&H_{0}: \alpha_{k}=0 \\
&H_{1}: \text{Not } H_{0} \\
&F=36.25 \geq F_{3,6}(0.10) =3.28 \\
&\text{Reject } H_{0}
\end{align}
$$
For fertilizer
$$
\begin{align}
&H_{0}: \beta_{k}=0 \\
&H_{1}: \text{Not } H_{0} \\
&F=156 \geq F_{2,6}(0.10) =3.46 \\
&\text{Reject } H_{0}
\end{align}
$$



## Problem 7
Solve Problem 6 using the Friedman’s Test. Compare the results to the results obtained in Problem 6.

Ranked table:

|            | A   | B   | C   |
| ---------- | --- | --- | --- |
| South Side | 2   | 1   | 3   |
| North Side | 2   | 1   | 3   |
| West Side  | 2   | 1   | 3   |
| East Side  | 2   | 1   | 3   |

$$
\begin{align}
&H_{0}: \text{There is no effect for any fertilizer} \\
&H_{1}: \text{Not } H_{0}
\end{align}
$$
$$
\begin{align} \\
&J=4 \\
&I =3 \\
&\bar{R}_{1}: \frac{8}{4} = 2\\
&\bar{R}_{2}: \frac{4}{4} = 1\\
&\bar{R}_{3}: \frac{12}{4}=3 \\
&\bar{R}_{..}: \frac{8+4+12}{12} = 2 \\
&\sum(\bar{R}_{i}-\bar{R})^2=  (2-2)^2+(2-1)^2+(2-3)^2=2 \\
&Q = \frac{12J}{I(I+1)}\left( \sum(R_{i}-\bar{R}_{..})^2 \right) = \frac{48}{12}(2) = 8 \\
& \chi^2_{2}(0.10) = 4.605, Q \gt \chi^2_{2}(0.10), \text{ Reject } H_{0}
\end{align}
$$

