Co variance matrix is used for finding out the test statistics in [[Inference]] testing. The matric is obtained from a [[Multiple variable regression]] by $$\sigma^2(X'X)^{-1}$$
where $X$ is the matrix of all values of $x_i$ in the regression. The matrix is of the form$$\begin{bmatrix}Var(\beta_0)&Cov(\beta_0,\beta_1)&Cov(\beta_0,\beta_2))\\Cov(\beta_1,\beta_0)&Var(\beta_1)&Cov(\beta_1,\beta_2)\\Cov(\beta_2,\beta_0)&Cov(\beta_2,\beta_1)&Var(\beta_2)
\end{bmatrix}$$ 

The variances lie along the diagnal with all possible covariances lying at the other positions. 