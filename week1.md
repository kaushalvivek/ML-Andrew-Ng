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
    $h(x)=\theta_0+\theta_1x$
    Equation for *Linear Regression*.

- The **Mean Squre Error** cost function is the most common **Cost Funciton** in Regression problems, for linear regression, the function is defined as follows:

    $J(\theta_0,\theta_1)=\frac{1}{2m}\sum_{i=1}^m (h_\theta(x^i)-y^i)^2$




