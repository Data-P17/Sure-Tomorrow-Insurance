# Sure Tomorrow Insurance Project - Work Plan

## Project Overview
The Sure Tomorrow insurance company wants to solve several tasks with the help of Machine Learning:
- **Task 1**: Find customers who are similar to a given customer (for marketing)
- **Task 2**: Predict whether a new customer is likely to receive an insurance benefit
- **Task 3**: Predict the number of insurance benefits a new customer is likely to receive using linear regression
- **Task 4**: Protect clients' personal data with obfuscation/masking without breaking the ML model

---

## 1. Import Libraries
**Objective**: Import all necessary Python libraries for data analysis, visualization, preprocessing, machine learning, and model evaluation.

### Tasks:
- [ ] Import data manipulation libraries (numpy, pandas)
- [ ] Import visualization libraries (matplotlib, seaborn)
- [ ] Import machine learning libraries (sklearn)
  - Preprocessing: MaxAbsScaler, OrdinalEncoder
  - Model selection: train_test_split
  - Neighbors: NearestNeighbors, KNeighborsClassifier
  - Linear model: LogisticRegression, LinearRegression
  - Metrics: AUC-ROC, ROC curve, classification metrics
- [ ] Import utility libraries (IPython.display)

**Current Status**: ✓ Complete

---

## 2. Data Exploration
**Objective**: Load and examine the dataset structure, columns, data types, and basic statistics.

### Tasks:
- [ ] Load CSV dataset (insurance_us.csv)
- [ ] Review dataset shape and structure
- [ ] Examine column names and data types
- [ ] Display sample rows (10-20 rows)
- [ ] Check for missing values
- [ ] Review summary statistics (describe())
- [ ] Rename columns for consistency (Gender → gender, Age → age, Salary → income, etc.)

**Current Status**: ✓ Complete

---

## 3. Data Preprocessing
**Objective**: Clean and transform data for analysis and modeling.

### Tasks:
- [ ] Convert data types as needed
  - [ ] Convert age from float to int
  - [ ] Verify conversion success
- [ ] Handle numerical precision
  - [ ] Round income column to 2 decimal places
  - [ ] Review rounded data samples
- [ ] Check for duplicates and inconsistencies
- [ ] Validate data integrity post-preprocessing

**Current Status**: ✓ Complete

---

## 4. Exploratory Data Analysis (EDA)
**Objective**: Visualize and understand data patterns and distributions.

### Tasks:
- [ ] Create pair plot histogram to visualize relationships
- [ ] Identify data patterns and potential clusters
- [ ] Analyze distribution of features
- [ ] Examine categorical vs numerical features
- [ ] Document findings and insights

**Current Status**: ✓ Complete

---

## 5. Feature Engineering & Data Preparation
**Objective**: Prepare features and target variables for modeling.

### Tasks:
- [ ] Identify personal information columns for Task 4 (obfuscation)
- [ ] Separate features (X) from target (y)
- [ ] Apply ordinal encoding to categorical features (gender)
- [ ] Prepare separate datasets for different tasks:
  - Task 1: Similarity (use scaled features)
  - Task 2: Classification (use scaled features)
  - Task 3: Regression (use scaled features)
  - Task 4: Obfuscated data (use transformed features)
- [ ] Document feature list for each task

**Current Status**: 🔄 In Progress

---

## 6. Model Development & Data Splitting
**Objective**: Prepare data for model training and evaluation.

### Tasks:
- [ ] Split data into features (X) and target variables (y) for each task
- [ ] Analyze class distribution (especially for Task 2)
- [ ] Apply appropriate scaling (MaxAbsScaler)
  - Scaled dataset for Tasks 1, 2, 3
  - Original dataset for baseline comparison
- [ ] Split into training, validation, and testing sets
  - Train: ~60%
  - Validation: ~20%
  - Test: ~20%
- [ ] Analyze dataset splits for balance and representativeness

**Current Status**: 🔄 In Progress

---

## 7. Model Training
**Objective**: Train machine learning models for each task.

### Task 1 - Similar Customers:
- [ ] Train KNeighborsClassifier (k=1 for exact nearest neighbors)
- [ ] Optimize k value using cross-validation

### Task 2 - Classification (Insurance Benefit Prediction):
- [ ] Train Logistic Regression model (baseline)
- [ ] Train Random Forest Classifier model
- [ ] Document model parameters and performance

### Task 3 - Regression (Insurance Benefits Count):
- [ ] Train Linear Regression model
- [ ] Train custom Linear Regression model (from scratch)
- [ ] Compare model performance

### Task 4 - Data Obfuscation:
- [ ] Develop data transformation algorithm (matrix multiplication)
- [ ] Train models on obfuscated data
- [ ] Compare with original model performance

**Current Status**: 🔄 In Progress

---

## 8. Model Adjustments & Optimization
**Objective**: Fine-tune models for better performance.

### Tasks:
- [ ] **Weighted Class Adjustments**: Handle class imbalance
  - [ ] Calculate class weights based on distribution
  - [ ] Apply weights to Logistic Regression
  - [ ] Apply weights to Random Forest Classifier
- [ ] **Threshold Adjustments**: Optimize decision boundaries
  - [ ] Test different probability thresholds (0.3, 0.4, 0.5, 0.6, 0.7)
  - [ ] Find optimal threshold based on AUC-ROC
- [ ] **Final Testing**: Validate models on test set
  - [ ] Generate predictions for test data
  - [ ] Calculate final performance metrics

**Current Status**: ⏳ Not Started

---

## 9. Model Metrics & Validation
**Objective**: Evaluate and validate model performance using appropriate metrics.

### Tasks:
- [ ] **Classification Metrics** (Tasks 1, 2, 4):
  - [ ] Calculate AUC-ROC score
  - [ ] Plot ROC Curve
  - [ ] Calculate precision, recall, F1-score
  - [ ] Generate confusion matrix
- [ ] **Regression Metrics** (Task 3):
  - [ ] Calculate Mean Absolute Error (MAE)
  - [ ] Calculate Root Mean Squared Error (RMSE)
  - [ ] Calculate R² score
- [ ] **Sanity Testing**:
  - [ ] Verify model makes logical predictions
  - [ ] Test on edge cases
  - [ ] Compare model results with dummy/baseline models
  - [ ] Validate Task 4: Confirm obfuscated model performance equals original

**Current Status**: ⏳ Not Started

---

## 10. Conclusion & Reporting
**Objective**: Summarize findings and model performance.

### Tasks:
- [ ] **Task 1 Results**: Summarize customer similarity findings
  - [ ] Present nearest neighbors for test cases
  - [ ] Show practical applications for marketing
- [ ] **Task 2 Results**: Summarize classification model performance
  - [ ] Compare Logistic Regression vs Random Forest
  - [ ] Report AUC-ROC scores
  - [ ] Document optimal threshold findings
- [ ] **Task 3 Results**: Summarize regression model performance
  - [ ] Report prediction accuracy metrics
  - [ ] Show prediction vs actual values
- [ ] **Task 4 Results**: Summarize obfuscation effectiveness
  - [ ] Confirm data is protected
  - [ ] Verify ML model quality preserved
  - [ ] Explain transformation algorithm
- [ ] **Overall Conclusions**:
  - [ ] Key findings and insights
  - [ ] Model recommendations
  - [ ] Limitations and future improvements
  - [ ] Business implications

**Current Status**: ⏳ Not Started

---

## Notebook Cell Organization

### Section 1: Import Libraries (Cells 1-5)
- Title and project overview
- Statement of tasks
- Library imports

### Section 2: Data Exploration (Cells 6-16)
- Load data
- Rename columns
- Sample data
- Data info
- Descriptive statistics
- Data visualization

### Section 3: Data Preprocessing (Cells 17-22)
- Type conversions
- Rounding/normalization
- Data validation

### Section 4: EDA (Cells 23-31)
- Feature relationships
- Distribution analysis
- Pattern identification

### Section 5: Feature Engineering (Cells 32-56)
- Feature preparation
- Data scaling
- Target variable identification
- Ordinal encoding for categorical features

### Section 6: Model Development (Cells 57-73)
- Data splitting
- Class distribution analysis
- Feature standardization

### Section 7: Model Training (Cells 74-93)
- Task 1: KNeighbors implementation
- Task 2: Logistic Regression and Random Forest
- Task 3: Linear Regression
- Task 4: Data obfuscation algorithm

### Section 8: Model Adjustments (Cells 94-100)
- Weighted class adjustments
- Threshold optimization
- Final model tuning

### Section 9: Metrics & Validation (Cells 101-106)
- ROC curves and AUC scores
- Performance metrics
- Model comparison
- Sanity checks

### Section 10: Conclusion (Future)
- Summary of all findings
- Business recommendations
- Final insights

---

## Progress Tracking

| Phase | Status | Completion |
|-------|--------|-----------|
| 1. Import Libraries | ✓ Complete | 100% |
| 2. Data Exploration | ✓ Complete | 100% |
| 3. Data Preprocessing | ✓ Complete | 100% |
| 4. EDA | ✓ Complete | 100% |
| 5. Feature Engineering | 🔄 In Progress | 50% |
| 6. Model Development | 🔄 In Progress | 60% |
| 7. Model Training | 🔄 In Progress | 70% |
| 8. Model Adjustments | ⏳ Not Started | 0% |
| 9. Model Metrics & Validation | ⏳ Not Started | 10% |
| 10. Conclusion | ⏳ Not Started | 0% |

---

## Key Deliverables

1. ✓ Data cleaning and preparation
2. ✓ Exploratory analysis and visualization
3. 🔄 Machine learning models for 4 tasks
4. ⏳ Performance metrics and validation
5. ⏳ Data obfuscation algorithm verification
6. ⏳ Final recommendations and insights
