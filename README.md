# Sure-Tomorrow-Insurance
A Linear Algebra Project

# Statement
The Sure Tomorrow insurance company wants to solve several tasks with the help of Machine Learning and you are asked to evaluate that possibility.

- Task 1: Find customers who are similar to a given customer. This will help the company's agents with marketing.
- Task 2: Predict whether a new customer is likely to receive an insurance benefit. Can a prediction model do better than a dummy model?
- Task 3: Predict the number of insurance benefits a new customer is likely to receive using a linear regression model.
- Task 4: Protect clients' personal data without breaking the model from the previous task. It's necessary to develop a data transformation algorithm that would make it hard to recover personal information if the data fell into the wrong hands. This is called data masking, or data obfuscation. But the data should be protected in such a way that the quality of machine learning models doesn't suffer. You don't need to pick the best model, just prove that the algorithm works correctly.

## Work Flow

### 1. Import Libraries

* Import libraries for data analysis, visualization, preprocessing, machine learning, and model evaluation.

### 2. Data Exploration

* Load datasets and review structure, columns, and data types.

### 3. Data Preprocessing

* Convert and format numerical data types.
* Analyze and standardize the data.

### 4. Exploratory Data Analysis (EDA)

* Create visualizations to examine data distributions and patterns.

### 5. Feature Engineering

#### Task 1: Similar Customers

* Find nearest neighbors using distance metrics.
* Scale features and compare original vs scaled results.
* Analyze customer similarity results.

#### Task 2: Insurance Benefit Classification

* Create binary target variables.
* Analyze class imbalance and visualize distributions.
* Split data into training and testing datasets.
* Evaluate predictions using F1 score and confusion matrix.
* Build and evaluate KNN classification models.
* Compare model results with random probability predictions.

#### Task 3: Regression with Linear Regression

* Train and evaluate Linear Regression models.
* Compare results using original and scaled data.
* Measure RMSE and R² performance metrics.

Task 4: Data Obfuscation

* Transform data using matrix multiplication.
* Verify data recovery and matrix invertibility.
* Test Linear Regression performance on obfuscated data.
* Validate that obfuscation preserves model quality.

6. Conclusion

* Summarize findings, model results, and insights.
