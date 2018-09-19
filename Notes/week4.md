# Week 4

- Logistic Regression is useful when the number of features is relatively low, but in real  life scenarios, where no. of features is large, Logistic regression becomes impractical owing to the large no. of features even if just the quadratic terms are taken. **Neural Network** solves this issue.
- **Activation Function** is a Neural Net terminology for function used to calculate output for a given instance of input.
- $X_o$ is called the **Bias Unit**.
- A neural network comprises of layers, there's the **Input Layer**, a few **Hidden Layers** and an **Output Layer**.
- If a network has $s_j$ units in layer $j$, $s_{j+1}$ units in layer $j+1$, then $\theta^{(j)}$ will be of dimension $s_{j+1} X (s_j+1)$.
- A structural breakdown of $\theta$ for a 3 layer neural network:  

![Image from Course](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/0rgjYLDeEeajLxLfjQiSjg_0c07c56839f8d6e8d7b0d09acedc88fd_Screenshot-2016-11-22-10.08.51.png?expiry=1537315200000&hmac=6z3E-CmCHRvVCIppE1J6PlPs6Wrywa933_fmxQHaaHA "Week 4, Andrew Ng : Machine Learning")  

- **Forward Propagation** is a process used to compute values in a neural network, by defining a new term $z$. Neural network *learns it's own features* n number of times, where n is the number of layers in the neural network.
- So, with $x = a^{(1)}$,  

    $z^{(j)}=\theta^{(j-1)}a^{(j-1)}$  
    where, $a^{(j)}=g(z^{(j)})$

- **Neural Network Architecture** is how the layers are interconnected in a neural netowrk.
- The neural network can be used to compute $x1$ AND/OR $x2$ as simple examples, while more complicated calculations can also yeild XOR, XNOR among others. For example:

![Image from Coursera](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/f_ueJLGnEea3qApInhZCFg_a5ff8edc62c9a09900eae075e8502e34_Screenshot-2016-11-23-10.03.48.png?expiry=1537488000000&hmac=aQ67zWqUi_R-OxW9L76urv9lWLy8cMpBqNQz-EEYQbo)

- If we change $\theta_o$ to -30 here, the execution becomes AND.
- Drawing truth tables are useful for determination.
- For negation, put a large negative weight in front of the value that's to be negated.
- XNOR can be implemented in a 3 layer structure with:
    ```
     Layer 1                 Layer 2                      Layer3
    |--------|     |------------------------------|      |-------|  
    (x1 , x2) ---> (x1 AND x2 ) (NOT x1 AND NOT x2) ---> x1 OR x2 ---> h(x)
    ```
![Image from Coursera](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/rag_zbGqEeaSmhJaoV5QvA_52c04a987dcb692da8979a2198f3d8d7_Screenshot-2016-11-23-10.28.41.png?expiry=1537488000000&hmac=gzBukxoG8NDGN8cRZLnFZKinWs2LmQV5iKkreiSHR9A)

- For **Multi-Class Classification**, we take the approach as summarised in the following picture:

![Image from Coursera](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/9Aeo6bGtEea4MxKdJPaTxA_4febc7ec9ac9dd0e4309bd1778171d36_Screenshot-2016-11-23-10.49.05.png?expiry=1537488000000&hmac=pHVoBTthFEMhTu8RoT13rQUlpcLfQf6dLfePXgKE9VQ)
```
----------
INCOMPLETE
----------
```