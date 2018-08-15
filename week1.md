# Week 1

- Task, Performance measure, Experience.
- **Supervised Learning**: Correct answer is known. Told to us. eg. real estate price prediction regression, breast cancer classification problem. *Regression* and *Classification* are types of Supervised learning. 
- **Unsupervised Learning**: Correct answer not known, computer asked to find ‘*structure*’ in given data. Eg. Clustering of news articles. Not-clustering algorithms, such as the cocktail party problem. 
- Dr.Ng’s notations:- **m** for no. of training examples, **x** for input and **y** for output.
- Basic **Linear Regression**:
```
    Training Data
        |
        v
    Learning Algo
        |
        v
x-->hypothesis (h)--> y
```
- $h(x)=\theta_0+\theta_1x$
Equation for *Linear Regression*.

- The **Mean Squre Error** cost function is the most common **Cost Funciton** in Regression problems, for linear regression, the function is defined as follows:

    $J(\theta_0,\theta_1)=\frac{1}{2m}\sum_{i=1}^m (h_\theta(x^i)-y^i)^2$

- Be clear on the difference between the hypothesis function $h(x)$ and the cost function $J(\theta_0, \theta_1)$.
- [Contour plots](https://en.wikipedia.org/wiki/Contour_line) and minimization in 3D space done to handle cost function $J(\theta_0, \theta_1)$.
  
- **Gradient Descent** is an algorithm to minimize the cost function. General functions like $J(\theta_0,\theta_1,...,\theta_n)$ can also be minimized, not limited to linear regression.
- $\theta_j:=\theta_j-\alpha\frac{\delta}{\delta\theta_j}J(\theta_0,\theta_1)$ (for j=0,1)
is the basic equation for gradient descent. $\theta_j$ is updated with new values to reduce J. Here, $\alpha$ is the learning rate. Updates to $\theta_0$ and $\theta_1$ **should be simultaneous**. 
- In gradient descent, the **learning rate** should not be too high, else we entertain the risk of overshooting minimization and diverging. If learning rate is too low, then the algorithm would be slow.
- Linear Regression with Gradient Descent can be summarised as follows:  
  
  $\theta_0:=\theta_0-\alpha \frac{1}{m}\sum_{i=1}^m(h_\theta(x_i)-y_i)$  
  
  $\theta_1:=\theta_1-\alpha \frac{1}{m}\sum_{i=1}^m((h_\theta(x_i)-y_i)x_i)$

- These equations are derived by partial differentiation of $J(\theta_0,\theta_1)$ on $\theta_0$ and $\theta_1$.
- Method is called **Batch Gradient Descent** as entire batch of data looked at for next iteration.
- Although Gradient Descent looks at local minima, in linear regression problems, local minima is always the global minima, hence, gradient descent works just fine without any moderations.
- A **Vector** is a N x 1 Matrix, where N is the dimensions of the particular vector.
- **PREDICTION = DATA MATRIX * PARAMETERS**, take data fields as 1 each for additional dimensions of parameter. Multiple hypothesis can be tested as well in matrix-matrix multiplications.
- Matrices that do not have an inverse are called *Degenerate* or *Singular* matrices.

