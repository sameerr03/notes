Forward search starts from an empty set of features. Each of the remaining features is tried and we estimate the classification/regression error for adding a specific feature. We select features that give maximum improvement in validation error.

Backwards search starts with the original dataset and drops features with the smallest impact on the error reduction.

These algorithms are "greedy", they select the best option at each step and do not always reach the global optimal value. 