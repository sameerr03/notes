LDA or Normal Discriminant analysis is a [[Dimensionality reduction]] method used in supervised classification problems. 

LDA looks for directions in the feature space where data points from different classes are as far apart as possible and datapoints within the same class are as close to each other as possible. 

The steps in LDA are
1. Compute the means of each class (group) and the overall mean
2. Compute the scatter matrices to measure
	1. within class scatter - how much variance exists within each class (how spread out the datapoints in the same class are from the mean)
	2. Between class scatter - How far apart different class means are from each other
3. Maximize the between class scatter while minimizing the within class scatter. LDA goes about this by solving an optimization problem that finds the best direction to separate the classes.
4. Project the data onto these directions (called linear discriminants), which reduces dimensionality while keeping the individual classes as distinguishable as possible.

#### Fisher Criterion
The fisher criterion is used to measure how good a particular projection is. It is given by $$J(\mathbf w) = \frac{(m_1-m_2)^2}{s_1^2+s_2^2}$$Where:
- $\textbf w$ is the vector onto which the data is projected
- $(m_1-m_2)^2$ is the squared distance between the projected means of the two classes, larger this value better the projection
- $s_1^2+s_2^2$ represents the total within class scatter after projection. Smaller values mean the datapoints are closer to the means of the classes

#### Scatter matrices
The scatter matrix for a specific class is given by $$S_i=\sum_{x\in D_i}^n(x-m_i)(x-m_i)^T$$where:
 - $D_i$ is the dataset corresponding to class $i$, that is all the points that belong to that class
 - $x$ is a datapoint in class $i$ (vector)
 - $m_i$ is the mean vector for class $i$, which represents the average of all datapoints in that class$$m_i=\frac 1{n_i}\sum_{i=1}^{n_i}x_i$$where $n_i$ is the number of datapoints in class $i$ and $x_i$ is the datapoint that belongs to class $i$

The **within class scatter matrix** $S_W$ is given by $$S_W=\sum_{i=1}^cS_i$$where $c$ is the number of classes in the dataset. This is just the sum of the within class variation across all the classes

The **between class scatter matrix** is given by $$S_B=\sum_{i=1}^cN_i(m_i-m)(m_i-m)^T$$Where:
- $m$ is the mean vector of the entire dataset
- $m_i$ is the mean vector of the respective class 
- $N_i$ is the number of datapoints in $i$
- $c$ is the number of classes

The term $(m_i-m)(m_i-m)^T$ captures the variance of class $i$'s mean relative to the overall mean. This measures how far apart the mean is from the overall mean. 

#### Finding the LDs
To maximize the separation between classes, we want to optimize for the ratio of the between class scatter to the within class scatter. We want more between class scatter and less within class scatter. We find the projection vector $\textbf w$ by solving the [[Eigenvector eigenvalue|eigenvalue]] problem $$S_W^{-1}S_B\textbf w=\lambda \textbf w$$We want to find a projection $\textbf w$ that maximizes the ratio, which will correspond to the largest eigenvalue. This is our linear discriminant. we can then project the data onto the LDs. 

#### Projection onto the LD
We can project our original datapoint $x$ onto the LD using$$y=\textbf w^Tx$$this is the value of the datapoint in the new one dimensional space (for 2 classes, else C-1 dimension projection). Now that the dataset has been projected, we can classify the data based on threshold values given by the **discriminant function**$$\delta(x)=x(\sigma^2(\mu_0-\mu_1))-2\sigma^2(\mu_0^2-\mu_1^2)+\ln(\frac{P(\omega_0)}{P(\omega_1)})$$Where:
- $\delta(x)$ is the linear discriminant function that gives us a decision boundary
- $x$ is the input point
- $\mu_1, \mu_0$ are the means of the two classes in the reduced feature space
- $\sigma^2$: the common within class variance, which assumes that both classes share the same variance
- $P(\omega_0), P(\omega_1)$ are the prior probabilities of the two classes - the probability of an input point belonging to class 0 or 1. 

If $\delta(x)$ is positive, then $x$ is assigned to $\omega_0$ else $\omega_1$. 

#### Disadvantages of LDA
1. Assumes gaussian distribution of data
2. Assumes that the covariance matrices of different classes are equal
3. Assumes that the data is linearly separable
4. May not perform well in high dimensional feature spaces
