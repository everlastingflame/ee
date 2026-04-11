## Problem 1

#### Perceptron
https://www.cs.cornell.edu/courses/cs4780/2018fa/lectures/lecturenote03.html

The perceptron algorithm is a vectorized classification method that uses a hyperplane and orthogonal weight vector, adjusting the hyperplane to separate the data over time. The pros of this algorithm is that they guarantee convergence in a finite number of steps if the data is linearly separable, which is also a con since this algorithm doesn't work with non-linearly separable data. 

#### Random forest
https://www.ibm.com/think/topics/random-forest
Random Forest is an ensemble version of the decision tree classification algorithm, the difference being that random forest creates several decision trees at once and classifies based on which tree is selected the most. The pros of this algorithm is that it fixes common overfitting problems that occur in decision trees by using ensemble learning, a process by which an algorithm simulates several models at once and aggregates the most popular results found across all the models. The difference here is that Random Forest will choose these decisions based on correlation, only creating models in the ensemble that have low correlation with each other. The cons of this algorithm is that since it is simulating multiple models at once, it is incredibly computationally intensive, and since it is creating several different models the results can be hard to understand. 

#### Ordinal Regression
https://www.geeksforgeeks.org/machine-learning/ordinal-regression/
Ordinal regression is a version of regression that deals with ordered data, such as a ranking or rating. Normal regression isn't as strong here since it treats all values the same, whereas ordinal regression respects this order, changing the problem into a binary classifier where it looks at each sample and checks if it is greater or less than the predefined ordered labels. The pros rest in the fact that this algorithm respects the order, making it more accurate than regression when using ordered labels. It also has very easy to interpret results. A major limitation with this algorithm is that it is harder to implement than regular regression, since it requires more delicate data handling. 

## Problem 2

Apply the Naive Bayes Classifier to the “iris” dataset (that is provided to you in the direction of the HW 10 assignment by following the below requirements:

1) Use sepal.length for the dependent variable and all other features (sepal.width, petal.length, petal.width, variety) for the independent variables.
2) Turn sepal.length into a qualitative variable with four possible values: Four (for sepal.length values from 4.0 to 4.9), Five (for sepal.length values from 5.0 to 5.9), Six (for sepal.length values from 6.0 to 6.9), and Seven (for sepal.length values from 7.0 to 7.9).
3) The goal is to use Naive Bayes Classifier to classify flowers into one of the four classes Four, Five, Six, or Seven based on their sepal width, petal length, petal width and variety. Note that variety is a qualitative variable, and sepal.width, petal.length and petal.width are quantitative.
4) Please write out clearly your answer for the probabilities $\pi_{k}$ and density functions $f_{kj}$, as well as explain how they are obtained. Make sure to include all graphs, plots, screenshots of output, etc.

$n=150$
$$
\pi_{k} = \left\{ \begin{matrix}
4: \frac{22}{150}&=0.1467\\
5: \frac{61}{150}&=0.4067\\
6: \frac{54}{150}&=0.36\\
7: \frac{13}{150}&=0.0867\\
\end{matrix} \right\}
$$
I obtained all of the following values by using the encoded classes and taking the mean, variance, and STD of the subset of corresponding features.

![[Pasted image 20260411131836.png]]


The formula for each $f_{kj}$ is:
$$
f_{kj}=(x_{j}) \frac{1}{\sqrt{ 2\pi \sigma^2_{kj} }}\exp \left( -\frac{(x_{j}-\mu_{kj})^2}{2\sigma^2_{kj}}\right)
$$
Here is a density plot of each of the features with their respective classes
![[Pasted image 20260411133156.png]]


Here are the proportions of each for each class and feature
![[Pasted image 20260411133249.png]]

And here is the corresponding proportion for each class.

![[Pasted image 20260411133328.png]]

For any new observation, you would have to use the formula to classify it:
$$
p_{k}(x)=\frac{\pi_{k}\cdot f_{k1}(x_{1})\cdot f_{k2}(x_{2}) \cdot f_{k3}(x_{3})\cdot f_{k4}(x_{4})}{\sum_{i=1}^4 \pi_{i} \cdot f_{i1}(x_{1})\cdot f_{i2}(x_{2})\cdot f_{i3}(x_{3})\cdot f_{i4}(x_{4})}
$$
In this formula, $f_{kj}$ is the gaussian density of sepal.width, petal.length, petal.width, and variety.  