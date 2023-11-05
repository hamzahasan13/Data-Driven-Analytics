# Data-Driven-Analytics

## Table of Contents
1) Tools used
2) Overview
3) Goal
4) Data Preprocessing
5) Outlier Analysis
6) A/B Testing
7) Exploratory Data Analysis
8) Dimension Reduction
*  8.1) Categorical Encoding
*  8.2) Data Normalization
*  8.3) Feature Selection
*  8.4) Principal Component Analysis
9) Evaluation of Machine Learning models
10) Conclusion/Discussion

### 1. Tools used
<img src="https://github.com/hamzahasan13/Airline-Passenger-Dissatisfaction-Analysis/blob/main/Images/Python-logo.png" alt="drawing" width="200"/>
<img src="https://github.com/hamzahasan13/Airline-Passenger-Dissatisfaction-Analysis/blob/main/Images/jupyter_nb.png" alt="drawing" width="400"/>

### 2. Overview
Each year, millions of used cars are sold causing this market to be large and dynamic. Due to this reason, this market is complicated and requires complex Data Mining techniques to navigate through large amounts of data to find insights. Understanding these insights can help the buyers and companies evaluate the factors that influence the prices for used cars. This pricing analytics, can help individuals and companies to understand the market price for a car before publishing it as an ad online. Companies can maximize their profits and boost their financial metrics in a competitive market by using data mining and machine learning algorithms to sell used cars effectively.

### 3. Goal
The goal of this project is to generate insights using Exploratory Data Analysis and see what variables affect the pricing of the used car. Secondly, the aim is to use the historical data to make predictions on the price of the used car using Regression. This model can then be deployed to predict real world cases of used cars and propel data driven decision making.

### 4. Data Preprocessing
<img width="791" alt="Screenshot 2023-11-05 at 12 51 38 PM" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/8610e137-83c5-465b-808a-eceaea679870">
The dataset was analyzed and found that five categorical variables containing missing values as shown in the figure.

<img width="860" alt="image" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/bbd5ccf8-5907-44b5-a9d3-2a0a516a7e52">
The heatmap shown in Figure, describes the correlation between null values in one column and the null values or data values in the corresponding columns. If there are null values in both columns, then the correlation is positive. On the other hand, if there are null values in one column and data values in other column then the correlation is weak or towards the negative value. The missing values were imputed using mode values of the respective columns.

### 5. Outlier Analysis
<img width="823" alt="image" src="https://github.com/hamzahasan13/Data-Driven-Analytics/assets/114373000/fdd7720f-1fe1-499f-bf4f-4d255560ef94">

Numerical variables, Price, Horsepower and Kilometer, were checked for outliers and then fixed by removing values that were greater than 3 standard deviations above the mean. 

### 6. A/B Testing


