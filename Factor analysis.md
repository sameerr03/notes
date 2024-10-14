We model the observed variables as linear combinations of some underlying latent variables called factors, along with some random noise. Mathematically, we represent it as $$x_i-\mu_i=v_{1i}z_i+v_{i2}z_2+\dots+v_{ik}z_k+\epsilon_i$$where:
- $z_i$ are the factors such that $\mathbb E(z_i)=0, \text{var}(z_i)=1, \text{cov}(z_i,z_j)=0, i\ne j$
- $\epsilon$ represents the noise. This is such that $\mathbb E(\epsilon_i)=\Psi_i, \text{cov}(\epsilon_i,\epsilon_j)=0, \text{cov}(\epsilon_i,z_j)=0,, i\ne j$. 
- $v_{ij}$ are what is called the factor loadings. 

Representing it using matrices, $$\textbf x-\mu=\textbf V\textbf z+\epsilon$$
FA tires to identify a small number of latent factors that can explain the correlation of co-variation between observed variables. These latent factors are unobservable but inferred from data. By finding the small number of factors, we are reducing the dimensions. 

We find $\textbf V$ such that $$\textbf S=\textbf V\textbf V^T+\Psi$$where $\textbf S$ is the estimation of the covariance matrix of all the observed variables. $\textbf V$ is a $d\times k$ matrix where $d$ is the number of dimensions and $k$ is the number of factors. In order to find the factor loadings, we use [[Eigenvector eigenvalue]] based solution:
$$Z=XV=XS^{-1}V$$Where $Z$ is the projection using factors, which are obtained from a transformation of $X$ using the loading matrix. This gives us a projection of $X$ in the reduced dimension