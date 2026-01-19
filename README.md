# weather-temperature-prediction
Exploratory Data Analysis and temperature prediction using Linear, Ridge, and Lasso Regression. Models are evaluated using MSE and R² with visualizations for correlation analysis and performance comparison.

## 1.Identified Problem
Weather data contains multiple variables such as humidity, wind speed, pressure, visibility, and location, all of which influence temperature. However, the relationship between these variables and temperature is not always obvious. Additionally, real-world weather data often includes missing values, outliers, and correlated features, which can affect prediction accuracy. The challenge is to analyze these weather factors effectively and build a reliable model that can accurately predict temperature.

## 2.Research Question
How accurately can temperature be predicted from weather variables using linear and regularized regression models?

## 3.Dataset
File used: weather_data_extended.csv
The dataset includes weather information from different locations with the following attributes:
Location
Temperature (°C)
Feels Like (°C)
Humidity (%)
Wind Speed (kph)
Cloud Cover (%)
Pressure (mb)
UV Index
Visibility (km)

## 3.Exploratory Data Analysis (EDA)
To understand the dataset better, several EDA steps were performed:
Initial inspection using info() and head()
Checking and handling missing values
Generating summary statistics using describe()
Converting the categorical Location column into numeric form
Studying relationships between variables using a correlation heatmap
Identifying potential outliers using box plots
These steps helped in understanding data distribution, correlations, and data quality issues.

## 4.Feature Engineering
The following feature engineering steps were applied:
Encoded the Location column as a numeric feature (Location_index)
Selected the most relevant features for prediction:
Humidity (%)
Wind Speed (kph)
Pressure (mb)
Visibility (km)
Location_index

Used RobustScaler to scale features and reduce the impact of outliers

## 5.Model Building
The dataset was divided into training (80%) and testing (20%) sets to evaluate model performance on unseen data.
The following regression models were trained and compared:
Simple Linear Regression
Ridge Regression (L2 regularization)
Lasso Regression (L1 regularization)

## 6.Model Evaluation
Model performance was evaluated using:
Mean Squared Error (MSE) – to measure prediction error
R-squared (R²) Score – to measure how well the model explains temperature variation
Results Summary
Model	MSE	R² Score
Simple Linear Regression	1.94	0.94
Ridge Regression	1.94	0.94
Lasso Regression	2.04	0.94

## 7.Visualizations
Several visualizations were created to support the analysis:
Correlation heatmap to study relationships between variables
Box plots to inspect outliers
Scatter plot comparing Actual vs Predicted Temperature
Bar chart comparing model performance using MSE and R²

## 8.Conclusion

Among the models tested, Simple Linear Regression produced the best results with the lowest Mean Squared Error and a high R² score of 0.94, meaning it explains 94% of the variation in temperature. Ridge Regression performed almost identically, suggesting that multicollinearity was not a major issue in the dataset. Lasso Regression slightly reduced accuracy due to feature shrinkage. Based on these results, Simple Linear Regression was chosen as the final model.
