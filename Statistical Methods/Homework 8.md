  Adult-onset diabetes is known to be highly genetically determined. A study was done comparing frequencies of a particular allele in a sample of such diabetics and a sample of nondiabetics. The data are shown in the following table:

|          | Diabetic | Normal |
| -------- | -------- | ------ |
| Bb or bb | 12       | 4      |
| BB       | 39       | 49     |
a.) Are the relative frequencies of the alleles significantly different in the two groups? Use $\alpha=0.01$.
$$
\begin{align}
&H_{0}: \text{There is no difference between the relative frequencies } \\
&H_{a}: \text{Not } H_{0}
\end{align}
$$

| 12  | 4   | 16  |
| --- | --- | --- |
| 39  | 49  | 88  |
| 51  | 53  | 104 |
$N_{11} \in (\text{max}(0,16 + 51 -  104), \text{min}(16,51))=(0,16)$
$n_{1.} = 16$
$n_{2.}=88$
$n_{21}=39$
$n_{.1}=51$
$n_{..}=104$

$$
\begin{align}
P(N_{11}=0) = \frac{\begin{pmatrix} 16 \\ 0 \end{pmatrix} \begin{pmatrix}
88 \\ 39 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx 0\\
P(N_{11}=1) = \frac{\begin{pmatrix} 16 \\ 1 \end{pmatrix} \begin{pmatrix}
88 \\ 38 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx 0\\
P(N_{11}=2) = \frac{\begin{pmatrix} 16 \\ 2 \end{pmatrix} \begin{pmatrix}
88 \\ 37 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx 0.0007\\
P(N_{11}=3) = \frac{\begin{pmatrix} 16 \\ 3 \end{pmatrix} \begin{pmatrix}
88 \\ 36 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx 0.0022 \\
P(N_{11}=4) = \frac{\begin{pmatrix} 16 \\ 4 \end{pmatrix} \begin{pmatrix}
88 \\ 35 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx 0.0049 \\
P(N_{11}=5) = \frac{\begin{pmatrix} 16 \\ 5 \end{pmatrix} \begin{pmatrix}
88 \\ 34 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx 0.0077 \\
P(N_{11}=6) = \frac{\begin{pmatrix} 16 \\ 6 \end{pmatrix} \begin{pmatrix}
88 \\ 33 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx 0.0087\\
P(N_{11}=7) = \frac{\begin{pmatrix} 16 \\ 7 \end{pmatrix} \begin{pmatrix}
88 \\ 32 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx  0.0073\\
P(N_{11}=8) = \frac{\begin{pmatrix} 16 \\ 8 \end{pmatrix} \begin{pmatrix}
88 \\ 31 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx 0.0046 \\
P(N_{11}=9) = \frac{\begin{pmatrix} 16 \\ 9 \end{pmatrix} \begin{pmatrix}
88 \\ 30 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx 0.0023 \\
P(N_{11}=10) = \frac{\begin{pmatrix} 16 \\ 10 \end{pmatrix} \begin{pmatrix}
88 \\ 29 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx 0.0008 \\
P(N_{11}=11) = \frac{\begin{pmatrix} 16 \\ 11 \end{pmatrix} \begin{pmatrix}
88 \\ 28 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx 0.0002 \\
P(N_{11}=12) = \frac{\begin{pmatrix} 16 \\ 12 \end{pmatrix} \begin{pmatrix}
88 \\ 27 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx 0 \\
P(N_{11}=13) = \frac{\begin{pmatrix} 16 \\ 13 \end{pmatrix} \begin{pmatrix}
88 \\ 26 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx 0 \\
P(N_{11}=14) = \frac{\begin{pmatrix} 16 \\ 14 \end{pmatrix} \begin{pmatrix}
88 \\ 25 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx 0 \\
P(N_{11}=15) = \frac{\begin{pmatrix} 16 \\ 15 \end{pmatrix} \begin{pmatrix}
88 \\ 24 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx 0 \\
P(N_{11}=16) = \frac{\begin{pmatrix} 16 \\ 16 \end{pmatrix} \begin{pmatrix}
88 \\ 23 \end{pmatrix}}{\begin{pmatrix}
104 \\ 51
\end{pmatrix}} &\approx 0
\end{align}
$$
$\text{RR}= 0,1,2,3,12,13,14,15,16$
We reject $H_{0}$ since $12 \in \text{RR}$

b.) What is the relevant odds ratio?
$$
\Delta = \frac{(12)(49)}{(39)(4)} \approx 3.7692
$$
Diabetes is nearly 4 times as likely with BB alleles than with Bb or bb

## Problem 2
Phillips and Smith(1990) conducted a study to investigate whether people could briefly postpone their deaths until after the occurrence of a significant occasion. The senior woman of the household plays a central ceremonial role in the Chinese Harvest Moon Festival. Phillips and Smith compared the mortality patterns of old Jewish women and old Chinese women who died of natural causes for the weeks immediately preceding and following the festival, using records from California for the years 1960–1984. Compare the mortality patterns shown in the table. (Week −1 is the week preceding the festival, week 1 is the week following, etc.). Use $\alpha = 0.05$

| Week | Chinese | Jewish |     |
| ---- | ------- | ------ | --- |
| -2   | 55      | 141    | 196 |
| -1   | 33      | 145    | 178 |
| 1    | 70      | 139    | 209 |
| 2    | 49      | 161    | 210 |
|      | 207     | 586    | 793 |
$$
\begin{align}
&H_{0}: \pi_{11} = \pi_{12} =\dots= \pi_{42} \\
&H_{a}: \text{Not } H_{0}
\end{align}
$$

| $O_{ij}$ | Chinese  | Jewish   |          |
| -------- | -------- | -------- | -------- |
| $N_{1.}$ | 55       | 141      | 196      |
| $N_{2.}$ | 33       | 145      | 178      |
| $N_{3.}$ | 70       | 139      | 209      |
| $N_{4.}$ | 49       | 161      | 210      |
|          | 207      | 586      | 793      |
|          | $N_{.1}$ | $N_{.2}$ | $n_{..}$ |
$$
\begin{align} \\
E_{ij} &= \frac{n_{.j}\cdot n_{i.}}{n_{..}}\\
E_{11} &= \frac{207\cdot 196}{793} \approx 51.1627 \\
E_{12} &= \frac{586\cdot 196}{793} \approx 144.8373 \\
E_{21} &= \frac{207\cdot 178}{793} \approx 46.4640 \\
E_{22} &= \frac{586\cdot 178}{793} \approx 131.5359 \\
E_{31} &= \frac{207\cdot 209}{793} \approx 54.5561 \\
E_{32} &= \frac{586\cdot 209}{793} \approx 154.4439 \\
E_{41} &= \frac{207\cdot 210}{793} \approx 54.8172 \\
E_{42} &= \frac{586\cdot 210}{793} \approx 155.1828
\end{align}
$$

| $E_{ij}$ |         |          |
| -------- | ------- | -------- |
|          | 51.1627 | 144.8373 |
|          | 46.4640 | 131.5359 |
|          | 54.5561 | 154.4439 |
|          | 54.8172 | 155.1828 |
$$
\begin{align}
\chi^2 &=\sum_{i=1}^I \sum_{j=1}^J \frac{(O_{ij}-E_{ij})^2}{E_{ij}} \\
\chi^2 &= \frac{(55-51.1627)^2}{51.1627} +  \frac{(141-144.8373)^2}{144.8373}+\dots \approx 12.4208 \\ \\
\alpha &= 0.05, \chi^2_{(3)}(\alpha=0.05) = 7.815 \\
\end{align}
$$
Since our test statistic is greater than the chi-squared value, we reject the null hypothesis. 

## Problem 3
Overfield and Klauber (1980) published the following data on the incidence of tuberculosis in relation to blood groups in a sample of Eskimos. Is there any association of the disease and blood group within the ABO system? Use $\alpha = 0.05$

![[Pasted image 20260331145339.png]]

$$
\begin{align}
&H_{0}: \text{There is no relation between the disease and blood group within ABO system} \\
&H_{a}: \text{Not } H_{0}
\end{align}
$$


| $O_{ij}$ | Severity          | O        | A        | B        | AB       |          |
| -------- | ----------------- | -------- | -------- | -------- | -------- | -------- |
| $N_{1.}$ | Moderate-Advanced | 7        | 5        | 3        | 13       | 28       |
| $N_{2.}$ | Minimal           | 27       | 32       | 8        | 18       | 85       |
| $N_{3.}$ | Not Present       | 55       | 50       | 7        | 24       | 136      |
|          |                   | 89       | 87       | 18       | 55       | 249      |
|          |                   | $N_{.1}$ | $N_{.2}$ | $N_{.3}$ | $N_{.4}$ | $n_{..}$ |

| $E_{ij}$ |         |         |        |         |
| -------- | ------- | ------- | ------ | ------- |
|          | 10.0080 | 9.7831  | 2.0241 | 6.1847  |
|          | 30.3815 | 29.6988 | 6.1446 | 18.7751 |
|          | 48.6104 | 47.5181 | 9.8313 | 30.0402 |

$$
\begin{align}
\chi^2 &= 15.3696\\
\chi^2_{6}(0.05) &= 12.592 
\end{align}
$$
We reject the null hypothesis, there is a relation between blood group and ABO system

## Problem 4
Records of 317 patients at least 48 years old who were diagnosed as having endometrial carcinoma were obtained from two hospitals (Smith et al. 1975). Matched controls for each case were obtained from the two institutions; the controls had cervical cancer, ovarian cancer, or carcinoma of the vulva. Each control was matched by age at diagnosis(within four years) and year of diagnosis (within two years) to a corresponding case of endometrial carcinoma. This sort of design, called a retrospective case-control study, is frequently used in medical investigations where a randomized experiment is not possible. The following table gives the numbers of cases and controls who had taken estrogen for at least 6 months prior to the diagnosis of cancer. Is there a significant relationship between estrogen use and endometrial cancer? Do you see any possible weak points in a retrospective case-control design? Use $\alpha =0.05$
![[Pasted image 20260331164144.png]]

A major weak point I noticed at first was that this study suffers from recall bias, where patients are asked to remember their estrogen use from months or years before their diagnosis, having a diagnosis of cancer may make people more accurate with what they were taking beforehand, whereas the control may not recall as carefully. There is also selection bias, where the controls weren't healthy people, but instead people with other cancers. The control group isn't healthy so it may obscure the linkage between cancer and estrogen usage. 

$$
\begin{align}
&H_{0}: \pi_{12} = \pi_{21}, \text{ estrogen usage has no effect.} \\
&H_{a}: \text{Not } H_{0}
\end{align}
$$
$$
\begin{align}
&\chi^2 = \frac{(113-15)^2}{113+15}=36.0263 \\
&\chi^2_{1}(0.05) = 3.841
\end{align}
$$
We reject $H_{0}$

## Problem 5

Suppose that a company wishes to examine the relationship of gender to job satisfaction, grouping job satisfaction into four categories: very satisfied, somewhat satisfied, somewhat dissatisfied, and very dissatisfied. The company plans to ask the opinions of 100 employees. Should you, the company’s statistician, carry out a chi-square test of independence or a test of homogeneity?

The statistician should carry out a chi-square test of independence, since the gender is not pre-defined, and the population is randomly sampled and tallied later on. The main question that is being asked is if gender is associated to job satisfaction. 