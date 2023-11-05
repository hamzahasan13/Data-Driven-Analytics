# Data-Driven-Analytics

## Table of Contents
1) Tools used
2) Overview
3) Goal
4) Data Preprocessing
5) Outlier Analysis
6) A/B Testing
7) Exploratory Data Analysis
* 7.1) Numerical Data Visualization
* 7.2) Categorical Data Visualization
8) Dimension Reduction
*  8.1) Categorical Encoding and Data Normalization
*  8.2) Feature Selection
*  8.3) Principal Component Analysis
9) Data Modeling
10) Evaluation of Machine Learning models
   10.1) Hyperparameter Tuning
11) Conclusion/Discussion

### 1. Tools used
<img src="https://github.com/hamzahasan13/Airline-Passenger-Dissatisfaction-Analysis/blob/main/Images/Python-logo.png" alt="drawing" width="200"/>
<img src="https://github.com/hamzahasan13/Airline-Passenger-Dissatisfaction-Analysis/blob/main/Images/jupyter_nb.png" alt="drawing" width="400"/>

### 2. Overview
Each year, millions of used cars are sold causing this market to be large and dynamic. Due to this reason, this market is complicated and requires complex Data Mining techniques to navigate through large amounts of data to find insights. Understanding these insights can help the buyers and companies evaluate the factors that influence the prices for used cars. This pricing analytics, can help individuals and companies to understand the market price for a car before publishing it as an ad online. Companies can maximize their profits and boost their financial metrics in a competitive market by using data mining and machine learning algorithms to sell used cars effectively.

### 3. Goal
The goal of this project is to generate insights using Exploratory Data Analysis and see what variables affect the pricing of the used car. Secondly, the aim is to use the historical data to make predictions on the price of the used car using Regression. This model can then be deployed to predict real world cases of used cars and propel data driven decision making.

### 4. Data Preprocessing

The dataset was analyzed and found that five categorical variables containing missing values as shown in the figure.

<img width="791" alt="Screenshot 2023-11-05 at 12 51 38 PM" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/8610e137-83c5-465b-808a-eceaea679870">

The heatmap shown in Figure, describes the correlation between null values in one column and the null values or data values in the corresponding columns. If there are null values in both columns, then the correlation is positive. On the other hand, if there are null values in one column and data values in other column then the correlation is weak or towards the negative value. The missing values were imputed using mode values of the respective columns.

<img width="860" alt="image" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/bbd5ccf8-5907-44b5-a9d3-2a0a516a7e52">

### 5. Outlier Analysis

Numerical variables, Price, Horsepower and Kilometer, were checked for outliers and then fixed by removing values that were greater than 3 standard deviations above the mean. 

<img width="823" alt="image" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/fdd7720f-1fe1-499f-bf4f-4d255560ef94">

### 6. A/B Testing

The Prices of car were checked to see if they changed during the Financial Crisis (2007-2009). To test this condition, a hypothesis was formulated:
• Null hypothesis: The mean price of cars before and during the financial crisis
(2007-2009) remained the same.
• Alternative hypothesis: The mean price of cars during the financial crisis (2007-
2009) is different from the mean price of cars before the crisis.
T-test and the following results were obtained as shown in figure above.

From the results, it can be concluded that there is a large difference between the mean of the two groups (t-statistic = 211.13, p-value <0.05). Hence, the null hypothesis can be rejected. This means that the mean price of cars during the financial crisis was significantly different than the mean price of cars before the financial crisis.

<img width="325" alt="image" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/6dbc710d-28fd-4f3f-831a-2e149c77e9dd">

### 7. Exploratory Data Analysis

#### 7.1 Numerical Data Visualization

The output variable is highly skewed to the right.

<img width="811" alt="image" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/f4bba2ca-7188-4f9e-ba3c-7882c0431f83">

From the correlation heatmap:
* Price and Horsepower are positively correlated
* Price and Kilometer are negatively correlated

<img width="883" alt="image" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/b89ab7a3-e763-4692-bc83-1f1b662c2c27">

#### 7.2 Categoricl Data Visualization

The most preferred fuel types are gasoline and diesel but the electric and hybrid cars have the highest average selling price.

<img width="853" alt="image" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/881fa0c3-fe5e-49b3-8c3e-5c2ae3a202b7">

<img width="860" alt="image" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/dd5569a7-9f4a-49ea-a814-64e79066b4ef">

### 8. Dimension Reduction
#### 8.1 Categorical Encoding and Dimension Reduction

Categorical Columns and were one-hot and label encoded. Numerical columns were normalized to bring the range of these variables between 0 and 1.

#### 8.2 Feature Selection

Feature Selection was applied to identify top features based on the correlation between each feature and the target variable.

<img width="798" alt="image" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/cc2a520d-e0c6-42a3-8dff-d62c7e4d081f">

#### 8.4 Principal Component Analysis

After categorical encoding, the number of variables increased to 28. This prompted the need for dimension reduction to find the minimum number of features that capture the maximum variance. Principal Component Analysis was carried out and a function was created to capture 99% variance. To capture 99% variance, 13 components were needed out of 28 variables. Heatmap for principal components were created. As shown in figure, all the PCs are uncorrelated to each other.

<img width="839" alt="image" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/7aaccfeb-0a3a-4cad-bdce-19dfdc00f416">

### 9. Data Modeling
After carrying out dimension reduction, the dataset was split into training, validation, and test sets in the following proportions:
• Training: 70%
• Validation: 15%
• Test: 15%

The following six regression algorithms were used:
*   Linear Regression
*   Elastic Net
*   Decision Tree Regressor
*   Gradient Boosting Regressor
*   XG Boosting
*   Random Forest Regressor

### 10. Evaluation of Machine Learning Models

Random Forest Regressor was the standout model as it has the highest R_squared value on the validation set.
Random Forest Regressor performed the best as it has the lowest MAE and RMSE values on the validation set

<img width="841" alt="image" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/27bbcf3f-e2ad-42dd-8bdb-809eae8d0e55">

<img width="840" alt="image" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/070c1359-ab72-4ad8-9ace-815ab0daf9c7">

After evaluating the metrics for all the models, it can be concluded that Random Forest Regressor was the best model having higher R_squared value and lower
MAE and RMSE values on the validation set. This model was then evaluated on the test set and achieved an R_squared of 0.75.

<img width="212" alt="image" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/078141aa-676c-457f-81de-599a9e2791e8">

#### 10.1 Hyperparameter Tuning

Hyperparameter tuning was carried out using Randomized Search CV on Elastic Net and Decision Tree Regressor.

<img width="847" alt="image" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/58ab54e0-261f-4979-9679-7d930e83d6c6">

<img width="860" alt="image" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/7ebfaef1-0376-405d-a851-345aad68f7cc">

Hyper parameter tuning had a positive impact on the model performance of Elastic Net and Decision Tree Regressor. The R_squared for Elastic Net increased from 0.18 to 0.42. Similarly, for Decision Tree Regressor, R_squared jumped from 0.68 to 0.72 before and after using hyper parameter tuning as seen in figures above.

### 11 Conclusion/Discussions

1) Using accurate prediction models, consumers can better estimate the price of the car resulting in improved pricing accuracy.
2) Car dealers can use these models to price the cars more accurately promoting transparency and reducing the risk of fraud.
3) By deploying this model, predicting the price of used cars can be automated leading to increased efficiency that saves time and money.
4) Accurate predictions using this ML model can lead to data driven decision making for both the consumers and the car dealers.



