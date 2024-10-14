#### Supervised Learning
Supervised machine learning takes in data and the desired output of the machine learning exercise (information that is already classified) and trains to achieve the results according to the information provided. 

Examples of supervised ML techniques are [[Simple Linear Regression|Linear Regressions]] - which predict numerical values from linear relationships with other numerical values and classification function which learn labels. 

#### Unsupervised Learning
The training data is given, but the model is not provided with the desired output. 

Clustering is an unsupervised ML technique that finds groups among datapoints such that similar datapoints are grouped together. The desired groups are not provided to the algorithm

#### Semi-Supervised Learning
The training data and a few desired outputs are provided. This method combines both supervised and unsupervised learning techniques. It improves performance when data that has already been classified is scarce. 

A text classification model is an example of a semi-supervised ML technique

#### Reinforcement Learning
An agent is trained using rewards and penalties based on its actions. The agent tries to maximize its cumulative reward over time. The model never stops learning unlike the other models, that only learn on the training data provided. 


| Supervised learning                                      | Unsupervised learning                                                                          |
| -------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| Humans provide labeled samples                           | No labeled samples provided                                                                    |
| Asks machine to learn the label to data patterns         | no assumptions about patterns, uses the algorithm to find similarities and differences in data |
| Uses trained model on labels to label future unseen data | Ideal solution for exploratory data analysis - nothing is known about data                     |

