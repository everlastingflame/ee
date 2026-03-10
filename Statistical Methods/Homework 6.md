Charles Booth
I Pledge My Honor that I Have Abided by the Stevens Honor Code
## Problem 1

A software company markets a new computer game with two experimental packaging designs. Design 1 is sent to 11 stores; their average sales the first month is 52 units with a sample standard deviation of 12 units. Design 2 is sent to 6 stores; their average sales the first month is 46 units with a sample standard deviation of 10 units. Test at 1% level of significance whether the data provide sufficient evidence to conclude that the mean sales per month of the two designs are different.

$\alpha = 0.01$, $\bar{x}_{1} = 52, \, \sigma_{1}= 12, \, \bar{x}_{2} =46,\, \sigma_{2}=10$

$$
\begin{align}
H_{0}:\mu_{0}-\mu_{1} =0 \\
H_{1}: \mu_{0}-\mu_{1} \neq 0
\end{align}
$$
$$
t = \frac{(\bar{x}_{1} -\bar{x}_{2})-(\mu_{0}-\mu_{1})}{\sqrt{ \frac{s_{1}^2}{n_{1}} +\frac{s_{2}^2}{n_{2}}}}= \frac{6}{\sqrt{ \frac{144}{11}+\frac{100}{6} }}\approx 1.0999
$$
$$
t_{0.005} \text{ df}=5:4.032
$$
$$
1.0999 \ngeq 4.032
$$
We fail to reject the null hypothesis, so the evidence supports that the sales are different


## Problem 2
The standard course at a local defensive-driving school includes several films depicting violent car crashes and graphic pictures of injuries sustained in these crashes. The driving school has shown these videos for many years, believing that they reduce the students’ average speeds on the highway. A group of concerned citizens, who feel that these videos are very disturbing, is not convinced that the videos reduce highway speeds enough to make a significant difference in highway safety. In fact, the group claims that these videos Reduce a person’s speed on the highway by less than 5 miles per hour, on average. To test the claim, the citizens install electronic data recorders (EDRs) on the vehicles of 10 volunteers, who agree to drive as they would normally for two weeks while the EDR records their vehicles’ speeds. After the initial driving period, each volunteer watches the videos. Then the EDRs again record their vehicles’ speeds for another two weeks. The following table contains the average highway speeds for each volunteer for the two-week periods before and after watching the videos.

Average Highway Speeds (in Miles per Hour)

| Before | After |
| ------ | ----- |
| 75.83  | 72.13 |
| 80.12  | 73.87 |
| 65.41  | 66.09 |
| 70.03  | 68.43 |
| 73.91  | 71.45 |
| 76.02  | 73.67 |
| 75.10  | 70.19 |
| 67.89  | 65.34 |
| 81.12  | 75.31 |
| 77.67  | 70.92 |
Use these data to test the concerned citizens’ claim that these videos reduce a person’s speed on the highway by less than 5 miles per hour, on average. Use a 0.05 level of significance. Assume the paired differences are normally distributed.

$$
\begin{align}
H_{0}: \mu_{0} \geq 5 \\
H_{1}: \mu_{1} < 5
\end{align}
$$


$$\begin{align}
\bar{d} &= \frac{(75.83-72.1)+(80.12-73.87)+\dots}{10} \\
&= \frac{3.7+6.26-0.68+1.6+2.46+2.35+4.91+2.55+5.81+6.75}{10} \\
&= \frac{35.71}{10} = 3.571
\end{align}
$$
$$
s_{d} = \sqrt{\frac{(75.83-72.1)^2+(80.12-73.87)^2 +\dots}{9} }= \sqrt{ \frac{177.5011}{9} }\approx 4.441
$$
$$
t = \frac{3.571 -5}{\frac{4.441}{\sqrt{ 9 }}} = -1.002
$$
$$
t_{\alpha}=t_{0.05}= 3.250
$$
$$
-1.002 \nleq -3.250
$$
We accept the null hypothesis, these videos do in fact reduce the speed of drivers 

## Problem 3

A manufacturer fills soda bottles. Periodically the company tests to see if there is a difference between the mean amounts of soda put in bottles of regular cola and diet cola. A random sample of 14 bottles of regular cola has a mean of 501.6 ml of soda with a standard deviation of 3.9 ml. A random sample of 16 bottles of diet cola has a mean of 498.9 ml of soda with a standard deviation of 5.3 ml. Test the claim that there is a difference between the mean fill levels for the two types of soda using a 0.01 level of significance. Assume that the population variances are not equal since different machines are used to fill bottles of regular cola and diet cola. All populations are approximately normal.

$\bar{x}_{1} = 506.1$, $s_{1}=3.9$, $n=14$, $\bar{x}_{2}=498.9$, $s_{2}=5.3$, $n=16$ $\alpha=0.01$

$$
\begin{align}
H_{0}: \mu_{1}-\mu_{2}=0 \\
H_{1}: \mu_{1}-\mu_{2} \neq 0
\end{align}
$$
$$
\begin{align}
t&= \frac{506.1-498.9 -0}{\sqrt{ \frac{3.9^2}{14}+ \frac{5.3^2}{16} }}= 4.27087013992 \\
t_{\frac{\alpha}{2}}=t_{0.005} &= 3.012 \\
4.271 &\geq 3.012
\end{align}
$$
We reject the null hypothesis, there is indeed a difference in the amount of soda per bottle. 


## Problem 4

University official hope that changes they have made have improved the retention rate. Last year, a sample of 1926 freshmen showed that 1400 returned as sophomores. This year, 1508 of 2011 freshmen sampled returned as sophomores. Determine if there is sufficient evidence at the 0.05 level to say that the retention rate has improved.

$$
\begin{align}
H_{0}: p_{1}-p_{2}=0 \\
H_{a}: p_{1}-p_{2} \neq 0
\end{align}
$$
$$
\begin{align}
\hat{p}_{1} &= \frac{1400}{1926} \approx 0.727 \\
\hat{p}_{2} &= \frac{1508}{2011} \approx 0.750 
\end{align}
$$
$$
\begin{align}
z &= \frac{(\hat{p}_{1}-\hat{p}_{2})-(p_{1}-p_{2})}{\sqrt{ \frac{\hat{p}_{1}(1-\hat{p}_{1})}{n_{1}} + \frac{\hat{p}_{2}(1-\hat{p}_{2})}{n_{2}} }} \\
z &= \frac{0.727-0.750 -0}{\sqrt{ \frac{0.727(1-0.727)}{1926} + \frac{0.750(1-0.750)}{2011}}} = -1.64 = 0.0505 \\
p &= P(|Z| >|z| ) = 2(1-0.9495) = 0.101 \\
0.101 &> 0.05
\end{align}
$$
We fail to reject the null hypothesis, indicating that there is sufficient evidence to say that the retention rate has improved. 

## Problem 5
One study claims that the variance in the resting heart rates of smokers is different than the variance in the resting heart rates of nonsmokers. A medical student decides to test this claim. The sample variance of resting heart rates, measured in beats per minute, for a random sample of 5 smokers is 545.1. The sample variance for a random sample of 5 nonsmokers is 103.7. Test the study’s claim using a 0.01 level of significance.

$$
\begin{align}
H_{0}: \sigma^2_{1}-\sigma^2_{2}=0 \\
H_{1}: \sigma^2_{1}-\sigma^2_{2} \neq 0
\end{align}
$$
$$
\begin{align}
F &= \frac{s_{1}^2}{s_{2}^2} = \frac{545.1}{103.7} \approx 5.257 \\
\frac{1}{F_{0.005}} &< F < F_{0.005} \\
0.043 & \lt 5.256 < 23.15

\end{align}
$$
We fail to reject the null hypothesis. 
## Problem 6

An internal auditor for Tiger Enterprises has been asked to determine if there is a difference in the amount charged for daily expenses by two top salesmen, Mr. Ellis and Mr. Ford. The auditor randomly selects seven days and determines the daily expenses for each of the salesmen.

Daily Expenses

| Mr. Ellis | Mr. Ford |
| --------- | -------- |
| 55        | 60       |
| 53        | 55       |
| 58        | 65       |
| 54        | 50       |
| 56        | 70       |
| 55        | 55       |
| 55        | 65       |
a.) Using the Wilcoxon rank-sum test, can the auditor conclude that there is a
difference in the median amount charged for daily expenses by the two top
salesmen, Mr. Ellis and Mr. Ford? Use α = 0.05.

$$
\begin{align}
H_{0}&: \text{The distribution of } D_{i} \text{ is symmetric about 0} \\
H_{1}&: \text{Not } H_{0}
\end{align}
$$
$n=7$

| Mr. Ellis | Mr. Ford |
| --------- | -------- |
| 55        | 60       |
| 53        | 55       |
| 58        | 65       |
| 54        | 50       |
| 56        | 70       |
| 55        | 55       |
| 55        | 65       |

| Value | Salesman | Rank |
| ----- | -------- | ---- |
| 50    | Ford     | 1    |
| 53    | Ellis    | 2    |
| 54    | Ellis    | 3    |
| 55    | Ellis    | 6    |
| 55    | Ellis    | 6    |
| 55    | Ellis    | 6    |
| 55    | Ford     | 6    |
| 55    | Ford     | 6    |
| 56    | Ellis    | 9    |
| 58    | Ellis    | 10   |
| 60    | Ford     | 11   |
| 65    | Ford     | 12.5 |
| 65    | Ford     | 12.5 |
| 70    | Ford     | 14   |

$R = 2 + 3 + 6+ 6+ 6+ 6+ 6 + 9 + 10 = 48$
$R'= 7(7+7+1)-48 =57$
$R^{*} = \text{min}(48,57) =48$
$R^{*}\leq R_{\text{table}} =48 \not\lt 36$
We fail to reject the null hypothesis 

b.) What assumptions were made in performing the test in part a)?
We assume that this grouping does not follow any particular distribution. 


## Problem 7

The management for a large grocery store chain would like to determine if a new cash register will enable cashiers to process the same number of items on average as the cash register which they are currently using. Seven cashiers are randomly selected, and the number of grocery items which they can process in three minutes is measured for both the old cash register and the new cash register. Perform the Wilcoxon signed-rank test on the above data, given $\alpha=0.05$

$$
\begin{align}
&H_{0} \text{: Distribution of $D_{i}$ is symmetric about 0}\\
&H_{1} \text{: Not } H_{0}
\end{align}
$$

| Cashier                  | 1   | 2   | 3   | 4   | 5   | 6   | 7   |
| ------------------------ | --- | --- | --- | --- | --- | --- | --- |
| Before                   | 60  | 70  | 55  | 74  | 62  | 52  | 58  |
| After                    | 65  | 71  | 58  | 75  | 65  | 57  | 57  |
| $D_{i}$                  | 5   | 1   | 3   | 1   | 3   | 5   | -1  |
| $\|D_{i}\|$              | 5   | 1   | 3   | 1   | 3   | 5   | 1   |
| $\text{rank } \|D_{i}\|$ | 6.5 | 2   | 4.5 | 2   | 4.5 | 6.5 | 2   |
| signed rank              | 6.5 | 2   | 4.5 | 2   | 4.5 | 6.5 | -2  |

$W_{+}=6.5+2+4.5+2+4.5+6.5= 26$
$W_{-} = 2$
$W = \text{min}(26,2) = 2$
$W_{\alpha=0.05}=2$
$\text{min}(26,2)\leq W_{\alpha=0.05}=2\leq 2$

We fail to reject the null hypothesis. 