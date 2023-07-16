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

2. How LIME explains an ML model?
  * LIME (Local Interpretable Model-agnostic Explanations) is a popular technique used to explain the predictions of machine learning models. It provides local explanations by approximating the behavior of the underlying model around a specific data point or instance. LIME is model-agnostic, meaning it can be applied to any machine learning model, regardless of its type or complexity.

Here's a high-level overview of how LIME works:

- Select an instance: Start by selecting the instance for which you want to explain the model's prediction. This could be an input data point for which you want to understand why the model made a particular prediction.

- Generate perturbations: Create perturbations or variations of the selected instance by introducing random noise or altering its feature values within a certain range. These perturbed instances will be used to understand the model's behavior in the vicinity of the original instance.

- Model predictions: Pass the perturbed instances through the model and obtain their corresponding predictions. This step involves feeding the perturbed instances through the original model, essentially acting as a proxy to predict what the model would output for those perturbed inputs.

- Weighting perturbations: Assign weights to the perturbed instances based on their proximity to the original instance. The weights can be determined using a distance measure, such as Euclidean distance or kernel similarity.

- Fit an interpretable model: Fit an interpretable model, such as linear regression or decision trees, to explain the relationship between the perturbed instances and the model's predictions. The weights assigned in the previous step are used to weigh the importance of each perturbed instance in training the interpretable model.

- Interpretation: Once the interpretable model is trained, it can provide explanations by highlighting the most influential features or factors contributing to the model's prediction for the selected instance. These explanations help understand the reasons behind the model's decision for that particular instance.

By examining the explanations provided by LIME, users can gain insights into the model's behavior, understand the importance of different features, and assess the model's reliability and potential biases. LIME's local explanations are particularly useful for identifying whether the model relies on relevant features or if it is influenced by noise or irrelevant factors in the data.

It's important to note that LIME provides local explanations, which means they are specific to the selected instance and may not necessarily represent the model's behavior globally. Nonetheless, LIME is a valuable tool for interpreting individual predictions and understanding the inner workings of black-box machine learning models.
