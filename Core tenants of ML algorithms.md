Machine learning algorithms use such a process as outlined by the flow chart:
![[Pasted image 20240827203402.png|400]]

When it comes to using a machine learning method, 3 components have to be taken care of:
- data representation - How should the data be provided to the algorithm
- Result optimization
- Evaluation on test data (out of sample)

### Effect of data distributions
The distribution of training data is going to affect the model built by the machine learning algorithm. The model will achieve good performance on the unseen data (test data) if the training data is drawn from the same distribution (both the data distributions are close to the population distribution). The training data should be representative of the population to ensure good out of sample performance. 

### Types of data
- Nominal data - Type of data that lacks an inherent order or ranking (eg: classification that cannot be ranked: 'human', 'dog', 'red')
- Ordinal data - Information with an inherent order/ranking but have unquantifiable differences between their values ('very bad', 'bad', 'ok', 'good', 'very good')
- Discrete data - Distinct separate values that can be measured. (Number of rooms in a building). 
- Continuous data - Data that can take any value in a defined interval (stock prices)

