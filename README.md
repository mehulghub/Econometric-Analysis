# Econometric-Analysis
# Impact of US Tariffs on prices of imported Chinese goods 2025

This project analyzes the impact of US tariffs on the import price index of goods from China in 2025. It uses historical tariff data and import price index data to build a linear regression model and predict the import price index for May 2025.

## Project Overview

The project performs the following steps:

1. **Data Loading and Preparation:**
   - Loads two CSV files: "Tariff Categories.csv" (containing tariff category information) and "US Tariffs on CHINA.csv" (containing monthly tariff data).
   - Handles missing values in the tariff categories data.
   - Converts dataframes to NumPy arrays for matrix operations.

2. **Weighted Average Tariff Calculation:**
   - Calculates the weighted average tariff for the first five months of 2025 based on the tariff categories and the number of days each tariff category was active.

3. **Import Price Index Data Loading and Preparation:**
   - Loads the "CHNTOT.csv" file, which contains the US Import Price Index for goods from China.
   - Sets the 'observation_date' column as the index.

4. **Exploratory Data Analysis:**
   - Visualizes the weighted average tariff over the first five months of 2025.
   - Visualizes the import price index over the same period.

5. **Linear Regression Modeling:**
   - Splits the data into training and testing sets. The first four months of data are used for training, and the fifth month (May) is used for testing/prediction.
   - Fits a linear regression model (Ordinary Least Squares) to predict the Import Price Index based on the Weighted Average Tariff.
   - Prints a summary of the regression model.

6. **Prediction and Visualization:**
   - Predicts the Import Price Index for May 2025 using the fitted model and the calculated weighted average tariff for May.
   - Visualizes the trained data points, the regression line, and the predicted data point for May.

## Requirements

- Python 3
- pandas
- numpy
- matplotlib
- statsmodels

## Data Files

- `Tariff Categories.csv`: Contains information about US tariff categories.
- `US Tariffs on CHINA.csv`: Contains number of days for each month for which each US tariff category was active on goods from China.
- `CHNTOT.csv`: Contains the US Import Price Index for goods from China.


## Running the Code

1. Save the code from the Colab notebook as a Python file (e.g., `tariff_analysis.py`).
2. Make sure the data files (`Tariff Categories.csv`, `US Tariffs on CHINA.csv`, `CHNTOT.csv`) are in the same directory as the Python file.
3. Run the Python file from your terminal.
