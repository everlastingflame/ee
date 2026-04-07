
## Problem 1

A chain of sports clubs wishes to use regression analysis to help determine which features should be included in their new location. They believe that median income in the area is a significant factor in determining the number of people who join a neighborhood sports club. The CEO of the chain gathered data from existing sports clubs regarding the number of members each club had, the median income in the area in which they were located, and whether the clubs had a pool, racquetball courts, or group fitness classes. If management can determine with 90% confidence that a pool, racquetball courts, or group fitness classes produces significantly more memberships than sports clubs without those features, they will include them in the new location.

![[Pasted image 20260403113532.png]]

a.) What sign do you expect the correlation coefficient between the number of members and the median income to have (without calculating)? Explain why.

I believe there will be a positive correlation between number of members and median income just from a cursory overview of the table. As you go down the table, it seems as though that with more members, the higher the median income is. 

b.) Create three dummy variables, pool, courts, and classes, that are equal to 1 if the observation contains this feature and equal to 0 if the observation does not contain this feature.
![[Pasted image 20260403114117.png]]
I used the code:
```
IF(C3 = "Yes", 1, 0)
IF(D3 = "Yes", 1, 0)
IF(E3 = "Yes", 1, 0)
```
After which I dragged down to have the formula apply to each of the columns

b.) Use statistical software to estimate the following regression models. In each case, write the estimated regression equation and state whether the coefficient of the independence variable is significant at the 0.10 level. (Make sure to include the following in your answers: hypotheses $H_{0}$ and $H_{a}$, test statistic value, p-value, conclusion.)

b.i) $\text{Members } = \beta_{0}+\beta_{1}(\text{Pool}) + \epsilon_{i}$
$$
\begin{align}
H_{0}: \beta_{1} =0 \\
H_{a}: \beta_{1} \neq 0
\end{align}
$$
![[Pasted image 20260403115141.png]]
We reject the null hypothesis
$$
\text{Members}= 2298.3+ 1432\beta_{1}
$$
b.ii) $\text{Members } = \beta_{0}+\beta_{1}(\text{Courts}) + \epsilon_{i}$

$$
\begin{align}
H_{0}: \beta_{1} =0 \\
H_{a}: \beta_{1} \neq 0
\end{align}
$$

![[Pasted image 20260403115332.png]]
We fail to reject the null hypothesis

b.iii) $\text{Members } = \beta_{0}+\beta_{1}(\text{Classes}) + \epsilon_{i}$

$$
\begin{align}
H_{0}: \beta_{1} =0 \\
H_{a}: \beta_{1} \neq 0
\end{align}
$$
![[Pasted image 20260403115403.png]]

We reject the null hypothesis, this test is significant. 
$$
\text{Members}= 1860.833 + 1559.267\beta_{1}
$$

d.) Estimate the following multiple regression model
$$
\text{Members}=\beta_{0}+\beta_{1}(\text{Income}) + \beta_{2}(\text{Pool})+\beta_{3}(\text{Courts})+\beta_{4}(\text{Classes})
$$
![[Pasted image 20260403120839.png]]
$$
\text{Members}=-961.402+  0.059861 \beta_{1}+ 84.13826 \beta_{2} + 77.67654 \beta_{3}-75.6709 \beta_{4}
$$
e.) Only median income in this situation is statistically significant. 
f.) Income is very important here because it seems as though it is positively correlated with the number of members. It also has a p-value of essentially 0, meaning that it is significant. 
g.) The sports chain should focus on my last model, and if they were to tweak it, they should just use the income as a variable and not worry about the rest. 



## Problem 2

The Supplemental Nutrition Assistance Program (SNAP) provides monthly benefits that help eligible low-income households buy the food they need for good health. For most households, SNAP finds account for only a portion of their food budgets, so they must also use their own funds to buy enough food to last throughout the month. Eligible households can receive food assistance through regular SNAP or through the Louisiana Combined Application Project (LaCAP). Using the data in the table, answer the following questions to help predict monthly benefits to eligible households.

![[Pasted image 20260407114921.png]]

a.) I think a good regression model to fit would be using the Gross Monthly and Family size as independent variables, Monthly Benefit as the output

b.) 
$$
\begin{align}
H_{0}: \beta_{1}= \beta_{2}=0 \\
H_{1}: \beta_{1} \neq \beta_{2} \neq 0
\end{align}
$$

![[Pasted image 20260407115551.png]]

$$
\alpha=0.05
$$
$$
\text{Monthly Benefit} = 40.79031 + 3.6594(\text{Family Size})+0.1461(\text{Gross Monthly Income})
$$
c.) This test is significant, we can reject the null hypothesis. I think the gross monthly income is a stronger indicator of monthly benefit, the family size does not provide a strong signal for this dataset.

d.) Give a 95% confidence interval for average monthly benefits for a four-member household with a gross monthly income of $2500. Interpret this interval.

![[Pasted image 20260407133918.png]]

There is a probability of 95% that a family of four with an income of $2500 receives SNAP benefits between $410.701-$430.768

e.) Provide a 99% prediction interval for a four-member household with a gross monthly income of $2500. Interpret this interval.

![[Pasted image 20260407134220.png]]

There is a 99% chance that the same family will receive snap benefits between $338.934-$502.535

f.) What is the difference between the intervals found in parts d and part e?

The spread is much wider with a higher confidence level. 



