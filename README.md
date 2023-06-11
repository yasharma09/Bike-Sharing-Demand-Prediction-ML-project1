Bike-sharing systems are a means of renting bicycles. Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort.

It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing a stable supply of rental bikes becomes a major concern, which will grow the business of bike sharing. The crucial part is the prediction of the bike count required at each hour for the stable supply of rental bikes, so it's a need of the hour to solve this problem. The bike-sharing rental process is highly correlated to the environmental and seasonal settings. For instance weather conditions, day of the week, season, hour of the day, etc. can affect the rental behaviors. Therefore, the proposed model will predict the demand for rental bikes given information about the weather and time of the day.
Bike-Sharing-Demand-Prediction
This project aims to enhance the mobility and convenience of the public through bike-sharing programs in metropolitan areas. One of the main challenges is maintaining a consistent supply of bikes for rental.

Table of Content
Problem Statement
Dataset
Data Pipeline
Project Structure
Conclusion
Problem Statement
Many metropolitan areas now offer bike rentals to improve mobility and convenience. Ensuring timely access to rental bikes is critical to reducing wait times for the public, making a consistent supply of rental bikes a major concern. The expected hourly bicycle count is particularly crucial in this regard. We have to build a Regression model to predict the number of bikes required at any point of time.

Dataset
The dataset is from Seoul's Bike Sharing Program. The data set includes over 8000 records and 14 attributes based on historical usage patterns, including temperature, time, and other data. For more information on the dataset, please visit the website at (https://github.com/yasharma09/Bike-Sharing-Demand-Prediction-ML-project1/blob/main/SeoulBikeData.csv)

Data Pipeline
Analyze Data: In this initial step, we attempted to comprehend the data and searched for various available features. We looked for things like the shape of the data, the data types of each feature, a statistical summary, etc. at this stage.
EDA: EDA stands for Exploratory Data Analysis. It is a process of analyzing and understanding the data. The goal of EDA is to gain insights into the data, identify patterns, and discover relationships and trends. It helps to identify outliers, missing values, and any other issues that may affect the analysis and modeling of the data.
Data Cleaning: Data cleaning is the process of identifying and correcting or removing inaccuracies, inconsistencies, and missing values in a dataset. We inspected the dataset for duplicate values. The null value and outlier detection and treatment followed. For the outliers, we used the Clipping method to handle the outlier without any loss to the data.
Feature Engineering: At this step, we did the encoding of categorical features. We used the correlation coefficient and VIF analysis to remove multi-colinearity and to select the most relevant features. we used a square root transformation for the target variable as it transformed the variable into a well-distributed form.
Model Training and Implementation:
We scaled the features to bring down all of the values to a similar range. We pass the features to 11 different regression models. We also did hyperparameter tuning using GridSearchCV.
Performance Evaluation: After passing it to various regression models and calculating the metrics, we choose a final model that can make better predictions. We evaluated different performance metrics but choose our final model using the r2 score and adj r2 score.
Project Structure
├── README.md
├── Dataset 
│   ├── [SeoulBikeData.csv](https://github.com/yasharma09/Bike-Sharing-Demand-Prediction-ML-project1/blob/main/SeoulBikeData.csv)
├── Problem Statement
│
├── Know Yoour Data
│
├── Understanding Your Variables
│
├── EDA
│   ├── Numeric & Categorical features
│   ├── Univariate Analysis
│   ├── Bivariate and Multivariate Analysis
│
├── Data Cleaning
│   ├── Duplicated values
│   ├── Missing values
│   ├── Skewness
│   ├── Treating Outliers
│
├── Feature Engineering
│   ├── Regression Plot
|   ├── Correlation Coefficient and Heatmap
|   ├── Encoding
|   ├── Normalization of Target Variable
│
├── Model Building
│   ├── Train Test Split
|   ├── Scaling Data
|   ├── Model Training
│
├── Model Implementation
│   ├── Decision Tree
|   ├── Random Forest
|   ├── GVM Boost
│   ├── XGBoost   
