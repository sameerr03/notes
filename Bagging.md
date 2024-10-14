Bagging or Bootstrap Aggregating is a meta algorithm designed to improve the stability and accuracy of machine learning algorithms used in statistical classification and regression. It decreases the variance and helps in avoiding [[Overfitting and regularization|overfitting]]. 

The process of bagging is as follows
1. Multiple subsets are created from the original data set with the same number of datapoints. These subsets are randomly sampled from the original data with replacement - some points may appear more than once in a subset and others may never appear. 
2. Base models is created on each of these subsets. 
3. The models are trained in parallel with each other, and are trained completely independently of each other. 
4. Once all the models are trained, their predictions are combined. In classification, this is done by voting. For regression it might be done through an average of all the numerical predictions. Mathematically, $$y(\textbf x)=\arg\max_{T}(T(\textbf x))$$ for classification tasks where $T$ is a part of the committee and $T(\textbf x)$ is the decision. For regression, $$y(\textbf x)=\frac 1M\sum_{m=1}^My_m(\textbf x)$$
#### Analysis of bagging
##### Regression
The error for each individual model is given by $$\mathbb E[\{y_m(\textbf x)-h\}^2]=\mathbb E[\epsilon_m(\textbf x)^2]$$where:
- $y_m$ is the model $m$
- $h$ is the true value
- $\epsilon_m$ is the error of the model

Therefore the average error is given by $$E_{AV}=\frac 1M\sum_{m=1}^M\mathbb E[\epsilon_m(\textbf x)^2]$$this is the average error of the models acting individually. Looking at the ensemble error$$E_{COM}=\mathbb E[\{\frac 1M\sum_{m=1}^My_m(\textbf x)-h\}^2]=\mathbb E[\{\frac 1M\sum_{m=1}^M\epsilon_m(\textbf x)\}^2]$$If we assume that the errors are distributed in a manner that they have 0 mean and are uncorrelated with each other between models, then after expanding the square terms and simplifying, $$E_{COM}=\frac{1}{M}E_{AV}$$