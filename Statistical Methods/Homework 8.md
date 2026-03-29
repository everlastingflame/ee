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
