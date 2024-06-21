# Lloyds-Banking-Group-Loan-Default-Prediction-Challenge

## Lloyds Banking Group Step Up Challenge

### Task B – Data Science: Predicting Loan Defaults

This repository contains the solution for Task B of the Lloyds Banking Group Step Up Challenge, which involves designing a process to predict the likelihood of a new customer not paying back their loan. The task was completed using Jupyter Notebook and Python.

#### Steps Involved

##### Data Preprocessing

- **Column Analysis**:
  - Utilised Jupyter Notebooks and Python to determine the type of each column.
  - Noticed the presence of many non-numerical columns which required encoding.

- **Encoding**:
  - Converted categorical variables into numerical format using one hot encoding and label encoding.
  - Dropped some features, such as the employee title column, to manage data extensiveness.

- **Handling Null Values**:
  - Removed features with a significant number of null values (e.g., `inq_last_12m`).
  - For features with fewer null values (e.g., `avg_cur_bal`), filled in missing values using the mean.

- **Data Splitting**:
  - Split the data into training and testing sets using an 80-20 split.

##### Model Training and Making Predictions

- Used the logistic regression model from the `sklearn` library to predict loan defaults.
- Logistic regression was chosen for its effectiveness in binary classification tasks, predicting whether a customer will default on a loan (Charged Off or Fully Paid).
- Trained the model and made predictions on the data.

##### Evaluating Model Performance

- Evaluated the model using metrics such as the classification report and the confusion matrix.
- Achieved an accuracy of 79%.
- Compared logistic regression with other models like XGBoost, Random Forest Classifier, and Decision Tree Classifier, but found no significant improvement in accuracy.

##### Most Predictive Features

- Used Jupyter Notebooks to extract coefficients representing the importance of each feature.
- Created a DataFrame with feature names and their corresponding coefficients.
- Sorted features by their absolute coefficient values to determine their importance.
- Identified that the most predictive features for loan repayment are the monthly payment owed by the borrower, the interest rate on the loan, and the number of payments on the loan.

### Conclusion

The logistic regression model provided a reliable method for predicting loan defaults with an accuracy of 79%. The analysis identified key features that influence loan repayment, offering valuable insights for decision-making.

### Files in Repository

- `Lloyds Loan Default Prediction.ipynb`: Jupyter Notebook containing the code and analysis for the task.
- `LBG1.csv`: Directory containing the dataset used for the analysis.

### Requirements

- Python 3.x
- Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

### Usage

To run the analysis, open `Lloyds Loan Default Prediction.ipynb` in Jupyter Notebook and execute the cells.
