[[Statistical Methods]] often employ sampling and analyzing data, which inherently defines what the study of statistics boils down to. 


Review topics below:
### Summary of elementary statistics:
The main goal of statistics is to study datasets. Datasets sample the **population** that we are interested in. If the goal was to extract particular trends or behaviors from the population, we would have to sample as it is not possible to gather all of the data from the entire population. The group that we're interested in is the population, and again, we study the sample, which is the data that we've collected from. There could be many samples from the population, so data collected from different parts of the population could be different from what we have collected. If we wanted to understand the behaviors of the entire population we need to know the probability that our conclusion reflects the entire population. If there is a low probability that the sample represents the population, then the conclusion we make is not reliable. We want to know the chance of the probability of the conclusion that it is reliable. Statistics primarily controls how we collect data and sample the population, as well as what we do to analyze the data. This is primarily what statisticians do. Probability is a necessity for the entirety of statistics. 

There is a measurement necessary for describing the population, for example if we're studying the health of newborns, weight could be a variable in the population we study. A **variable** is just a characteristic of the population that varies. 

### Qualitative vs Quantitative data:
Quantitative data are counts or measurements that are obtained through counting and measuring
Qualitative data are characteristics or observations 
The methods used for these types of data are completely different from each other, so it is important to understand what kind of data you are working with before you start preforming tat methods
You need to ask if you count or measure your data, then it would be quantitative, if not, then it is qualitative. 

Rankings:
Does not imply a particular count or measurement, so they must be qualitative.

### Discrete vs Continuous Quantitative data
Continuous data can take on any value on an interval, discrete data only takes on a particular set of values. 

Common mistake: creating histograms and trying to create a continuous distribution 

Two types of measures:
Measures of location, measures of variability

Newborn data:
**Location**
Measures of location: collect data from 100 newborns, getting a quick idea of their health, calculate the average weight of the newborns. 
(Mean, median, mode, trimmed min, percentiles, quantiles, 5 number summary (max, min, q1,q2,q3)) Tell us about the typical value of our data (how big the values are)

Measures of variability:
(variance, standard deviation)

### Density Curves

If you have quantitative continuous data, you can use the curve to make an approximation on the data. If you have a bell shaped curve, it is normally distributed. If it is skewed left or right (the flat "tail" determines the leftness or rightness of the skew) 
The density curve just represents the distribution of values in a dataset. This gives us an idea of the shape of our data 


### Cumulative Distribution Function (CDF)
$$
F(x) = P(X) \leq x = \int_{-\infty}^{x} f(t) dt
$$
There is a one-one correspondence from PDF to CDF. If we know the PDF, we can determine the CDF by taking the integral. To find the PDF from the CDF, all we need is $F'(x) = f(x)$

### Probability Density Function (PDF)
We describe the PDF as the curve that lie on the measures of each variable. 

![[Pasted image 20260121195122.png]]

### Empirical Cumulative Density Function (ECDF)
$$
\text{ECDF}(x) = \frac{1}{n}(\#x_{i} \leq x)
$$
Defined as the average number of values less than or equal to $x$, used to display the data from lowest to highest from their percentiles.

Example:
1.) Plot the ECDF of this batch of numbers: $1, 14,10,9,11,9$
$$
\begin{align}
&n = 6 \\
&\text{Dataset: } 1,9,9,10,11,14 \\
& \text{ECDF}(1) = \frac{1}{6}(1)=\frac{1}{6}=0.1\bar{6} \\
& \text{ECDF}(9) = \frac{1}{6}(3) = \frac{1}{2} = 0.5 \\
& \text{ECDF}(10) = \frac{1}{6}(4)=\frac{2}{3} = 0.\bar{6} \\
& \text{ECDF}(11) = \frac{1}{6}(5) = \frac{5}{6}= 0.8\bar{3} \\
& \text{ECDF}(14) = \frac{1}{6}(6) = \frac{6}{6} = 1
\end{align}
$$
Points: $(1,0.1\bar{6}), (9,0.5), (10, 0.\bar{6}), (11, 0.8\bar{3}), (14, 1)$
ECDF is a piecewise function that is continuous from the right. 
```tikz
\begin{document}
\begin{tikzpicture}[scale=1.7, xscale = 0.4, yscale = 1.6]
    % Axes
    \draw[->] (-0.5,0) -- (15.5,0) node[right] {$x$};
    \draw[->] (0,-0.2) -- (0,1.3) node[above] {ECDF$(x)$};
    
    % Grid (optional)
    \draw[gray!30, very thin] (0,0) grid[step=1] (15,1);
    
    % Y-axis labels
    \foreach \y in {0, 0.167, 0.5, 0.667, 0.833, 1.0} {
        \draw (0,\y) -- (-0.1,\y) node[left, font=\small] {$\y$};
    }
    
    % X-axis labels
    \foreach \x in {0,1,5,9,10,11,14,15} {
        \draw (\x,0) -- (\x,-0.05) node[below, font=\small] {$\x$};
    }
    
    % ECDF step function
    % Start at 0
    \draw[blue, thick] (0,0) -- (1,0);
    % Jump at x=1
    \draw[blue, thick, fill=blue] (1,0) circle (1.5pt);
    \draw[blue, thick, fill=white] (1,0.167) circle (1.5pt);
    \draw[blue, thick] (1,0.167) -- (9,0.167);
    % Jump at x=9
    \draw[blue, thick, fill=blue] (9,0.167) circle (1.5pt);
    \draw[blue, thick, fill=white] (9,0.5) circle (1.5pt);
    \draw[blue, thick] (9,0.5) -- (10,0.5);
    % Jump at x=10
    \draw[blue, thick, fill=blue] (10,0.5) circle (1.5pt);
    \draw[blue, thick, fill=white] (10,0.667) circle (1.5pt);
    \draw[blue, thick] (10,0.667) -- (11,0.667);
    % Jump at x=11
    \draw[blue, thick, fill=blue] (11,0.667) circle (1.5pt);
    \draw[blue, thick, fill=white] (11,0.833) circle (1.5pt);
    \draw[blue, thick] (11,0.833) -- (14,0.833);
    % Jump at x=14
    \draw[blue, thick, fill=blue] (14,0.833) circle (1.5pt);
    \draw[blue, thick, fill=white] (14,1) circle (1.5pt);
    \draw[blue, thick] (14,1) -- (15,1);
    \draw[blue, thick, fill=blue] (15,1) circle (1.5pt);
    
    % Data points (optional, for emphasis)
    \fill[red] (1,0.167) circle (2pt);
    \fill[red] (9,0.5) circle (2pt);
    \fill[red] (10,0.667) circle (2pt);
    \fill[red] (11,0.833) circle (2pt);
    \fill[red] (14,1) circle (2pt);
    
\end{tikzpicture}
\end{document}
```
A common practice is to bring up the level 0. You can also connect the vertical lines so that it looks like a stair. 
A curve can be created to approximate the curve of the CDF, $F(x)$

We can use the ECDF to determine the proportions, percentiles for data ranges
Identify the mode, assess the range of the data, compare sample distros, and se how well it fits the distribution. 

We know that the mode of a bell curve by looking at its peak, so we can follow this logic.

We can determine the mode of the dataset using the ECDF by looking at the biggest jumps between points. In this example, the biggest jump happens around the point 9, so that would be our mode. 

Proportion of values between 9 and 11? Y coordinate of 9 is 0.5, or 50% of the data, so about 50% of the data is less than or equal to 9. 11 has a Y coordinate of 0.83, so if we take the difference of these two, we find that that ~23% of the data is between 9 and 11. 

Proportion of values between 8 and 13, 0.833 - 0.167 = 0.67.

### Survival function
$$
S(t) = 1-F(t)
$$
### Hazard function
$$
h(t) = \frac{f(t)}{1-F(t)} = -\frac{d}{dt}\log S(t)
$$
Where $f$ is the density function and $F$ is the CDF of $f$

Proof
$$
\begin{align}
S(t) = 1-F(t) \\
\log S(t) = \log(1-F(t)) \\
\frac{d}{dt}\log S(t) = \frac{1}{1-F(t)}\cdot -(f(t)) \\
\frac{d}{dt}\log S(t) = \frac{f(t)}{1-F(t)} \\
h = \frac{f(t)}{1-F(t)} = -\frac{d}{dt}\log S(t)
\end{align}
$$
Can be thought as the instantaneous rate of mortality for an individual alive at time $t$. If $T$ is the lifetime of a device, $h(t)$ is just the instantaneous or age-specific related failure


Example:
![[Pasted image 20260121202559.png]]

a.) To compute this rate, we must do the following calculations:

$$
\begin{align}
&\text{a.) } \frac{4}{3 \cdot 1200} = \frac{1}{900} \approx 0.0011 \\
&\text{b.) } \frac{6}{2\cdot (1200-4)} = \frac{6}{2392} \approx 0.00251 \\
&\text{c.) } 
\end{align}
$$


### Hazard Function Example:

$$
\begin{align}
F(t) = 1-\exp((-\alpha t)^\beta) \\
F'(t) = f(t) \\
f(t)  =-\alpha\beta t^{\beta-1}\exp((-\alpha t)^\beta) \\
h(t) = \frac{-\alpha\beta t^{\beta-1}\exp((-\alpha t)^\beta)}{\exp((-\alpha t)^\beta)} \\
h(t) = -\alpha \beta t^{\beta-1}
\end{align}
$$

