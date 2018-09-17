# Week 4

- Logistic Regression is useful when the number of features is relatively low, but in real  life scenarios, where no. of features is large, Logistic regression becomes impractical owing to the large no. of features even if just the quadratic terms are taken. **Neural Network** solves this issue.
- **Activation Function** is a Neural Net terminology for function used to calculate output for a given instance of input.
- $X_o$ is called the **Bias Unit**.
- A neural network comprises of layers, there's the **Input Layer**, a few **Hidden Layers** and an **Output Layer**.
- If a network has $s_j$ units in layer $j$, $s_{j+1}$ units in layer $j+1$, then $\theta^{(j)}$ will be of dimension $s_{j+1} X (s_j+1)$.
- A structural breakdown of $\theta$ for a 3 layer neural network:  

![Image from Course](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/0rgjYLDeEeajLxLfjQiSjg_0c07c56839f8d6e8d7b0d09acedc88fd_Screenshot-2016-11-22-10.08.51.png?expiry=1537315200000&hmac=6z3E-CmCHRvVCIppE1J6PlPs6Wrywa933_fmxQHaaHA "Week 4, Andrew Ng : Machine Learning")