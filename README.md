# flight_delay
This project is about regression analysis using flight delay analysis
# Flight Delay Prediction Project

## Description
This project involves predicting whether a flight will be delayed based on various factors like departure time, airline, and weather conditions. It provides an introduction to regression analysis and time-series data.

## Objective
To develop a regression model to predict flight delays using historical flight data.

## Project Steps

### 1. Data Collection and Loading
- Dataset downloaded from Kaggle.
- Loaded using Python libraries like `pandas`.

### 2. Data Preprocessing
- Checked for missing values and calculated the percentage of null values.
- Selected numerical columns for correlation analysis.
- Dropped unnecessary columns:
  - Columns dropped: `YEAR`, `MONTH`, `DAY`, `DAY_OF_WEEK`, `FLIGHT_NUMBER`, `SCHEDULED_DEPARTURE`, `SCHEDULED_TIME`, `ELAPSED_TIME`, `AIR_TIME`, `DISTANCE`, `WHEELS_ON`, `SCHEDULED_ARRIVAL`, `ARRIVAL_TIME`, `DIVERTED`, `CANCELLED`, `SECURITY_DELAY`, `TAIL_NUMBER`, `ORIGIN_AIRPORT`, `DESTINATION_AIRPORT`, `DEPARTURE_TIME`, `TAXI_OUT`, `WHEELS_OFF`, `TAXI_IN`, `CANCELLATION_REASON`.
- Filled missing values with zeros.
- Performed one-hot encoding for the `AIRLINE` column.

### 3. Exploratory Data Analysis
- Generated scatter plots to visualize relationships between:
  - `DEPARTURE_DELAY` and `ARRIVAL_DELAY`
  - `AIR_SYSTEM_DELAY` and `ARRIVAL_DELAY`
  - `AIRLINE_DELAY` and `ARRIVAL_DELAY`
  - `LATE_AIRCRAFT_DELAY` and `ARRIVAL_DELAY`
  - `WEATHER_DELAY` and `ARRIVAL_DELAY`

### 4. Model Training and Evaluation
#### Linear Regression
- Features (`X`) and target (`y`) defined.
- Split data into training (80%) and testing (20%) sets.
- Trained a `LinearRegression` model.
- Model evaluation:
  - Mean Absolute Error (MAE): Computed
  - Root Mean Squared Error (RMSE): Computed

#### Decision Tree Regressor
- Initialized a `DecisionTreeRegressor`.
- Trained the model and evaluated it using:
  - Mean Absolute Error (MAE): Computed
  - Root Mean Squared Error (RMSE): Computed
- Visualized feature importance using a horizontal bar chart.
- Plotted Actual vs Predicted Arrival Delays.

## Results
- **Linear Regression**:
  - MAE and RMSE values were calculated to measure the model's performance.
- **Decision Tree Regressor**:
  - MAE and RMSE values were calculated.
  - Visualized feature importance to understand the contribution of individual features.
  - Compared actual and predicted values using scatter plots.

## Libraries Used
- pandas
- numpy
- matplotlib
- scikit-learn

## Conclusion
This project demonstrates how to preprocess flight delay data, perform exploratory data analysis, and build regression models to predict flight delays. The feature importance and scatter plots provide insights into the factors affecting flight delays.

## Future Work
- Experiment with additional regression models like Random Forest, Gradient Boosting, or XGBoost.
- Optimize hyperparameters of the models to improve prediction accuracy.
- Incorporate external data sources such as weather forecasts for enhanced feature engineering.

