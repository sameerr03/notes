A classification model is a model that finds an abstract representation of the relationship between the attribute set $X$ of a datapoint and its corresponding class label $y$ (Human with attributes $X$, being classified as a mammal ($y$)). It takes in information in the attribute set, and after a set of unobserved operations learnt from training data, the model produces the class label $y$, which is the output.
![[Pasted image 20240911195032.png]]
The model can be represented as a tree, a probability table or a [[Vectors|vector]]. 

Classification can be used to classify previously unseen datapoints (predictive model) or can help in identifying characteristics in the set $X$ that are most useful in determining the class (Descriptive model).

**Induction** is the process of using an algorithm to build an accurate classification model from the training data. **Deduction** is the process of applying a classification model on unseen instances of test data to predict labels. 

#### Performance of a classification model
The model should be able to accurately predict class labels on unseen (test dataset) data. Models that produce predictive insights have good generalization performance. 

We can summarize the results of the model using a confusion matrix. 

| ActualClass/Predicted | Class 1  | Class 0  |
| --------------------- | -------- | -------- |
| Class 1               | $f_{11}$ | $f_{10}$ |
| Class 0               | $f_{01}$ | $f_{00}$ |
We can define the term **accuracy** as the ratio of the number of correct predictions by the number of total predictions:$$\text{Accuracy} = \frac{f_{11}+f_{00}}{f_{11}+f_{10}+f_{01}+f_{00}}$$The error rate is given by $$\text{Error rate} = 1-\text{Accuracy}$$
##### Classwise performance metrics
**Recall** for a class is the number of true positives by the number of positives in the data. For class 1 and 0, $$\text{Recall}_1=\frac{f_{11}}{f_{11}+f_{10}}, \ \text{Recall}_0=\frac{f_{00}}{f_{00}+f_{01}}$$It is important to note that high recall does not necessarily mean good performance. if the model blindly labelled everything as positive, we could theoretically have high recall but poor generalization performance. We can also look at another metric that solves this in conjunction with recall, the **precision** which is the ratio of true positives to true positives and false positives. For class 1 and 0, $$\text{Precision}_1=\frac{f_{11}}{f_{11}+f_{01}}, \ \text{Precision}_0=\frac{f_{00}}{f_{00}+f_{10}}$$
#### Types of classification models
- [[Naive Bayes classifier]]
- [[Decision tree classifier]]
- 
