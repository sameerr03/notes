Probabilistic machine learning [[Classification]] model. It is naive because it makes the assumption of independence among all the observations in the attribute set $X$, which need not be true depending on the dataset. We can set up the classification problem using [[bayes' theorem]].
$$P(C_k|X)=\frac{P(X|C_k)\cdot P(C_k)}{P(X)}$$where:
- $P(C_k|X$) is the probability that an instance $X$ belongs to the class $C_k$.
- $P(X|C_k)$ is the probability of observing $X$ given that it belongs to class $C_k$
- $P(C_k)$ is the prior probability of class $C_k$
- $P(X)$ is the probability of observing instance $X$, which will be the same irrespective of the class that we are running this calculation for. 

Based on the assumption of independence of attributes, we can say that $$P(X|C_k)=P(x_1|C_k)\cdot P(x_2|C_k)\dots P(x_n|C_k)$$From the bayes theorem, we can then say that $$P(C_k|X)\cdot P(X)=P(x_1|C_k)\cdot P(x_2|C_k)\dots P(x_n|C_k)\cdot P(C_k)$$We don't know $P(X)$ however. We can get around this by taking the ratio of the probabilities and making a decision based on this, cancelling out $P(X)$. If there are 2 classes, 1 and 0, we can say $$P_r=\frac{P(C_1|X)\cdot P(X)}{P(C_0|X)\cdot P(X)}=\frac{P(C_1|X)}{P(C_0|X)}$$If $P_r$ is greater than 1, then we say that the datapoint with attribute set $X$ belongs to class 1, else 0. 

#### Multiclass classification
We represent the problem as $$\text{Predicted Class}=\arg\max_{k}P(C_k|X)$$Substituting in bayes theorem, $$\text{Predicted Class}=\arg\max_{k}\ [P(X|C_k)\cdot P(C_k)]$$Since we are comparing using argmax, the $P(X)$ acts just as a scaling factor, and therefore cancels out. This leaves us with the most likely class according to the naive bayes classifier in a multiclass system. 

#### Laplacian Smoothing
Laplacian smoothing is used to deal with the problem of a particular attribute not appearing once within a class. If attribute $x_a$ never appears in the dataset in class $C_k$, then the probability $P(x_a|C_k)$ is 0 and since this classifier relies on multiplicative probability, the posterior probability $P(C_k|X)$ becomes 0. In order to get around this, $$P(x_a|C_k)=\frac{N(x_a,C_k)+1}{N(C_k)+|X|}$$where
- $N(x_a,C_k)$ is the number of times the feature/attribute $x_a$ appears in $C_k$ in the training data
- $N(C_k)$ is the total number of instances in class $C_k$
- $|X|$ is the total number of possible values for the feature $x_a$ (cardinality of set of attribute values)

