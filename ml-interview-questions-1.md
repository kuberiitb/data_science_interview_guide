1. Can you explain bias and variance in machine learning?
  * Bias refers to the error introduced by approximating a real-world problem with a simplified model. A model with high bias tends to make strong assumptions about the data, resulting in systematic errors and a limited ability to capture complex patterns. It can be seen as the algorithm's tendency to consistently miss the mark, regardless of the amount of data available for training. High-bias models are usually simpler and have fewer parameters, making them less prone to overfitting but potentially underperforming in complex tasks.

Variance, on the other hand, represents the variability or sensitivity of the model's predictions to fluctuations in the training data. A model with high variance is excessively sensitive to the specific training examples it encounters, resulting in a lack of generalization to unseen data. High-variance models tend to be more complex, with more parameters and greater flexibility, enabling them to fit the training data very well. However, this flexibility can lead to overfitting, where the model learns noise and irrelevant patterns instead of the underlying true patterns.

| topic       | bias                                                                           | variance |
| ----------- | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| what is?    | error introduced by approximating a real-world problem with a simplified model | Variability or sensitivity of the model's predictions to fluctuations in the training data |
| algorithm   | simple algorithm, miss the data points a lot, regardsless of amount of data    | complex algorithm, fit the data points too much and lack of generalization                 |
| model       |  High-bias models are usually simpler and have fewer parameters                | High variance models are usually complex and has lots of parameters |
| overfitting | less prone                                                                     | more prone |
| performance | less performance                                                               | high performance|

Ideally, we want a model that has low bias to capture important patterns in the data, but also low variance to avoid overfitting and make reliable predictions on unseen examples.

2. Next question
  * Answer 
