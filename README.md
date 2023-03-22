# LogisticRegression-HR-DATASET-.ipynb
This repository contains code for implementing logistic regression on the HR dataset. The goal is to predict whether an employee will leave a company based on certain features.

# Dataset
The HR dataset used in this code can be found in the Datasets folder. It is a comma-separated values (CSV) file containing information on various employees in a company. The columns in the dataset are as follows:

satisfaction_level: level of satisfaction of the employee (between 0 and 1)

last_evaluation: time since last evaluation (in years)

number_project: number of projects completed by the employee

average_montly_hours: average monthly hours worked by the employee

time_spend_company: time spent by the employee in the company (in years)

Work_accident: whether the employee had a work accident or not (0 = no, 1 = yes)

promotion_last_5years: whether the employee was promoted in the last 5 years or not (0 = no, 1 = yes)

Department: the department the employee belongs to

salary: level of salary of the employee (low, medium or high)

left(Target Variable): whether the employee left the company or not (0 = no, 1 = yes)

# Data Preprocessing
The first step is to preprocess the data. This includes:

1-Moving the dependent variable left to the last index in the dataset.

2-Converting non-categorical values in the data to categorical values (2 attributes only).

3-Assigning the dependent and independent variables.

4-Splitting the data into test and train subsets.

# Explanation of the Model Training Part
The code uses the scikit-learn library to implement logistic regression. First, the model is trained on the training data using only the important features.

After selecting the important features using Recursive Feature Elimination (RFE), the next step is to train the logistic regression model on the selected features. In this code, we are using the LogisticRegression class from the scikit-learn library to train the model.

Before training the model, we first instantiate an object of LogisticRegression class with a max_iter parameter. The max_iter parameter controls the maximum number of iterations taken for the solver to converge, and we set it to 1000.

Next, we fit the RFE model to the training data using the fit_transform() method of the RFE class, which returns the transformed training data with only the selected features. We then fit the logistic regression model on the selected features using the fit() method of the LogisticRegression class.

After training the model, we use it to predict the class of the test data. To do this, we transform the test data using the transform() method of the RFE object

# Visualizing the Data
The code also includes a visualization of the predicted probabilities of the model. This is done by creating a range of values for the independent variable, reshaping the coefficients to match the shape of the independent variable, and calculating the predicted probability for each value in the range. The predicted probabilities are then plotted against the independent variable.
