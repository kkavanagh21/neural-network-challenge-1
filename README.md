# Neural Network Challenge 1

## Project Overview

The goal of this project is to build a predictive model that helps financial institutions assess the likelihood of loan repayment by students. By examining features like GPA, financial aid, career prospects, and more, the model provides a binary classification: whether the loan will be repaid (1) or not (0).

The project also explores how a similar model could be adapted to recommend student loan options to students by analyzing key data points such as academic performance and financial background.

## Data

The dataset used in this project includes multiple features that play a role in loan repayment decisions, such as:

- **Payment History**: A student’s track record of payments.
- **GPA Ranking**: Performance during their academic studies.
- **Time to Completion**: The estimated time left to complete their degree.
- **Financial Aid Score**: How much financial aid they’ve received.
- **Loan Scores**: Aggregated data about total loan amounts and repayment terms.

By combining these variables, we aim to capture a comprehensive picture of the student’s likelihood of repayment.

## Model Architecture

We employed a **deep neural network** with the following structure:

- **Input Layer**: 11 features representing student data.
- **Hidden Layer 1**: 12 neurons with ReLU activation.
- **Hidden Layer 2**: 8 neurons with ReLU activation.
- **Output Layer**: 1 neuron with sigmoid activation, used for binary classification.

The model was compiled using the **Adam optimizer** and **binary cross-entropy** as the loss function. After training the model for 50 epochs, we achieved a test accuracy of **(insert test accuracy here)**, showing promising results in predicting student loan repayment success.

## Prediction Process

Once trained, the model was used to predict loan repayment success on unseen testing data. The model outputs probabilities, which are rounded to binary values (0 or 1) to indicate whether a loan will be successfully repaid. Additionally, a classification report is generated to provide detailed performance metrics like precision, recall, and F1-score.

## Next Steps: A Recommendation System

In addition to predicting repayment success, this model can serve as the foundation for a **student loan recommendation system**. By analyzing student-specific data, the system could recommend loan options that are better suited to the student’s academic performance, financial situation, and career prospects. For this system, **content-based filtering** is the most suitable approach, as it would focus on matching the loan options to each individual’s unique characteristics.

## Real-World Considerations

Building a recommendation system for student loans involves navigating two major challenges:
1. **Data Privacy and Security**: Protecting sensitive personal and financial data is critical.
2. **Bias and Fairness**: The system must be designed to ensure equitable recommendations for students from all backgrounds, avoiding biases that could exacerbate financial inequalities.

## How to Use This Project

1. **Model Training**: The model can be trained using the provided dataset by running the Jupyter notebook. You can customize the number of epochs, batch size, and model architecture as needed.
2. **Predictions**: After training, you can load the model to make predictions on new student data.
3. **Recommendation System**: The project also sets the foundation for developing a recommendation system by analyzing similar student profiles.

