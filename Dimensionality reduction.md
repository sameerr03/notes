Some features (Dimensions) in a dataset bear little information or bear information that is not useful. Such dimensions can be dropped from the dataset. On the other hand, many features can be combined together without a loss of information.

There are two methods with which we can go about dimensionality retuction
1. Feature selection: Choosing $k<d$ important features and ignoring the remaining $d-k$, eg: Impurity Measure
2. Feature extraction: Project the original $x_i, i=1,\dots, d$ dimensions to new $k<d$ dimensions $z_j, j=1,\dots,k$. eg: [[Principal component analysis (PCA)]], [[Linear discriminant analysis (LDA)]], Factor Analysis (FA)

