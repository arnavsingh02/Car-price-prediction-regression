This project explores predicting car prices using multiple regression techniques on the Automobile dataset. The dataset contains specifications of different cars (such as engine size, horsepower, curb weight, and other features), with the target variable being the car price.

The final version of the code integrated all the improvements systematically:
1. Preprocessing and Handling of Missing Data:
Missing data was handled by filling missing values with the column means.
This ensured no rows or features were dropped prematurely.

2. Feature Engineering:
Log transformations and interaction terms were introduced to handle
nonlinearities and improve model expressiveness.
Binning of year data to group continuous values and reduce complexity.
3. Feature Selection:
Zero variance features were removed to reduce noise in the dataset.
Highly correlated features were iteratively dropped to address
multicollinearity.
Low variance features were also removed, as they are likely uninformative.
4. Standardization:
The features were standardized (mean = 0, std = 1), which is essential for
models like ridge regression that are sensitive to scale differences between
features.

5. Ridge Regression with Cross-Validation:
Ridge regression was used as the final model to address both overfitting and
numerical instability.
Cross-validation was performed over a range of lambda values to find the
optimal regularization strength, which ensures a balance between model
complexity and predictive accuracy.

6. Model Evaluation:

The model's performance was assessed using Mean Squared Error (MSE),
Root Mean Squared Error (RMSE), and R-squared, providing a
comprehensive view of how well the model fits the test data.

Final Improvements:
The final code takes a complete machine learning pipeline approach, incorporating data
preprocessing, feature engineering, model selection (cross-validation), and evaluation. By
progressively addressing data issues, scaling, and regularization, the model becomes more robust
and predictive, while ensuring stability through ridge regression and cross-validation.
