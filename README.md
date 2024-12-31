# EDA-Data-Preprocessing-on-Google-App-Store-Rating-Dataset-Using-Python

## Problem Statement

The Play Store apps data has enormous potential to drive app-making businesses to success.However, many apps are being developed every single day and only a few of them become profitable. It is important for developers to be able to predict the success of their app and incorporate features which makes an app successful. Before any such predictive-study can be done, it is necessary to do EDA and data-preprocessing on the apps data available for google app store applications. From the collected apps data and user ratings from the app stores, let's try to extract insightful information. 

## Objective

This project focuses on the exploratory data analysis (EDA) and preprocessing of the Google Play Store Apps dataset. The goal is to clean, transform, and explore the dataset, making it ready for machine learning and predictive analytics tasks.

## Dataset Information

The dataset contains more than **10,000 apps** data and includes the following columns: 


| **Column**        | **Description**                                             |
|-------------------|-------------------------------------------------------------|
| **App**           | Name of the app.                                            |
| **Category**      | Category to which the app belongs.                          |
| **Rating**        | Average user rating of the app.                             |
| **Size**          | Size of the app in bytes.                                   |
| **Installs**      | Number of installations.                                    |
| **Type**          | Whether the app is free or paid.                            |
| **Price**         | Price of the app (if paid).                                 |
| **Content Rating**| Age-based content rating of the app (e.g., 'Everyone', 'Teen'). |
| **Genres**        | Genres associated with the app.                              |
| **Last Updated**  | Date when the app was last updated.                         |
| **Current Ver**   | The current version of the app.                             |
| **Android Ver**   | Minimum Android version required for the app.               |


# Steps Involved in the Project

## 1. Data Import and Overview
Essential libraries like Pandas, NumPy, Matplotlib, and Seaborn are imported to perform the analysis. The dataset is read into a Pandas DataFrame.
The first 5 and last 5 records of the dataframe are retrieved for an initial view.

## 2. Dataset Information and Shape
Checked the shape, data types and structure of the dataframe.

## 3. Summary Statistics
Generated summary statistics for numerical columns to understand the central tendency, spread, skewness and distribution of data.
Generated summary statistics for categorical columns to understand the count (total records), unique (Distinct Category Value), top (mode), and freq (frequency).

## 4. Handling Duplicate Records
Checked for the presence of the duplicate records.
If duplicates records are present, then all the duplicate records are removed.

## 5. Cleaning the 'Category' Column
Inspect the 'Category' column for invalid or irrelevant categories and clean it accordingly.

## 6. Handling Missing Values in 'Rating'
Identify and handle missing values in the 'Rating' column. Missing ratings are dropped, and a new column 'Rating_category' is created by classifying ratings into 'High' (>3.5) and 'Low' (<=3.5).

## 7. Distribution of 'Rating_category'
Analyze and visualize the distribution of the 'Rating_category' column.

## 8. Handling 'Reviews' Column
Converted the 'Reviews' column to a numeric data type. To check for presence of outliers, a boxplot is plotted. Since the column has outlier, applied a log transformation to handle outliers.

## 9. Clean and Convert 'Size' Column
The 'Size' column contains alphanumeric values.Treating this column by converting the values to numerical format (M = million, K = thousand), and droped rows where 'Size' is marked as 'Varies with device'.

## 10. Clean and Convert 'Installs' Column
Inspect the 'Installs' column for unwanted characters, if unwanted characters are present, then treat the unwanted characters and convert the column to integers.

## 11. Clean and Convert 'Price' Column
clean the 'Price' column by removing the '$' symbol and convert the remaining values to numeric data.

## 12. Droping Redundant Columns
Redundant columns such as 'App', 'Rating', 'Genres', 'Last Updated', 'Current Ver', and 'Android Ver' are dropped to focus on relevant features.

## 13. Encoding Categorical Columns
Categorical columns such as 'Category', 'Content Rating', and 'Type' are encoded using appropriate encoding techniques (e.g., label encoding, one-hot encoding).

## 14. Split Data into Features and Target
The data is split into independent features and a target variable ('Rating_category').

## 15. Split the dataset into train and test
The dataset is split into 2 parts. Training and Testing dataset.

## 16. Standardizing the Data
The features are standardized using `StandardScaler` to ensure that they are on the same scale, improving the performance of machine learning models.
