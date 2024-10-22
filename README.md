PROJECT NAME: NAIVE BAYES UNDER THE HOOD

PROJECT GOAL:

The primary objective of this project is to demystify the Naive Bayes classifier, presenting it in an accessible manner that anyone can understand. It aims to break down the fundamental concepts behind this powerful machine learning algorithm, illustrating how it works and providing a step-by-step implementation at a basic level. By the end of this project, readers will have a clear understanding of the Naive Bayes classifier's principles, applications, and practical implementation, empowering them to apply these insights in real-world scenarios.

DESCRIPTION:

This project focuses on implementing a robust Naive Bayes classifier using Python, building upon the foundational concepts of probability theory and statistical inference. At its core, the Naive Bayes algorithm leverages Bayes' theorem, which relates the conditional and marginal probabilities of random variables, to make predictions based on input features.

To enhance the model's reliability, we incorporate logarithmic transformation to address potential underflow issues that can arise during probability calculations, especially when dealing with very small values. When probabilities are multiplied together, as is common in Naive Bayes, the resulting product can quickly become exceedingly small, potentially falling below the range of standard floating-point representation and causing numerical instability. By applying logarithms, we transform these multiplications into sums, effectively stabilizing the program and eliminating the risk of underflow while maintaining the accuracy of our predictions.

Moreover, we introduce additive smoothing, a technique that mitigates the problem of zero probabilities when estimating class-conditional probabilities. This functionality allows users to specify the degree of smoothing, enhancing the model's performance in scenarios with limited training data or unseen features. By adding a small constant (smoothing parameter) to the frequency counts, we ensure that no probability is ever exactly zero, allowing the algorithm to gracefully handle unseen attribute values during prediction.

Finally, the project expands its applicability by enabling the Naive Bayes algorithm to work with numerical input attributes. Instead of treating these attributes as categorical, we model their conditional distribution using a normal (Gaussian) distribution. This approach entails estimating the mean and standard deviation for each numerical feature within each class, thereby allowing us to compute probabilities based on the properties of the normal distribution. Consequently, the classifier can effectively handle a mixture of categorical and continuous features, making it a versatile tool for various classification tasks.

Through these enhancements, the project aims to provide a comprehensive implementation of the Naive Bayes classifier that balances mathematical rigor with practical usability.

DATA OVERVIEW:

The training data consists of 200 entries with the following attributes: Age: Integer values (e.g., 23, 47) Sex: Categorical values (F, M) BP: Categorical values (HIGH, LOW, NORMAL) Cholesterol: Categorical values (HIGH, NORMAL) Na: Continuous values (float) K: Continuous values (float) Drug: Target variable (categorical with classes drugY, drugX, drugA, drugC, drugB)

USED PYTHON LIBRARIES: pandas, numpy, scipy.stats
