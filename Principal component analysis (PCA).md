PCA is an unsupervised [[Dimensionality reduction]] algorithm.

PCA defines a set of principal components. These are essentially linear combinations of the dimensions of the dataset. We define these principal components as 
- 1st: Direction of greatest variation in that direction (Linear combination of dimensions that explains the maximum variation in the dataset)
- 2nd: Orthogonal to the first PC. Explains the maximum variability of what's left
- .... and so on until $d$, which is the original dimensionality

These first $m<d$ PCs become the $m$ new dimensions. We then project every single datapoint from $d$ dimensions to $m$ dimensions. We do so by getting rid of the data along that PC. Since they explain minimal variation, we minimize the loss of data when reducing the dimensions. Basically minimizing the distances between original points and their lower dimension projections.

#### PCA process
1. Find the covariance matrix of the dataset, $D$ such that $$\Sigma=\begin{bmatrix}\text{var}(x_1)&\text{cov}(x_1,x_2) &\dots&\text{cov}(x_1,x_n)\\\text{cov}(x_2,x_1)&\text{var}(x_2)&\dots&\text{cov}(x_2,x_n)\\\vdots&\vdots&\ddots&\vdots\\\text{cov}(x_n,x_1)&\text{cov}(x_n,x_2)&\dots&\text{var}(x_n)\end{bmatrix}$$
	This is a square matrix that gives the covariance and between each pair of elements. this gives us the notion of variance in multiple dimensions. It is important that we de-mean the dataset first. We subtract the mean of each dimension from all the datapoints for each dimension, to center the dataset. This ensures that the first PC passes through the origin. 
1. Find the [[Eigenvector eigenvalue|eigenvalues]] and corresponding eigenvectors of the matrix$$\Sigma e=\lambda e$$The eigenvalues ($\lambda$) represent the amount of variance in the data along each PC, which is given by the eigenvectors ($e$). Larger eigenvalues indicate larger amount of variance along that principle component. 
2. Find the eigenvalues by solving $$\det (\Sigma-\lambda I)=0$$We then find the $i$th eigenvector by solving $$\Sigma e_i=\lambda_i e_i$$ which will give us the PCs.
3. Sort the eigenvectors by their corresponding eigenvalues in descending order. 
4. Choose the top $k$ eigenvectors where $k$ is the desired dimensionality of the reduced dataset
5. Project the original data to the PCs. For each observation $\textbf x = x_1,\dots, x_n$ we center the data, $\textbf x'=x_1-\mu_1,\dots, x_n-\mu_n$. We then can project the data to each PC using $$z_i=(\textbf x')^T\cdot e_i$$where $z_i$ is the coordinate of $\textbf x'$ in the direction of the $i$th principal component. We do this for $k$ eigenvectors (PCs) for all the datapoints in the dataset to get the new dataset. 


#### Choosing PCs
The scree plot plots the eigenvalues along the number of principal components. It tells you how much of the total variance is explained by each PC. We could also normalize the eigenvalues and see what fraction of the total variation each eigenvalue covers. ![[Pasted image 20241002195944.png]]
![[Pasted image 20241002195959.png]]
