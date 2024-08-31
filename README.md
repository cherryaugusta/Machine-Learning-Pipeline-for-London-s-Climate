# Developing a Predictive Machine Learning Pipeline for London's Climate

As climate change continues to affect global weather patterns, accurate weather prediction has become increasingly vital for businesses. This project focuses on supporting the development of a machine learning pipeline to forecast the climate in London, England, with a specific emphasis on predicting the mean temperature in degrees Celsius (°C).

Given the complex nature of weather prediction, numerous experiments must be conducted to identify the most effective approach. The project entails experimenting with various regression models to predict mean temperature, leveraging a combination of sklearn and mlflow.

The dataset for this project, stored in "london_weather.csv," includes the following columns:
- **date** - the recorded date of measurement (**int**)
- **cloud_cover** - cloud cover in oktas (**float**)
- **sunshine** - sunshine duration in hours (hrs) (**float**)
- **global_radiation** - irradiance in Watts per square meter (W/m²) (**float**)
- **max_temp** - maximum temperature in degrees Celsius (°C) (**float**)
- **mean_temp** - **target** variable, mean temperature in degrees Celsius (°C) (**float**)
- **min_temp** - minimum temperature in degrees Celsius (°C) (**float**)
- **precipitation** - precipitation in millimeters (mm) (**float**)
- **pressure** - atmospheric pressure in Pascals (Pa) (**float**)
- **snow_depth** - snow depth in centimeters (cm) (**float**)
