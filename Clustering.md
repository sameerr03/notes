Clustering groups points in $n$ dimensional spaces using the concept of similarity. Similarity can be measured using 
- Euclidian Distance: The squared difference in each dimension. 2d euclidian distance is $$d=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2}$$
- Categorical distance: $d=0$ if the category is the same, else $d=1$
- Cosine similarity: Similarity based on the angle between the datapoints formed at the origin. Given by $$\text{cosine similarity}=\cos \theta=\frac{A\cdot B}{||A||||B||}=\frac{\sum_{i=1}^nA_iB_i}{\sqrt{\sum_{i=1}^nA_i^2}\sqrt{\sum_{i=1}^nB_i^2}}$$This is used for measuring text similarity. If the theta is high/ cos theta is low similarity is low. 

#### Types of clustering algorithms
- Centroid based: Forms centroids of the datapoints and clusters based on this
- Distribution based: Clustering modelled using statistical distributions. Assumes that datapoints are generated from a probability distribution and the algorithms attempts to parameterize this distribution to group similar points into clusters
- Density based: Groups together datapoints in high density concentration and separates points in low concentration regions. Groups points in dataspace that have a high density of points
- Hierarchical: Creates clusters incrementally. Types are 
	1. Agglomerative (bottom up) - Merges two points that are most similar and forms a cluster, adds points until all points have been merged into a single cluster
	2. Divisive (Top down) - Starts with all points belonging to one cluster and splits the least similar clusters until only single datapoints remain
	![[Pasted image 20241003002344.png]]Decisions to join/split are made on how the clusters are linked - Single (shortest distance between closest points of different clusters), Complete (max distance between points of 2 different clusters), Centroid (Distance between centroids of the clusters), Average (Average of all pair distance between points of both clusters)

#### k means clustering
The algorithm for $k$ means clustering is as follows
1. Assume a value for the number of clusters, $k$
2. Start with a random set of points acting as the cluster centers
3. Assign all remaining points to clusters based on distance to the cluster centers
4. Recompute the centers as centroids of the groups
5. Repeat till convergence (centroids stop changing)

The algorithm iterates between two steps, the assignment step where datapoints are assigned to clusters$$S_i^{(t)}=\{x_p:||x_p-m_i^{(t)}||^2\le||x_p-m_j^{(t)}||^2\ \forall j,1\le j\le k\}$$This finds the distance of the point from all centroids, and each datapoint is assigned exactly to one cluster. (the cluster is a set). 

The update step changes the value of the centroids$$m_i^{(t+1)}=\frac 1{|S_i^{(t)}|}\sum_{x_j\in S_i^{(t)}}x_j$$where the term in the denominator is the cardinality of the cluster. It basically calculates the mean of all the points in the cluster and updates the center of the cluster based on that 

For an assumed value of $k$, we stop when a local minima is reached, which is characterized as a point where the distance of each point from its respective cluster center is minimized (Within cluster sum of squares)$$\text{WCSS} = \arg\min_S\sum_{i=1}^k\sum_{x_i\in S_i}||x_i-\mu||^2$$The total distance not changing means we reached a stopping criterion. However, the algorithm is not guaranteed to find the best solution.

##### Choosing the value of k
This is done by iterating through the number of clusters from 2 to $n-1$. For each value of $k$ we calculate the WCSS and plot the WCSS value against k value. The higher $k$, the larger the number of clusters and WCSS will be lower. We can find the **elbow point**, where with each subsequent increase in the number of clusters from that point, there is minimal decrease in WCSS. This is the optimal number of clusters
![[Pasted image 20241003003953.png]]

#### Gaussian Mixture Model (GMM)
GMM is an expectation maximization algorithm. It represents a distribution as $$p(\textbf x)=\sum_{k=1}^K\pi_kN(\textbf x|\mu_k, \Sigma_k)$$Where:
- $p(\textbf x)$ is the probability density function of the overall mixture model
- $\Sigma_k$ is the covariance matrix of the $k$th gaussian
- $\mu_k$ is the covariance matrix of the kth gaussian
- $\pi_k$ is the mixing coefficient, where $$\sum_{k=1}^K\pi_k=1\ \text{and}\ \pi_k\ge0\ \forall k$$
GMMs are density estimators. They can combine multiple distributions with different weights to produce a more complex, flexible distribution, but this model is harder to optimize. The Maximum likelihood is given by the max of$$\ln p(\textbf X|\pi,\mu,\Sigma)=\sum_{n=1}^N\ln(\sum_{k=1}^K\pi_kN(\textbf x^{(n)}|\mu_k, \Sigma_k))$$Where:
- $N(\textbf x^{(n)}|\mu_k, \Sigma_k)$ represents the probability density of the nth datapoint under the kth gaussian component with the mean and variance as given

the function sums the log probabilities of the datapoint existing in each of the k gaussians. We weight the probabilities using the mixing coefficients. This sum represents the total probability of observing that datapoint under our entire mixture model. We then sum that up over every datapoint. We maximize the likelihood function with respect to $\Theta=\{\pi_k, \mu_k, \Sigma_k\}$

A latent variable is not directly observed but can can be inferred from data. If the variable $z$ follows a categorical distribution with parameters $\pi$, where $\pi_k\ge 0, \sum_k\pi_k=1$ then $$p(\textbf x)=\sum_{k=1}^Kp(\textbf x,z =k)=\sum_{k=1}^Kp(z=k)p(\textbf x|z=k)$$This is the probability that the latent variable takes a specific value, times the probability of observing x given that value of z. z represents which gaussian component the datapoint came from. With this, the log likelihood becomes$$\ln p(\textbf X|\pi, \mu, \Sigma)=\sum_{n=1}^N\ln p(\textbf x^{(n)}|\pi, \mu,\Sigma) = \sum_{n=1}^N\ln\sum_{z^{(n)}=1}^Kp(\textbf x^{(n)}|z^{(n)};\mu,\Sigma)p(z^{(n)}|\pi)$$
If we knew $z^{(n)}$ for every $x^{(n)}$, the maximum likelihood problem is easy. The likelihood function is $$\ln p(\textbf X|\pi, \mu, \Sigma)=\sum_{n=1}^N\ln p(\textbf x^{(n)}|z^{(n)};\mu,\Sigma)+\ln p(z^{(n)}|\pi)$$maximizing, we get$$\mu_k=\frac{\sum_{n=1}^N1_{[z^{(n)}=k]}\textbf x^{(n)}}{\sum_{n=1}^N1_{[z^{(n)}=k]}}$$$$\Sigma_k=\frac{\sum_{n=1}^N1_{[z^{(n)}=k]}(\textbf x^{(n)}-\mu_k)(\textbf x^{(n)}-\mu_k)^T}{\sum_{n=1}^N1_{[z^{(n)}=k]}}$$$$\pi_k=\frac 1N\sum_{n=1}^N1_{[z^{(n)}=k]}$$
To fit the model, 
1. Initialize $\mu_k, \Sigma_k, \pi_k$ and evaluate the initial log likelihood 
2. E step: Compute the posterior probability over $z$ given the current model. How much do we think each gaussian generates each datapoint$$\gamma(z_{nk})=\frac{\pi_kN(\textbf x_n|\mu_k, \Sigma_k)}{\sum_{j=1}^K\pi_kN(\textbf x_n|\mu_k, \Sigma_k)}$$gamma is not the probability, but is the responsibility. It represents the probability that the nth datapoint was generated by the kth gaussian given our current model parameters.
3. M step: Assuming that the data was generated this way, change the parameters of each gaussian to maximize the probability that it would generate the data. Uses the equations above
4. Re evaluate the log likelihood. Check for convergence of the parameters or the log likelihood. If no convergence, return to step 2

#### DBSCAN
DBSCAN is a density based clustering algorithm. For each point of a cluster, the neighborhood of a given radius has to contain at least a minimum number of points. The params are Eps that defines the neighborhood and MinPts that determine the minimum number of points with the Eps radius. MinPts has to be large for larger datasets. 
![[Pasted image 20241003012204.png]]

Process
1. For each point, find all neighbors within eps
2. Identify core points with more than minpts neigbors - mark as visited
3. For each core point if it is not already assigned to a cluster, create a new cluster
4. Find recursively all its density connected points and assign them to the same cluster as a core point. Two points are density connected if there exists a third point whihc has sufficient number of points in its neighbors and both the initial points are within the eps distance of the third process
5. Iterate through remaining unvisited points. Points that do not belong to any clusters are noise.

#### Measuring cluster quality
Good clustering should minimize intracluster distance and maximize intercluster distance We can use Silhouette score for this. $$S(i)=\frac{b(i)-a(i)}{\max\{a(i),b(i)\}}$$Where:
- $a(i)$ is the average distance of point $i$ from all other points in its own cluster. (intra cluster distance)\
- $b(i)$ is the smallest average distance of $i$ to all points in any other cluster (inter cluster distance of i wrt all other cluster)

increase in intra cluster distance or decrease in intercluster distance gives lower scores. 