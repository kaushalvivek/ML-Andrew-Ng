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

    $Cost(h_\theta(x),y) = -log(h_\theta(x))$ if $y=1$
            $ -log(1-h_\theta(x))$ if $y=0$  

    For implementation, this equation can be represented as

    $Cost(h_\theta(x),y) = -y log(h_\theta(x)) - (1-y) log(1-h_\theta(x))$  

    Which implies that

    $J(\theta) = -\frac{1}{m}[\sum_{i=1}^m -y^i log(h_\theta(x^i)) - (1-y^i) log(1-h_\theta(x^i))]$

- Minimization still done using gradient descent, with simultaneous updates to $\theta_j$
- The algorithm remains

  $\theta_j:=\theta_j-\alpha \frac{1}{m}\sum_{i=1}^m((h_\theta(x_i)-y_i)x_i)$

  but the definition of $h_\theta(x)$ has now changed.

- Vectorised implementation:

    $\theta = \theta - \frac{\alpha}{m} X^T (g(X\theta)-y)$

- A problem with gradient descent is the manaual selection of learning rate that's done. Algorithms such as **Conjugate Descent, BFGS and L-BFGS** do not have this problem owing to a dynamic learning rate calculated by a clever inner loop. Hence, they have faster convergence. The inner loops are fairly complex and understanding them is not easy.
- Implementation of advanced optimizaiton algorithms requires a specific structure to code it in Octave/MATLAB. Evaluation for $J(\theta)$ and $\frac{\delta}{\delta\theta_j}$:-

```MATLAB
function [jVal, gradient] = costFunction(theta)
  jVal = [...code to compute J(theta)...];
  gradient = [...code to compute derivative of J(theta)...];
end
```

- For the advanced optmisation function itself, the code should be structured as follows:

```MATLAB
options = optimset('GradObj', 'on', 'MaxIter', 100);
initialTheta = zeros(2,1);
   [optTheta, functionVal, exitFlag] = fminunc(@costFunction, initialTheta, options);
```

- In one-vs-all, train k parallel 2 class classifiers and then use a max function to take the classication that is the *most confident* about it's predictions.
- **Overfitting** is when an algorithm tries too hard to be accurate for the training set and ends up not being generalised enough to make accurate predictions.
- Ways to overcome overfitting:
    - Select features to keep.
    - Model selection algorithm.
    - Regularization.
- **Regularisation** is a technique to simplify cost functions by adding a term that *regularises* parameters.
- An example of a cost function with added regularization is as follows:
  
    $J(\theta)=\frac{1}{2m}[\sum_{i=1}^m(h_\theta(x^i)iy^i)^2+\lambda\sum_{j=1}^n\theta^2_j$

- If $\lambda$ is too big, then $\theta$ values are highly penalised and it fails to fit even basic test data. As $\theta$ values reduce close to zero, and what we get is $h_\theta(x)=\theta_o$
- **$\theta_o$ is not penalised in Regularisation.**
- Linear Regression update function with Regularisation:

    $\theta_j = \theta_j(1-\frac{\lambda}{m})-\frac{\deltaJ}{\delta\theta}$
    where J is the normal cost function.

- For the Normal form, expression for $\theta$ changes to:

    $\theta = (X^TX + \lambda\begin{matrix}0&0&..&0&0\\0&1&..&0&0\\.&.&.&.&.\\0&0&..&1&0\\0&0&..&0&1\end{matrix})^{-1}X^TY$
        
```
--------------
INCOMPLETE
--------------
```