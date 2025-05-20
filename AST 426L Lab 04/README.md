<h1 style="font-family: Georgia;">AST 426L: Technology Applications for Precision Agriculture</h1>
<p style="font-family: Georgia;"><strong>Instructor:</strong> Dr. Pappu Kumar Yadav</p>

# Lab 4: Using NDVI Data to Predict Corn and Soybean Yields in Google Colab with Python Programming

## Overview

This lab focuses on practical applications in precision agriculture, where we will process and analyze NDVI data to predict crop yields for corn and soybean. 
The dataset for this lab includes dummy NDVI and yield data, and we will generate regression models to understand the relationships between variables. 
Additionally, we will evaluate the performance of models using metrics such as RMSE and MAE, while exploring the use of geospatial data in agricultural decision-making.


## Technical Background


### Linear Regression Model
Linear regression is a fundamental statistical technique used to understand the relationship between a dependent variable (e.g., yield) and one or more independent variables (e.g., NDVI). It assumes that the relationship is linear and can be modeled with a straight line.

### Root Mean Square Error (RMSE)
RMSE is a widely used metric for evaluating the performance of regression models. It measures the square root of the average squared differences between predicted and observed values. A lower RMSE indicates better accuracy.

### Mean Absolute Error (MAE)
MAE measures the average magnitude of errors in a regression model, offering a straightforward interpretation of prediction errors.

### Pearson Correlation Coefficient (R²)
The Pearson Correlation Coefficient, often denoted as R², quantifies the strength of the linear relationship between two variables. It ranges from -1 to 1, where:
- A value of 1 indicates a perfect positive linear relationship.
- A value of -1 indicates a perfect negative linear relationship.
- A value of 0 suggests no linear correlation.

### Coefficient of Determination (R²)
The coefficient of determination, also denoted as R², measures the proportion of variance in the dependent variable that is predictable from the independent variable(s). It ranges from 0 to 1:
- A value of 1 indicates that the model perfectly predicts the dependent variable.
- A value of 0 indicates that the model explains none of the variability.


## Objectives


1. To generate dummy NDVI and yield datasets for corn and soybean using Python programming.
2. To generate linear regression models and analyze model performance using coefficients, RMSE, and MAE metrics.
3. To use the developed regression model to predict yield for a new dataset.


## Experimental Steps and Procedure


### Experiment 1: Generate Dummy NDVI and Yield Dataset for Corn and Soybean

#### Procedure:

1. Open a new Google Colab Notebook and name it "AST 426L Lab 4 2024."
2. Set up the environment by importing necessary Python libraries for data manipulation and visualization.
3. Generate dummy NDVI values ranging between 0.3 and 0.9 to simulate remote sensing data.
4. Generate dummy yield data for corn based on NDVI values with added random variations to mimic real-world scenarios.
5. Generate dummy yield data for soybean similarly based on NDVI values.
6. Combine the NDVI values and corresponding corn and soybean yield data into a single dataset.
7. Save the generated dataset as a CSV file named "NDVI_Yield_Dataset.csv" for further analysis.
8. Display a preview of the dataset by printing the first few rows to ensure correctness.
9. Save the Colab Notebook and dataset for later use in Experiment 2.



### Experiment 2: Use Generated Linear Regression Models to Predict Real-World Corn and Soybean Yield

#### Procedure:

1. Reopen the Google Colab Notebook created in Experiment 1.
2. Load the dataset "NDVI_Yield_Dataset.csv" into the Colab environment for analysis.
3. Explore the dataset to understand its structure and verify data integrity.
4. Prepare the data for analysis by separating NDVI values as independent variables and yields as dependent variables for corn and soybean.
5. Use Scikit-learn to create linear regression models for predicting yields based on NDVI values.
6. Fit the regression model for corn yields and extract the model coefficients and intercept.
7. Fit the regression model for soybean yields similarly and extract its coefficients and intercept.
8. Evaluate the corn model's performance using metrics such as RMSE and MAE.
9. Evaluate the soybean model's performance using the same metrics.
10. Visualize the relationships between NDVI values and predicted yields for corn and soybean using scatter plots and regression lines.
11. Use the corn regression model to predict yields for a new dataset of NDVI values.
12. Use the soybean regression model to predict yields for a new dataset of NDVI values.
13. Save the prediction results and evaluation metrics as a CSV file for submission.
14. Save the updated Colab Notebook with all outputs and visualizations for final submission.

