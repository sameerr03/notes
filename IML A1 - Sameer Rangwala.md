## Part 1 - Regression
[github repo](https://github.com/sameerr03/regression_task)
### Introduction
In this assignment, we had to create a regression model to predict fuel consumption of cars of different types from the provided features. In the training dataset, we are provided with the following information: Year, Make, Model, Vehicle class, Engine Size, Number of Cylinders, Transmission type, Fuel Type, Fuel Consumption, CO emissions. 

In order to complete this task, i made a multiple linear regression model that uses a few of these features, trained on the given fuel_train.csv dataset to predict Fuel consumption information. 

### Methodology
In order to build and train this model, I built a model to optimize the linear regression parameters to minimize the sum of the square of error terms. If we are using $p$ features from the dataset which is $n$ datapoints in size, the matrix $X\in \mathbb R^{n\times p+1}$ is our feature matrix that has $n$ rows and $p+1$ columns. The vector $\beta\in \mathbb R^{p+1}$ contains all the parameters that we need to set in the model. $Y, \epsilon \in \mathbb R^{n}$ are the vectors of the target variable (fuel consumption) and the residuals (difference between predicted and actual fuel consumption). The model is given as $$y_i=\beta_0+\beta_1x_{1i}+\beta_2x_{2i}+\dots+\beta_px_{pi}+\epsilon_i$$Representing the model using matrix notation, $$Y=X\beta+\epsilon$$In order to find the optimal value of $\beta$, we need to minimize the sum of square residuals$$\min_\beta (Y-X\beta)^2$$Taking the derivative with respect to $\beta$, we get$$\frac \partial {\partial\beta}((Y-X\beta)^T(Y-X\beta))=-2X(Y-X\beta)$$To minimize, we set this value to zero, $$-2X(Y-X\beta)=0$$$$-2X^TY+2X^TX\beta=0$$$$X^TX\beta=X^TY$$Therefore, the optimal values of $\beta$ that minimize the sum of square residuals is given by $$\beta^*=(X^TX)^{-1}X^TY$$This solution is implemented using numpy's linear algebra operations. 

### Experimentation
##### Pre-model observations and data preprocessing
Before building out the model, using libraries like matplotlib and seaborn, I tried to get some understanding of the dataset. Plotting scatterplots between the individual numerical features and fuel consumption, 
![[Pasted image 20240927021617.png|500]]
CO emissions appears to be the closest related to fuel consumption. Further, looking at the correlation matrix, we find that Engine size, cylinders , fuel consumption and co emission are all highly correlated with each other. Using more than one of these variables may result in multicolinearity issues. 
![[Pasted image 20240927022155.png]]
This boxplot shows the distribution of fuel consumption according to emissions. This could be a promising variable for prediction, but we need to convert it from categorical to many binary variables. 

Before model training, we performed the following preprocessing steps:

1. Handled missing values by removing rows with any null values.
2. Encoded categorical variables (Vehicle Class) using dummy variables.
3. Combined similar vehicle classes to reduce the number of dummy variables.

##### Model 1
We use the simple model with CO emissions as a first step. The regression equation is $$y_i=\beta_0+\beta_1\text{CO emissions}_{i}+\epsilon_i$$
##### Model 2
To ideally improve the simple model, we can try using vehicle class to give the model more features. We first combine a few of the classes, in order to reduce the total number of binary variables necessary. Compact and Subcompact are combined into Small Car, Passenger and cargo vans into Vans, Small and mid-size station wagons into Station wagon, Standard and small pickup trucks into pickup trucks, minicompact and two seater into very small car. We then use these new categories to create 9 total variables in our regression equation $$y_i=\beta_0+\beta_1\text{CO emissions}_i+\beta_2\text{VC Small car}_i+\dots+\beta_{9}\text{VC van}+\epsilon_i$$
##### Model 3
To test if this model can be improved further, we could drop some of the dummy variables that not statistically significant (their coefficient $\beta$ is not statistically different from zero). This is for two classes - minivans and very small cars. Therefore our simpler model becomes$$y_i=\beta_0+\beta_1\text{CO emissions}_i+\beta_2\text{VC Small car}_i+\dots+\beta_{7}\text{VC van}+\epsilon_i$$
### Results

| Metric | Model 1 | Model 2 | Model 3 |
| ------ | ------- | ------- | ------- |
| MSE    | 0.3853  | **0.2824**  | 0.2861  |
| RMSE   | 0.6207  | **0.5314**  | 0.5349  |
| R^2    | 0.9614  | **0.9717**  | 0.9714  |

Based on the training data, Model 2 achieves the best performance across all metrics. Even when adjusting the R-squared for the additional loss of degrees of freedom in Model 2 (due to a larger number of features) using Adjusted R-squared, Model 2 still shows the best in-sample performance.

Model 2 likely performs better because it incorporates both the strong linear relationship between CO emissions and fuel consumption, as well as the categorical information from vehicle classes, which can capture some non-linear aspects of the relationship.


### Challenges
1. Dealing with multicollinearity among features, which required careful feature selection.
2. Balancing model complexity with performance, as seen in the trade-off between Models 2 and 3.
3. Encoding categorical variables effectively without creating too many dummy variables.
4. Lack of enough datapoints for categorical variables (Eg: Fuel type 'E'), which upon inclusion could overfit the model to the training data resulting in poor test predictions

## Part 2 - Decision tree classifier
[github repo](https://github.com/sameerr03/decision_tree_task)
### Introduction
In this assignment, we have to create a decision tree classifier to detect and predict fraudulent transactions from the provided dataset, which includes information on transaction type, account balances of origin and destination before and after the transaction, and whether the transaction is fraudulent or not. 

To complete this task, I wrote a recursive algorithm to train a decision tree classifier that can use either continuous or binary variables to split data and make a prediction of whether a transaction is fraudulent or not.

### Methodology
The decision tree classifier used here recursively splits the data based on the feature and threshold that provides the best information gain (calculated using weighted gini) at each step. The key components of the implementation are:

1. **Node Class**: Represents a node in the decision tree, containing information about the splitting feature, threshold, child nodes, and predicted value for leaf nodes.
2. **DecisionTreeClassifier Class**: The main class that builds and uses the decision tree. Key methods include:
    - `fit`: Builds the tree recursively.
    - `_grow_tree`: Recursively grows the tree by finding the best split at each node.
    - `_best_split`: Finds the best feature and threshold to split on at a given node. For continuous variables, the thresholds is found by trying deciles of the range of the data. For binary variables that are either 1 or 0, the threshold is simply set to 0.5
    - `_information_gain`: Calculates the information gain for a potential split.
    - `_gini`: Calculates the weighted gini impurity of a node.
    - `predict`: Makes predictions on new data by traversing the tree.
3. **Splitting Criteria**: The model uses the Gini impurity as the splitting criterion. For a node with probability $p_i$ of an item being of class $i$, the Gini impurity is calculated as: $$\text{Gini} = 1 - \sum_{i=0}^Nw_i(p_i^2)$$The weight gives us another hyperparameter that results in the model paying more attention to class 1 (isFraud), since the dataset is heavily skewed towards very few positive isFraud cases, so a naive model that predicts 0 can still get high equal weight gini. 
4. **Best Split Selection**: For each feature, the algorithm considers multiple potential split points and selects the one that maximizes the information gain: $$\text{Information Gain} = \text{Gini}(\text{parent}) - (w_\text{left} * \text{Gini}(\text{left}) + w_\text{right} * \text{Gini}(\text{right}))$$ where $w_\text{left}$ and $w_\text{right}$ are the proportions of samples going to the left and right child nodes respectively.
### Experimentation
##### Pre model observations and data preprocessing
From the preliminary data analysis, we find that only certain classes contain fraudulent transactions, namely -transfers and cash withdrawals. ![[Pasted image 20240928141032.png|600]]
We can use this information to create a new feature from transaction type in the dataset: 1 if the transaction type is either CASH_OUT or TRANSFER, 0 otherwise. 

We can also consider cases where the Amount column value is equal to the Old Origin balance. This means that the entire amount of money in the origin account is set to be transacted. It is likely that in fraudulent transaction, the entire account is transferred/liquidated. Looking at the proportion of data in this case, ![[fraud_distribution.png]]We see that the vast majority of transactions using the entire initial account balance are fraudulent. This is another important feature that we can add to the model in the preprocessing step, 1 if the amount == OldBalanceOrig. 

##### Model 1: Basic Decision Tree

For the first model, I implemented a basic decision tree with the following parameters:

- Maximum depth (dmax): None (allow the tree to grow until pure leaves or minimum samples are reached)
- Minimum samples per leaf (minsamp): 2
- Features used: All preprocessed features

##### Model 2: Weighted gini impurity

Given that fraudulent transactions are typically rare events, I implemented a weighted version of the Gini impurity calculation to give more importance to the minority class:

- Maximum depth (dmax): None
- Minimum samples per leaf (minsamp): 2
- Weight for fraudulent class (w): 2
- Features used: All preprocessed features

##### Model 3: Depth-Limited Tree

The models with weighted gini and no depth restrictions show good performance, however the trees are very complex and the same continuous numerical features get split repeatedly. This is the model overfitting to the data. When we limit the maximum depth to 2 we get a much simpler and intuitive model, that still gives us good results, albeit slightly worse than the earlier model

- Maximum depth (dmax): 2
- Minimum samples per leaf (minsamp): 2
- Weight for fraudulent class (w): 2.0
- Features used: All preprocessed features

### Results

| Metrics   | Model 1 | Model 2 | Model 3 |
| --------- | ------- | ------- | ------- |
| Accuracy  | 1.0     | 1.0     | 1.0     |
| Precision | 0       | 1.0     | 1.0     |
| Recall    | 0       | 1.0     | 0.98    |
| F1-Score  | 0       | 1.0     | 0.99    |
**Model 1 confusion matrix**

|                  | Predicted non Fraud | Predicted Fraud |
| ---------------- | ------------------- | --------------- |
| Actual non fraud | 5083503             | 0               |
| Actual Fraud     | 6593                | 0               |
**Model 2 confusion matrix**

|                  | Predicted non Fraud | Predicted Fraud |
| ---------------- | ------------------- | --------------- |
| Actual non fraud | 5083503             | 0               |
| Actual Fraud     | 27                  | 6566            |

**Model 3 confusion matrix**

|                  | Predicted non Fraud | Predicted Fraud |
| ---------------- | ------------------- | --------------- |
| Actual non fraud | 5083503             | 0               |
| Actual Fraud     | 149                 | 6444            |
### Challenges
1. Selecting and engineering relevant features from the dataset for fraud detection
2. Handling both continuous and binary variable splits without prior knowledge of the variable 
3. Handling imbalanced nature of the dataset
4. Balancing model complexity with performance to avoid overfitting

## Conclusion

Our multiple linear regression model (Model 2) demonstrates strong predictive performance for fuel consumption based on CO emissions and vehicle class, taking advantage of the strong linear relationship between emissions and fuel consumption, while taking into account the class of vehicle to ideally improve predictive power of the model. 

The simplified decision tree model (Model 3) demonstrates strong predictive power in detecting fraud in the training set according to F1 score, precision and recall. While the model does a good job at minimizing type 1 error (false positive), in fraud detection it is typically more important to optimize for minimizing type 2 error (true negative) as it is better to accidentally label a non fraudulent transaction as fraudulent then to let fraudulent transactions be labeled as non fraudulent. In this aspect, the model could be better. 