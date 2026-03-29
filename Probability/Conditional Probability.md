[[Probability]]
Sometimes knowing that an event $A$ occurred cant tell you whether or not event $B$ occurred. Other times, knowing that an event $A$ occurred changes the probability that event $B$ occurred. 

Definiton:
If $P(B) >0$ then,
$$
P(A|B) = \frac{P(A \cap B)}{P(B)}
$$
Examples:
If we roll 2 dice, what is the probability that their sum is 8?
We know there are 36 possible outcomes with equal probability
{(2,6), (3,5), (4,4), (5,3), (6,2)} are the only possible outcomes, so therefore the probability is just 5/36

If we know the first die is a 3, what is the probability the sum is an 8? 
There are now fewer outcomes, since the set of outcomes is:
{(3,1), (3,2), (3,3), (3,4), (3,5), (3,6)}, and out of this set, there is only one option, (3,5), so it is 1/6

To illustrate:
$$
P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{\frac{1}{36}}{\frac{6}{36}}
$$
Multiplication rule:
$A_{1},A_{2},\dots,A_{n}$ are all events where
$$
\begin{align}
&P(A_{1} \cap A_{2} \cap \dots \cap A_{n}) = P(A_{1}) \cdot P(A_{2}|A_{1})\cdot P(A_{3}|A_{2} \cap A_{1})\dots \cdot \cdot P(A_{n}|A_{1} \cap A_{2} \cap\dots A_{n-1}) \\
&P(A_{1}) \cdot \frac{P(A_{1} \cap A_{2})}{P(A_{2})} \cdot \frac{P(A_{1} \cap A_{2} \cap A_{3})}{P(A_{1} \cap A_{2})} \cdot \dots \cdot \frac{P(A_{1} \cap A_{2} \cap\dots A_{n-1})}{P(A_{1} \cap A_{2} \cap\dots \cap A_{n-1})} \cdot \frac{P(A_{1}\cap A_{2} \cap \dots \cap A_{n})}{P(A_{1} \cap A_{2} \cap \dots \cap A_{n-1})} \\
&= P(A_{1} \cap A_{2} \cap \dots \cap A_{n})
\end{align}
$$

Bayes Rule:
$$
P(A|B) = \frac{P(A \cap B)}{{P(B)}} = \frac{P(B|A)P(A)}{P(B)}
$$
Why are we able to switch? We have the identity that 
$$
\begin{align}
P(B|A) &= \frac{P(A \cap B)}{P(A)} \\
P(B|A)P(A) &= P(A \cap B)
\end{align}
$$
We can also express $P(B)$ as:
$$
P(B) = P(B \cap A) + P(B\cap A^C)
$$
Example:
A disease has a rate of 1/10000. A test screening for this diseases has a 99% accuracy rate –that is, if you have the disease, you will test positive 99% of the time, and if you don’t have the disease, you will test negative 99% of the time. If someone receives a positive test, what’s their probability of having the disease?
$A = \text{probability of having disease}, B= \text{probability of positive test}$

$$
P(A|B) = \frac{P(A \cap B)}{{P(B)}} = \frac{P(B|A)P(A)}{P(B)}=\frac{P(B|A)P(A)}{P(A \cap B)+P(B \cap A^C)} = \frac{\frac{99}{100} \cdot \frac{1}{10000}}{0.99\cdot\frac{1}{10000}+0.01\cdot\frac{9999}{10000}} 
$$
