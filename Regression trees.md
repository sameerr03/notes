A regression tree is a [[Decision tree classifier|decision tree]] that is used to predict continuous values. 

#### Single variable regression tree
We use mean square error to find the optimal partitions in the dataset. Suppose we have input variable vector $X$ and output variable vector $Y$. In order to create a regression tree, the $X$ series is sorted, and partitioned using the threshold $\tau$. $X_A = X_i<\tau\ \forall X_i\in X$. Thus we get $X_A$ and $X_B$ (all $x$ greater than $\tau$). Using this partition, we can get $Y_A$ and $Y_B$. Using these partitioned sets, we can find the predicted $Y$ for a partition, which is just the average of all $Y_i$ values in that partition

$$\hat Y_A=\frac 1{n_A}(Y_{1A}+Y_{2A}+\dots)$$This is the predicted value of $Y$ for all $X_i$ values in $A$ ($X_i<\tau$)

We find the prediction $\hat Y_i$ for each value of $X_i$ in $X$. If there are $n$ values totally, the mean square error is given by $$\text{MSE}=\frac 1n\sum^n(Y_i-\hat Y_i)^2$$
We then change $\tau$ in order to minimize the MSE. $$\min_{\tau}\text{MSE}$$
#### Multivariate regression tree
1. Data is sorted based on each variable separately
2. Steps are repeated for each variable to find the best split point for each variable
3. The variable that produces the split with the lowest MSE is the first decision variable. This process is repeated for other variables until the best generalization error is achieved. 