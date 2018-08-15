# Week 2

- In **Multivariate Linear Regression**, n denotes the number of features, multiple features are used for prediction. The hypothesis function changes to: 
  $h\theta(x)=\theta_0+\theta_1 x_1+\theta_2 x_2+...+\theta_n x_n$
- In $x^j_i$, j is the row of different features, while i is the specific feature in a row of different features.
- Addition $x_0=1$ defined to make features 0 indexed. Then $X = [x_0,x_1,...,x_n]$ and $\theta=[\theta_0,\theta_1,...,\theta_n]$. Both are 0 indexed. Then, our hypothesis becomes: 
  $h(x)=\theta^T X$ , both are (n+1) x 1 
- Gradient Descent for Multivariate Linear Regression: 
  $\theta_j := \theta_j - \frac{1}{2m} \sum^m+i=1 (h_\theta(x^i) - y^i)x^i_j$
- When features are very differently scaled, as in, Area of House (in 0-2000 Sq.ft.) and Number of Bedrooms(1-5), the contour can be extremely skinny, tall and elliptical. Gradient descent has problems on such a contour, as it oscillates back and forth, taking a lot of time. We do **Feature Scaling** to overcome this. Here, Area will be taken as value/2000 and bedrooms as N/5.
- The goal of *Feature Scaling* is to bring all features in *approximately* the same range of values (**-1 to 1**). As a general rule of thumb, values form -3 to 3 and -1/3 to 1/3 are fine, smaller or bigger and we need to scale.
- **Mean Normalization** implies adjusting features such that the mean of values is roughly 0. $x_i-\mu$ for all values is the general method.
- Feature scaling does not have to be too exact and generally done as :
  $x_i := \frac{x_i - \mu_i}{S_i}$ where $S_i$ is the range of $x_i$.
