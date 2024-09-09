# Developing a Predictive Machine Learning Pipeline for London's Climate

## Project Description
As climate change continues to impact global weather patterns, accurate weather forecasting has become increasingly critical for various industries. This project aims to develop a machine learning pipeline to predict the climate in London, England, with a focus on forecasting the mean temperature in degrees Celsius (°C).

Given the complexity of weather prediction, multiple experiments are required to determine the most effective approach. The project involves testing various regression models to predict the mean temperature, utilizing a combination of Scikit-learn and MLflow for model development and tracking.

The dataset, stored in "london_weather.csv," includes the following columns:
- **date** – the recorded date of measurement (**int**)
- **cloud_cover** – cloud cover in oktas (**float**)
- **sunshine** – sunshine duration in hours (hrs) (**float**)
- **global_radiation** – irradiance in Watts per square meter (W/m²) (**float**)
- **max_temp** – maximum temperature in degrees Celsius (°C) (**float**)
- **mean_temp** – the **target** variable, mean temperature in degrees Celsius (°C) (**float**)
- **min_temp** – minimum temperature in degrees Celsius (°C) (**float**)
- **precipitation** – precipitation in millimeters (mm) (**float**)
- **pressure** – atmospheric pressure in Pascals (Pa) (**float**)
- **snow_depth** – snow depth in centimeters (cm) (**float**)

**Key Tools**: Python (Pandas, NumPy, MLflow, Matplotlib, Seaborn, Scikit-learn)

## Analysis
The dataset contains 15,341 entries across 10 columns, with 9 columns of type `float64` and 1 column of type `int64`. While most columns have nearly complete data, some contain missing values. To quantify the missing data, the total entry count (15,341) was compared to the non-null counts for each column.

Here is the breakdown of missing values:
- **"cloud_cover"** and **"global_radiation"** each have 19 missing values (15,341 total entries - 15,322 non-null).
- **"max_temp"** and **"precipitation"** each have 6 missing values (15,341 total entries - 15,335 non-null).
- **"mean_temp"** has 36 missing values (15,341 total entries - 15,305 non-null).
- **"min_temp"** has 2 missing values (15,341 total entries - 15,339 non-null).
- **"pressure"** is missing 4 values (15,341 total entries - 15,337 non-null).
- **"snow_depth"** has the most missing data, with 1,441 missing values (15,341 total entries - 13,900 non-null).

This summary highlights the extent of missing data in each column.

### Model Performance Comparison

The performance of three regression models was evaluated based on Root Mean Squared Error (RMSE):

| Model                     | RMSE     |
|----------------------------|----------|
| Linear Regression           | 0.9166   |
| Decision Tree Regressor     | 1.2662   |
| Random Forest Regressor     | 0.9189   |

## Conclusion
The experiment results indicate that the **Linear Regression** model achieved the lowest RMSE of **0.9166**, demonstrating the best predictive accuracy among the models tested. The **Random Forest Regressor** followed closely with an RMSE of **0.9189**. In contrast, the **Decision Tree Regressor** had the highest RMSE at **1.2662**, making it the least accurate model in this comparison.
