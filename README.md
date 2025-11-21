# ml_regression_miller
# Miller Regression Final

## Project Overview
This project focuses on successfully creating a ML regression model on the Kaggle Medical Cost Personal Dataset to predict an individual's insurance cost.

## Links

[This Notebook](https://github.com/DMill31/ml_regression_miller/blob/main/regression_miller.ipynb)

[Peer Review](https://github.com/DMill31/ml_regression_miller/blob/main/peer_review.md)

## Steps

## Imports
The necessary python libraries are imported at the top.

## Section 1. Load and Inspect the Data

### 1.1 Load the Data
The dataset can be found in the data folder, so we use the read_csv() function from pandas to get the data into a pandas DataFrame.

### 1.2 Check for Missing Values and Display Summary Statistics
After loading the data we look at the data itself to find any possible issues.

## Section 2. Data Exploration and Preparation

### 2.1 Explore Data Patterns and Distributions
Histograms of categorical features are created and scatter plots of numerical features are created.
We also plot the distribution of the target variable to see if it's a normal bell curve or not.

### 2.2 Handle Missing Values and Clean Data
The dataset doesn't have any missing values, so we just have to clean the data.
To do that, we convert categorical data to numeric.

### 2.3 Feature Engineering
Here new features are made by either altering a column or by combining columns.

## Section 3. Feature Selection and Justification

### 3.1 Choose Features and Target
The features chosen are:

Input features
- age
- smoker
- smoker_age
- bmi_squared

Target:
- log_charges

### 3.2 Define X and y
Here we just use some code to create the X and y variables that will be used to train/test the models.

## Section 4. Train a Model (Linear Regression)

### 4.1 Split the Data
We use the train_test_split() function to create the training and testing sets

### 4.2 Train Model
Here we create the Linear Regression model and train it using the .fit() function.

### 4.3 Evaluate Performance
Since the model is regression, we print the R2 score, RMSE, and MAE to evaluate performance.

## Section 5. Improve the Model (Implement Pipelines)

### 5.1 Implement Pipeline 1 (Imputer -> StandardScaler -> Linear Regression)
The first pipeline is created, trained, and predictions are made.

### 5.2 Implement Pipeline 2 (Imputer -> Polynomial Features (degree=3) -> StandardScaler -> Linear Regression)
The second pipeline is created, trained, and predictions are made.

### 5.3 Compare Performances
Here we print the metrics for all three models created.

## Section 6. Final Thoughts and Insights

### 6.1 Summarize Findings
A summary table is created and thoughts are given as to why some models performed better than others.

**Table:**
|  Model            |  R2   |  RMSE  |  MAE  |
| :--------------:  | ----: | -----: | ---:  |
| Linear Regression | 0.827 | 0.369  | 0.256 |
| Pipeline 1        | 0.827 | 0.369  | 0.256 |
| Pipeline 2 (poly) | 0.858 | 0.335  | 0.202 |

Linear Regression and the first pipeline performed the same, so it's mentioned that there must be a nonlinear relationship in the data that causes the second pipeline to perform better.

### 6.2 Discuss Challenges
A discussion of the troubles that came with this project is had.  They mostly resolve around my inexperience with pipelines and creating new features by mathematically altering current columns.

### 6.3 What I Would Do With More Time
If given more time, this project would go both forwards and backwards.
I would create the model without altering the features to see how much feature engineering helped model performance and I would try to better pipeline 2 by adding more to it.

---
## How to Run the Project

### 1. Open the Notebook
This project's notebook can be found at:

regression_miller.ipynb

[notebook](https://github.com/DMill31/ml_regression_miller/blob/main/regression_miller.ipynb)

### 2. Activate the Virtual Environment & Select Kernel
In the terminal, run:

```shell
.\.venv\Scripts\activate
```

Once the virtual environment is up, at the top of the notebook select the kernel that goes with it

### 3. Run the Notebook
Either select the 'Run All' button at the top of the notebook or run the notebook cell by cell