# Week 3

- **Classification** problems involve prediction on a boolean variable using data available.
- Applying Linear Regression to classification problems is not a great idea, as a few wide data points can skew the hypothesis and yield poor predictions.
- **Logistic Regression** is an algorithm used for classification problems where the output is always between 0 and 1 unlike Linear Regression. **Logistic Regression :** $0 \leq h_\theta \leq 1$  
- **Sigmoid Function** is defined as: $g(x) = \frac{1}{1-e^{-x}}$
- For Logistic Regression, as $0 \leq \theta \leq 1$, we take the hypothesis as:

    $h_\theta(x) = g(\theta^T x)$, where $g()$ is Sigmoid function.

- Now, $h_\theta (x)$ is seen as the probablity that y is 1, given x, and parameterized by $\theta$.
- An event is more likely if it's probability > 0.5. On the sigmoid funciton, $g(x) > 0.5$, if $x > 0$. Hence:

    If $h(\theta_T x) > 0 =>$ prediction is $y = 1$ is more probable.

- The **Decision Boundary** is a boundary that separates regions where $y = 0$ is predicted from regions where $y=1$ is predicted. It need not be linear, it can be totatlly abstract.
- 
```
--------------
INCOMPLETE
--------------
```