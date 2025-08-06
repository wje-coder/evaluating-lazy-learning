# evaluating-lazy-learning
This project compares lazy learning methods like K-Nearest Neighbors (K-NN) with eager learning methods like Gradient Descent, Stochastic Gradient Descent (SGD), and Adam. The goal was to see how these models perform when resources (training time and data) are limited, using the Letter Recognition Dataset from the UCI Machine Learning Repository.

# What I Did
Used the Letter Recognition Dataset (20,000 samples, 16 features) but limited training to 2,000 samples to simulate a low-resource environment. Standardized features and tested models under constrained training (fewer epochs, reduced data). Compared accuracy, inference time, memory usage, and scalability across all models. Looked at how lazy learners like K-NN stack up against eager methods when resources are tight.

# Models Used
K-Nearest Neighbors (K-NN) – lazy learner, no training phase, defers computation to prediction. Gradient Descent – eager learner with batch updates. Stochastic Gradient Descent (SGD) – eager learner with single-sample updates for faster training. Adam – eager optimizer using momentum and adaptive learning rates.

# Results
K-NN did the best overall – highest accuracy and still efficient with memory and speed.
SGD was the fastest, but accuracy dropped. Gradient Descent was balanced, decent accuracy and efficiency. Adam performed the worst because it needs more training data and epochs to show its real strength. K-NN’s lazy approach worked great in this environment because it doesn’t rely on training — it just stores the data and makes predictions based on similarity.

