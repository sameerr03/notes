Makes predictions by following a tree like structure, taking decisions at each node. We can make our predictions more efficient by more carefully deciding the order of nodes (order of decisions). When working with continuous variables, we need to discretize them. We can make decisions based on the discretized buckets (annual income greater or less than equal to threshold $T$, we choose $T$ that maximizes information gain). The model also tends to struggle with determining decision criteria when the optimal method of choosing data is by using multiple attributes at once (either numerically $x+y<3$ or with multiple categorical variables).

![[Pasted image 20240911225233.png]]

In order to determine how to split the tree, we can use the following measures of impurity:$$\text{Entropy} = -\sum_{i=0}^{c-1}p_i(t)\log_2p_i(t)$$
Where:
- $c$ is the number of classes
- $p_i(t)$ is the probability of class $i$ at node $t$. It represents the proportion of data points in class $i$ at that node. 
Entropy is analogous to how much more information is required. It measures uncertainty with higher entropy meaning more impurity
$$\text{Gini Index}=1-\sum_{i=0}^{c-1}p_i(t)^2$$
A pure node will have a 0 on the gini index and a 0 entropy. This focuses on squared probabilities, it is computationally simpler than entropy, while having a similar effect
$$\text{Classification Error}=1-\max_i[p_i(t)]$$This looks at the probability of the majority class. A pure node has a 0 classification error. It focuses on the proportions of misclassifications. 

#### Splitting the tree
At each node in the tree, the algorithm determines the best method of splitting the dataset using the impurity measures. It then selects the split of data that maximizes the reduction in the impurity. We thus want to find the impurity of all the children based on how we split the dataset. This is given by $$I(\text{children})=\sum_{j=1}^k\frac{N(v_j)}{N}I(v_j)$$where $N(v_j)$ is the number of training instances associated with the child node $v_j$, $N$ is the total number of instances and $I(v_j)$ is the impurity of the child node. We want to maximize the information gain (reduction in impurity). This is given by $$\Delta=I(\text{parent})-I(\text{children})$$The larger the difference, the better the splitting condition. 


### Gain Ratio
using information gain to split the tree is biased towards splitting according to more variables according to each node (ID would be a good example) - this will give us great performance in training data but very poor out of sample performance. 

We can use the gain ratio to counter this bias by normalizing the information gain by adjusting for the number of splits that those attributes will create. This is in the split information term. 
$$\text{Gain Ratio} = \frac{\Delta_{\text{info}}}{\text{Split Info}}=\frac{\text{Entropy}(\text{Parent})-\sum_{i=1}^k\frac{N(v_i)}{v_i}\text{Entropy}(v_i)}{-\sum_{i=1}^k\frac{N(v_i)}N\log_2\frac{N(v_i)}{N}}$$
The split info is essentially the entropy of the distribution of the training data among the child nodes based on the split attribute.
#### Example
**Problem:**  
We have a dataset of 6 fruits. Each fruit is classified as either **Apple** or **Orange**, based on two features: **Color** (Red/Orange) and **Size** (Small/Large).

**Dataset:**

|Fruit ID|Color|Size|Class|
|---|---|---|---|
|1|Red|Large|Apple|
|2|Red|Small|Apple|
|3|Orange|Large|Orange|
|4|Orange|Small|Orange|
|5|Red|Small|Apple|
|6|Orange|Large|Orange|

**Step 1: Initial Impurity at the Root Node (Using Gini Index)**  
At the root node, we calculate the Gini Index. There are 3 apples and 3 oranges.
![[Pasted image 20240911233134.png]]
**Step 2: Splitting by "Color"**  
We now split the data based on the feature **Color** (Red or Orange).

- **Left Node (Color = Red):**

|Fruit ID|Color|Size|Class|
|---|---|---|---|
|1|Red|Large|Apple|
|2|Red|Small|Apple|
|5|Red|Small|Apple|

There are 3 apples and 0 oranges in this group. The node is pure (all apples), so the Gini Index is:

![[Pasted image 20240911233207.png|200]]

- **Right Node (Color = Orange):**

|Fruit ID|Color|Size|Class|
|---|---|---|---|
|3|Orange|Large|Orange|
|4|Orange|Small|Orange|
|6|Orange|Large|Orange|

There are 3 oranges and 0 apples in this group. The node is pure (all oranges), so the Gini Index is:
![[Pasted image 20240911233241.png|200]]

**Step 3: Information Gain from the Split**  
Since both resulting nodes are pure, the Gini Index at these child nodes is 0, and the **total weighted Gini** after the split becomes:
![[Pasted image 20240911233305.png|300]]
The **Information Gain** is the reduction in Gini Index from the root node:
![[Pasted image 20240911233333.png|400]]

![[Pasted image 20240911233359.png]]

This is the final decision tree.

#### Model Selection
We want to select the model that shows the lowest generalization error rate. To do this, we can use a **validation set** of data. This data is not used for training, which means that the data has never been seen by the model before. This can give us an estimate of the generalization error rate, and we can select a model based on the best performance on the validation set. 

$$\text{Gen. Error Rate}(m)=\text{Train Error}(m, D.\text{train})+\alpha\times\text{complexity}(M)$$Where:
- $M$ is the set of all possible decision trees
- $m$ is a specific model corresponding to the decision tree learnt

Given 2 models with the same error, the simpler model will be preferred to the more complex model.

#### Complexity of a decision tree
Ratio of the number of leaf nodes to the number of training instances$$\text{err}_g(T)=\text{err}(T)+\Omega\frac{k}{N_\text{train}}$$Where $\Omega$ is a hyperparameter that makes a trade off between reducing training error and minimizing model complexity. It can be thought of as the cost of adding a leaf node to the tree. $T$ is the decision tree according to the training data. This formula will prevent overfitting.  