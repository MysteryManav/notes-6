### Bias:
- It refers to the error introduced by approximating a real-world problem with a simplified model
- High bias occurs when model is too simplistic and fails to capture the underlying patterns in the data, leading to underfitting
- Models with high bias are typically too simple to represent the complexity of data and have high training error and high test error

### Variance:
- It measures model's sensitivity to small fluctuations or noise in training data
- High variance occurs when the model is too complex and captures random noise or fluctuations in the training data leading to overfitting
- Models with high variance perform well on training data but generalise poorly on unseen data, resulting in low training error but high test error

### Model Complexity:
- It refers to the flexibility or capacity of the model to capture the underlying patterns in data
- Complex models have a larger number of parameters or degrees of freedom and can capture intricate relationships between features and target variable
- However, overly complex models are prone to overfitting and may generalise poorly to new data

### Relationships between Bias, Variance and Model Complexity:
- Bias and Variance are inversely related to each other. As model complexity increases, bias tends to decrease while variance increases. Conversely, reducing the complexity of model increases bias but reduces variance

### Strategies to manage Bias, Variance and Model Complexity:
- Regularisation
- Cross-Validation
- Feature Selection
- Model Ensemble
- Data Augmentation
