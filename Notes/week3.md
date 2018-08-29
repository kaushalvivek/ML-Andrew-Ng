# Week 3

- **Classification** problems involve prediction on a boolean variable using data available.
- Applying Linear Regression to classification problems is not a great idea, as a few wide data points can skew the hypothesis and yield poor predictions.
- **Logistic Regression** is an algorithm used for classification problems where the output is always between 0 and 1 unlike Linear Regression. **Logistic Regression :** $0 \leq h_\theta \leq 1$  
- **Sigmoid Function** is defined as: $g(x) = \frac{1}{1-e^{-x}}$
- For Logistic Regression, as $0 \leq \theta \leq 1$, we take the hypothesis as:

    $h_\theta(x) = g(\theta^T x)$, where $g()$ is Sigmoid function.

- Now, $h_\theta (x)$ is seen as the probablity that y is 1, given x, and parameterized by $\theta$.
- An event is more likely if it's probability > 0.5. On the sigmoid funciton, $g(x) > 0.5$, if $x > 0$. Hence:

    If $h(\theta_T x) > 0 =>$ prediction $y = 1$ is more probable.

- The **Decision Boundary** is a boundary that separates regions where $y = 0$ is predicted from regions where $y=1$ is predicted. It need not be linear, it can be totatlly abstract.
  
- **Cost Function for Logistic Regression:**

    $Cost(h_\theta(x),y) = -log(h_\theta(x)) if y=1$  
    $ -log(1-h_\theta(x)) if y=0$  

    For implementation, this equation can be represented as

    $Cost(h_\theta(x),y) = -y log(h_\theta(x)) - (1-y) log(1-h_\theta(x))$  

    Which implies that

    $J(\theta) = -\frac{1}{m}[\sum_{i=1}^m -y^(i) log(h_\theta(x^(i))) - (1-y^(i)) log(1-h_\theta(x^(i)))]$

- Minimization still done using gradient descent, with simultaneous updates to $\theta_j$
- The algorithm remains

  $\theta_j:=\theta_j-\alpha \frac{1}{m}\sum_{i=1}^m((h_\theta(x_i)-y_i)x_i)$

  but the definition of $h_\theta(x)$ has now changed.
```
--------------
INCOMPLETE
--------------
```