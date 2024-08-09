# 1. Problem
House price predictions are very important for investors to make decisions of buying houses. There are many features which play roles in house price decisions. Based on historical data of house sales in different regions in the U.S., we need to predict house price based on features.

Which features can significantly affect housing prices?

Build a model in one month to reflect on the relationships between price of houses and the features.

# 2. Dataset Overview

This dataset has a total of 1,401,066 entries and 10 columns. The columns include a mix of object and float64 data types, with some missing values across several columns.

Here's a quick summary of each column:
    status: A categorical column (likely containing strings) with no missing values.
    bed: A numerical column (floating-point) with some missing values (around 1,216,528 non-null values).
    bath: Another numerical column with some missing values.
    acre_lot: A numerical column representing lot sizes, with a significant number of missing values.
    city: A categorical column with very few missing values.
    state: A categorical column without missing values.
    zip_code: A numerical column representing zip codes with some missing values.
    house_size: A numerical column with substantial missing values.
    prev_sold_date: A date column represented as an object, with a large number of missing values.
    price: A numerical column with few missing values.

# 3. Data Cleaning
•	Handle Missing Values: Decide on strategies to fill missing values in numerical and categorical columns.
•	Convert Data Types: Convert prev_sold_date from an object to a datetime type.
•	Outlier Detection: Identify and potentially remove or adjust outliers in numerical columns like price, acre_lot, or house_size.

# 4. Exploratory Data Analysis (EDA)
•	Summary Statistics: Calculate mean, median, and mode for numerical columns.
•	Visualizations: Use histograms, box plots, and scatter plots to understand the distribution of numerical data.
•	Correlation Analysis: Explore correlations between price and other numerical features.

# 5. Feature Engineering
•	Create New Features: Use existing columns to create new features, like 'average_acre_lot','average_house_size',etc.
•	Encode Categorical Variables: Convert status, city, zip_code, and state into numerical formats for machine learning tasks.

# 6. Machine Learning Models
•	Regression Models: Predict price based on other features using linear regression.
          Model Performance:
          Mean Squared Error: 0.8443409875971409
          R^2 Score: 0.15328624829493187
•	Random Forest Model: 
          Model Performance:
          Mean Squared Error: 0.014193229245588218
          R^2 Score: 0.9857668849909297
•	Neural Networks Model: 
          Model Performance:
          Mean Squared Error: 0.3350867183075398
          R^2 Score: 0.6639716221616279
   Comparing the prediction performance of the three models, random forest has the best prediction effect, with a prediction accuracy of 99%，We recommend choosing the random forest model as the prediction model.