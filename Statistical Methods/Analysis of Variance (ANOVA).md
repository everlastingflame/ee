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
Statistical model:


## F-test
## Tukey's method

## Bonferroni

## Kruskal-Wallis test


# Two way tests
One dependent variable and two independent variables