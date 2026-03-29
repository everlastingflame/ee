[[Statistical Methods]]
Most of this data analysis is done with two way tables, where there are different categorical variables for both the columns and rows of data. 

Our goal is to know if these two categorical variables are independent or dependent. 

## Fisher's Exact Test

A statistical test to determine if there are nonrandom associations between two categorical variables. Usually employed when sample sizes are small, but it is valid for all sample sizes. We use this in general when the row totals and the column totals are fixed by design, the sample size is small, and more than 20% of the cells have expected cell counts less than 5, and no expected cell amount is less than 1. 



We know that any distribution is associated with an experiment, and any experiment associated with the [[Hypergeometric Distribution]] has $M$ successes in $N$ trials, where the number $x$ is the number of success in the first $n$ trials. 

| $N_{11}$ | $N_{12}$ | $n_{1.}$ |
| -------- | -------- | -------- |
| $N_{21}$ | $N_{22}$ | $n_{2.}$ |
| $n_{.1}$ | $n_{2.}$ | $n_{..}$ |

Test statistic:
$$
P(n_{11})= \frac{\begin{pmatrix}
n_{1.} \\ n_{11}
\end{pmatrix}
\begin{pmatrix}
n_{2.} \\ n_{21}
\end{pmatrix}}{\begin{pmatrix}
n_{..} \\ n_{.1}
\end{pmatrix}}
$$

$N_{11}$ is the number of successes in $n_{.1}$ draws without replacement from a population of $n_{1}$ successes and $n_{2.}$ failures. 
$n_{1.}$ is the number of successes
$n_{2.}$ is the number of failures
$n_{.1}$ is the number of draws 

Here we consider the famous tea tasting example! In a summer tea party in Cambridge, England, a lady claimed to be able to discern, by taste alone, whether a cup of tea with milk had the tea poured first or the milk poured first. An experiment was performed by Sir R.A. Fisher himself, then and there, to see if her claim was valid. Eight cups of tea were prepared and presented to her in random order. Four had the milk poured first, and other four had the tea poured first. The lady tasted each one and rendered her opinion. The results are summarized in the following table:

| actually poured first (row) | Lady says poured first (col) |      |        |       |
| --------------------------- | ---------------------------- | ---- | ------ | ----- |
|                             | tea                          | milk | Totals |       |
| tea                         | 3                            | 1    | 4      | $M$   |
| milk                        | 1                            | 3    | 4      | $N-M$ |
| totals                      | 4                            | 4    | 8      | $N$   |
|                             | $n$                          |      |        |       |
Test at $\alpha = 0.1$

Step 1.) Write out the two hypotheses:
$$
\begin{align}
&H_{0}: \text{The lady has no distinguishing ability} \\
&H_{1}: \text{Not } H_{0}
\end{align}
$$
Step 2.) List all possible values for $N_{11}$

$N_{11} = 0,1,2,3,4$

Step 3.) Compute the probabilities for all possible values of $N_{11}$
$$
\begin{align}
P(N_{11}=0) = \frac{\begin{pmatrix}4 \\0\end{pmatrix}\begin{pmatrix}4 \\4\end{pmatrix}}{\begin{pmatrix}8 \\4\end{pmatrix}} =0.01428 \\
P(N_{11}=1) = \frac{\begin{pmatrix}4 \\1\end{pmatrix}\begin{pmatrix}4 \\3\end{pmatrix}}{\begin{pmatrix}8 \\4\end{pmatrix}} =0.2285 \\
P(N_{11}=2) = \frac{\begin{pmatrix}4 \\2\end{pmatrix}\begin{pmatrix}4 \\2\end{pmatrix}}{\begin{pmatrix}8 \\4\end{pmatrix}} = 0.5142 \\
P(N_{11}=4) = \frac{\begin{pmatrix}4 \\3\end{pmatrix}\begin{pmatrix}4 \\1\end{pmatrix}}{\begin{pmatrix}8 \\4\end{pmatrix}} = 0.2285\\
P(N_{11}=4) = \frac{\begin{pmatrix}4 \\4\end{pmatrix}\begin{pmatrix}4 \\0\end{pmatrix}}{\begin{pmatrix}8 \\4\end{pmatrix}} =0.01428 \\
\end{align}
$$
Step 4.) Make a conclusion:
Way 1: RR, $\alpha = 0.1$

We order the values:
0.014286, 0.014286, 0.228571, 0.228571, 0.5142
$N_{11} =0$



Or we take the p-value: 

$(0.014286)\cdot 2+ 0.228571\cdot 2 >0.1$, fail to reject $H_{0}$

### Example 2
In one experiment, the supervisors were given a personnel file and had to decide whether to promote the employee or to hold the file and interview additional candidates. By random selection, 24 of the supervisors examined a file labeled as being that of a male employee and 24 examined a file labeled as being that of a female employee; the files were otherwise identical. The results are summarized in the following table:

|           | Male | Female |     |       |
| --------- | ---- | ------ | --- | ----- |
| Promote   | 21   | 14     | 35  | $M$   |
| Hold File | 3    | 10     | 13  | $M-N$ |
|           | 24   | 24     | 48  | $N$   |
|           | $n$  |        |     |       |
Test if there is a sex bias, use $\alpha =0.05$

$H_{0}$ There is no bias
$H_{1}$ There is a bias

Step 2.) $N_{11} = 11,12,13,\dots,24$
Cannot be 0,1,2,3... because we marginalize such that 
$N_{11} \geq 0$
$N_{12} = M- N_{11} \geq 0$
$N_{21} = n- N_{11} \geq 0$
$N_{22} = M-N - (n -N_{11}) \geq 0$

Step 3.) Calculate probabilities using hypergeometric dist

| $n_{11}$           | 11          | 12          | 13      | 14     | 15      | 16      | 17      |     |
| ------------------ | ----------- | ----------- | ------- | ------ | ------- | ------- | ------- | --- |
| $P(N_{11}=n_{11})$ | $\approx 0$ | $\approx 0$ | $0.004$ | $0.02$ | $0.072$ | $0.162$ | $0.241$ | ... |
$\alpha = 0.05$
$RR = 11,12,13,14,15,16,17,18,19,20,21,22,23,24$ Keep adding until it passes 0, 

$21 \in RR, \text{ We reject } H_{0}$ There is bias. 9



### The Chi-Square test of Homogeneity
