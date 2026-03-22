[[Statistical Methods]]

Two main cases for ANOVA, comparing population means or if populations have the same distribution or not

## F-Distributions 

The F-distribution with $d_{1}$ and $d_{2}$ degrees of freedom is the distribution of 
$$
X = \frac{\frac{S_{1}}{d_{1}}}{\frac{S_{2}}{d_{2}}}
$$
$S_{1}$ and $S_{2}$ are independent random variables with chi-squared distributions with $d_{1}$ numerator degrees of freedom and $d_{2}$ denominator degrees of freedom. It is a continuous distribution on $(0,\infty)$, not symmetrical (skewed to the right)

## What is ANOVA? 
Situation where we want to compare population means. Examples include phone manufacturer wanting to compare the average talk times for several different models of cellular phone, or a marketing director wants to compare the average numbers of tickets sold for various promotional campaigns

# One way tests
Includes one independent variable, one dependent variable. the independent variable has to be quantitative. 

The method: 

One factor (indep variable, different populations per group)

|          | $\mu_{1}$ | $\mu_{2}$ | $\dots$ | $u_{i}$  |
| -------- | --------- | --------- | ------- | -------- |
| sample1  | group 1   | group 2   | $\dots$ | group I  |
| sample2  | $Y_{11}$  | $Y_{21}$  | $\dots$ | $Y_{I1}$ |
| sample3  | $Y_{12}$  | $Y_{22}$  | $\dots$ | $Y_{I2}$ |
| $\dots$  | $\dots$   | $\dots$   | $\dots$ | $\dots$  |
| sample J | $Y_{1J}$  | $Y_{2J}$  | $\dots$ | $Y_{IJ}$ |
|          |           |           |         |          |
$Y_{ij}=$ the $j$th observation of $i$th treatements, I groups, J samples
$\mu$ is the overall mean of the population for all treatments, $\mu_{i}$ is the mean of the population for treatment i

We want to know if the mean for each population significantly deviates from the global population. 

One way ANOVA:

$$
Y_{ij}= \mu+ \alpha_{i}+ \epsilon_{ij} ,\, \, \sum_{i=1}^I \alpha_{i}=0
$$
We find the population mean $\mu$. For each population, they each have their own mean. The sum of each group multiplied by the number of groups must equal the population mean.  i.e, $\sum \mu_{i} =I \cdot \mu$
We also compare each population mean, 
$$
\begin{align}
\alpha_{1}= \mu_{1}-\mu \\
\alpha_{2}=\mu_{2}-\mu \\
\dots \\
\alpha_{I}=\mu_{I}-\mu
\end{align}
$$
The random error, known as $\epsilon_{ij}$ is the difference among the data points within one group. The $\alpha$ and random error are both contributors to their differences. $\alpha$ describes between group differences and $\epsilon$ describes within group differences. These are both sources of variation. 

Important formulas:
$$
\begin{align}
\sum_{i=1}^I \alpha_{i}&=0 \\
E(Y_{ij})&= \mu+\alpha_{i} \\
\bar{Y}_{i.} &= \frac{1}{J} \sum_{j=1}^J Y_{ij} \\
\bar{Y}_{..}&=\frac{1}{IJ} \sum_{i=1}^I \sum_{j=1}^J Y_{ij} \\
\sum_{i=1}^I \sum_{j=1}^J (Y_{ij}- \bar{Y}_{..})^2&= \sum_{i=1}^I\sum_{j=1}^J (Y_{ij}- \bar{Y}_{.})^2 +J\sum_{j=1}^J (Y_{i.}- \bar{Y}_{..})^2\\
\text{SS}_{\text{TOT}}&= \text{SS}_{\text{W}} + \text{SS}_{\text{B}}
\end{align}
$$
## F-test

We apply this test when the $I$ populations of interest are normally distributed with equal standard deviations, all samples are independent and randomly selected from each population

Hypothesis:
$$
\begin{align}
&H_{0}: \mu_{1}=\mu_{2}=\dots \mu_{I} \\
&H_{a}: \text{At least one } \mu \text{ is different}
\end{align}
$$
or 
$$
\begin{align}
&H_{0}: \alpha_{1}=\alpha_{2}=\dots \alpha_{I} \\
&H_{a}: \text{At least one } \alpha_{i} \text{ is different}
\end{align}
$$

| Source of Variation | Sum of Squares           | Degrees of Freedom | Mean Square                         | F-Statistic                                                                  |
| ------------------- | ------------------------ | ------------------ | ----------------------------------- | ---------------------------------------------------------------------------- |
| Between groups      | $\text{SS}_{\text{B}}$   | $I-1$              | $\frac{\text{SS}_{\text{B}}}{I-1}$  | $\frac{\frac{\text{SS}_{\text{B}}}{I-1}}{\frac{\text{SS}_{\text{W}}}{IJ-1}}$ |
| Within groups       | $\text{SS}_{\text{W}}$   | $IJ-1$             | $\frac{\text{SS}_{\text{W}}}{IJ-1}$ |                                                                              |
| Total               | $\text{SS}_{\text{TOT}}$ | $IJ-1$             |                                     |                                                                              |
Total: Reject $H_{0}$ if $F \geq F_{\alpha}$


## Tukey's method
Assumptions: The populations of interest are normally distributed with equal standard deviations, the observations are independent within and among groups. Groups must have equal sizes

Hypotheses:
$$
\begin{align}
H_{0}: \mu_{l}-\mu_{k} = 0 \\
H_{1}: \mu_{l}-\mu_{k} \neq 0
\end{align}
$$
For all pairs $(l,k): l\neq k$

Test statistic:
$$
q_{\text{Tukey}}= \frac{|\bar{Y}_{l}-\bar{Y}_{k}-0|}{\frac{S_{P}}{\sqrt{ J }}}, s^2_{p} = \frac{\text{SS}_{\text{W}}}{I(J-1)}
$$
Rejection region: Reject $H_{0}$ if $q_{\text{Tukey}}> q_{I, IJ-1}(\alpha)$ or p-value $< \alpha$. The values of $q_{I,IJ-1}(\alpha)$ are found in a table. 

In specific wording, we have that
$$
\begin{align}
&\text{Reject } H_{0} \text{ if } q_{\text{Tukey}}=\frac{|\bar{Y}_{l}-\bar{Y}_{k}|}{\frac{S_{p}}{\sqrt{ J }}} >q_{I,IJ-I}(\alpha) \\
&\text{Reject } H_{0} \text{ if } |\bar{Y}_{l}-\bar{Y}_{k}|  > q_{I,IJ-I}(\alpha) \cdot \frac{S_{p}}{\sqrt{ J }} \\
&\text{Accept } H_{0} \text{ if } |\bar{Y}_{l}-\bar{Y}_{k}| \leq q_{I,IJ-I}(\alpha)\cdot \frac{S_{p}}{\sqrt{ J }} \\
&\text{Condfidence interval for } \mu_{l}-\mu_{k}:  (\bar{Y}_{j}-\bar{Y}_{k}) -q_{I,IJ-I}(\alpha) \cdot \frac{S_{p}}{\sqrt{ J }} \leq 0 \leq (\bar{Y}_{j}-\bar{Y}_{k}) +q_{I,IJ-I}(\alpha) \cdot \frac{S_{p}}{\sqrt{ J }}
\end{align}
$$
## Bonferroni

If m null hypotheses are to be tested, a desired overall type 1 error rate of at most $\alpha$ can be guaranteed by testing each of the null hypothesis at level $\frac{\alpha}{m}$. Equivalently, if m CIs are each formed to have $CI 100\left( 1-\frac{\alpha}{m} \right)\%$ then they all hold simultaneously with CI at least $100(1-\alpha)\%$ Does not require equal sample sizes in each treatment. Critical T values are found in the table. 

For the test below: 
$m=C(2,I)=\frac{I!}{2(I-2)!}$

Hypothesis:
$$
\begin{align}
H_{0}: \mu_{l}-\mu_{k} =0 \\
H_{1}: \mu_{l} - \mu_{k} \neq 0
\end{align}
$$
For all pairs $(l,k): l\neq k$
$$
\begin{align}
\alpha &= P\left( |(\bar{Y}_{l}-\mu_{l})-(\bar{Y}_{k}-\mu_{k})|< t_{I(J-1)}\left( \frac{\alpha}{2m} \right) S_{p} \frac{2}{\sqrt{ J }}\right) \\
&= P\left( \frac{(|(\bar{Y}_{l}-\mu_{l})-(\bar{Y}_{k}-\mu_{k})|}{S_{p} \sqrt{\frac{2}{J} }} <t_{I(J-1)} \left(\frac{\alpha}{2m}\right)\right) \\
CI &= \mu_{l}-\mu_{k} \in (\bar{Y}_{l}-\bar{Y}_{k}) \pm t_{I(J-1)}\left(\frac{\alpha}{2m}\right) S_{p} \sqrt{ \frac{2}{J} }
\end{align}
$$
## Kruskal-Wallis test

No assumption about the type of distribution, however the main assumption is that the standard deviations are equal among populations and all samples are independent and randomly selected from each population. The factor (independent variable) is a categorical variable with two or more groups (treatments or levels), the response (dependent variable) is numerical. This is an adjusted version of the Mann-Whitney test where the results are ranked. 


![[Pasted image 20260322161007.png]]
# Two way tests
One dependent variable and two independent variables

We assume that the populations of interest are approximately normally distributed with equal standard deviations and all the samples are independent and randomly selected from each population. The factors are categorical variables each with two or more groups

### F-Test

![[Pasted image 20260322161441.png]]


	

![[Pasted image 20260322161505.png]]