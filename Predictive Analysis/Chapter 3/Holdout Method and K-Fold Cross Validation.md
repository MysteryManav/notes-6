- Cross-Validation is a technique used in machine learning to assess the performance of a predictive model
- It involves splitting the dataset into subsets, training the model on some of these subsets and evaluating its performance on the remaining subsets
- Two commonly used cross-validation techniques are:
	1. Holdout method
	2. K-Fold Cross Validation method

### Holdout Method:
- Dataset is divided into two subsets: Training set and Validation set
- Training set is used to train the model, while the validation set is used to evaluate its performance
- Typically, dataset is randomly split into a certain percentage for training and remaining percentage for validation, like 70/30, 80/20, etc.
- Model is trained on training set and its performance is assessed on validation set
- Drawback: It can produce high variance in performance estimate, especially in small datasets, because the evaluation heavily depends on particular instances chosen for training and validation

### K-Fold Cross Validation:
- It is a more robust cross-validation technique that overcomes limitations of Holdout Method by partitioning the dataset into *K* equal-sized subsets or folds
- The dataset is divided into *K* folds, with *K-1* folds used for training and remaining fold used for validation. This process is repeated *K* times, with each fold used as the validation set exactly once
- After *K* iterations, the performance of model is evaluated by averaging the results from each fold
- It is a more reliable estimate of model's performance because it ensures that all instances in dataset are used for both training and validation, reducing the variance in performance estimate