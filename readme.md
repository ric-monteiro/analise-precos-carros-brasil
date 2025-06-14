# Analysis and Prediction of Vehicle Prices in Brazil

-----

## Project Description

This project was developed as a group assignment for the Applied Programming Language course, part of the postgraduate program in Applied Artificial Intelligence at the Federal University of Paraná. Its objective is to perform a detailed exploratory analysis and build machine learning models to predict the average prices of cars in the Brazilian market. Using a vehicle dataset, we explored various features and applied regression algorithms to identify the most influential factors in pricing and to achieve the best prediction accuracy.

-----

## Project Participants

  * Francisco Viana
  * Gabriel Godinho
  * Guilherme Bilibio
  * José Augusto Viana
  * Ricardo Monteiro
  * Rodrigo Dittmar

## Professor

Prof. Dr. Luani de Oliveira Rosa Piva

-----

## Objectives

  * Perform data preprocessing and cleaning, handling missing values and transforming variables.
  * Conduct an exploratory data analysis (EDA) to extract insights about the price distribution and the relationship between vehicle characteristics.
  * Develop and train regression models (RandomForest Regressor and XGBoost Regressor) to predict car prices.
  * Evaluate and compare the performance of the models using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and Coefficient of Determination (R²).
  * Identify the most important variables for determining vehicle prices.

-----

## Data Sources

  * `precos_carros_brasil.csv`: Main dataset containing information about various car models, their characteristics (brand, model, year, engine, transmission, fuel, etc.), and prices.
  * `metadados.xlsx - metadados.csv`: File containing the description of the columns present in the main dataset, aiding in the understanding of the variables.
  * The original dataset was extracted from the [Kaggle](https://www.kaggle.com/datasets/vagnerbessa/average-car-prices-bazil/data) website. It was adapted for use in this exercise.

-----

## Methodology

1.  **Library Installation and Import:** Setting up the environment with the necessary Python libraries (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost).
2.  **Data Loading and Initial Inspection:** Reading the datasets and a first look at the structure and data types.
3.  **Data Preprocessing and Cleaning:**
      * Handling missing values (using median for numerical data and mode for categorical data).
      * Removing duplicates.
      * Transforming categorical variables into numerical ones (Label Encoding and One-Hot Encoding).
4.  **Exploratory Data Analysis (EDA):**
      * Descriptive statistical analysis of the variables.
      * Visualization of the price distribution.
      * Investigation of the relationship between price and other characteristics such as brand, transmission type, fuel type, and model year.
5.  **Feature Engineering (if applicable):**
      * Selection of the most relevant features for modeling.
6.  **Data Splitting:** Separating the dataset into training and testing sets.
7.  **Model Training:**
      * RandomForest Regressor
      * XGBoost Regressor
8.  **Model Evaluation:**
      * Calculation of MAE, MSE, and R² metrics for both models on the test set.
      * Performance comparison to determine the best model.
9.  **Variable Importance Analysis:** Identification of the features that contribute most to the models' predictions.

-----

## Main Results and Conclusions

  * **Data Handling:** Missing values were treated with median and mode, and no duplicates were found after the initial removal.

  * **Exploratory Analysis:**

      * Brands with higher prices tend to have more expensive automatic models.
      * More expensive brands generally offer gasoline and flex-fuel models, while alcohol-powered models tend to be cheaper.

  * **Model Performance:**

      * **RandomForest Regressor:**
          * MAE: 4899.3127
          * MSE: 96211948.1803
          * R² Score: 0.9515
      * **XGBoost Regressor:**
          * MAE: 4515.4686
          * MSE: 87097148.4247
          * R² Score: 0.9561

  * **Best Model:** The **XGBoost Regressor** model showed the best overall performance, with an R² (coefficient of determination) of 0.9561, indicating a high capacity to explain the variability in car prices.

  * **Variable Importance:**

      * In the RandomForest model, `brand` and `engine_size` were the most important.
      * In the XGBoost model, `engine_size` and `fuel` (fuel type) had the greatest impact.

The analyses and the developed models provide relevant insights into the factors that determine car prices in Brazil and demonstrate the ability of machine learning models to make accurate predictions.
