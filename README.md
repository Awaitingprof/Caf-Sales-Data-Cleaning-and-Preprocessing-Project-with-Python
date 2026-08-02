# Caf-Sales-Data-Cleaning-and-Preprocessing-Project-with-Python
A comprehensive end-to-end data cleaning, preprocessing, validation, and quality assurance project performed in Python using Pandas and NumPy to transform raw café transaction data into a clean, consistent, and analysis-ready dataset.

## Project Overview

Data is only as valuable as its quality.

This project shows a data cleaning workflow by applying industry-standard preprocessing techniques to a café sales transaction dataset. The goal was to identify and resolve data quality issues while preserving the integrity of the original information.

Rather than performing simple data replacement, the cleaning process follows a logical and business-driven approach. Missing numerical values were reconstructed using relationships between existing variables whenever possible before applying statistical imputation methods. This ensures the cleaned dataset remains both accurate and analytically reliable.

The final output is a fully cleaned dataset that is ready for:

Business Intelligence reporting
Dashboard development
Exploratory Data Analysis (EDA)
Statistical analysis
Machine Learning
Predictive modelling
Business decision-making

## Project Objectives

The primary objectives of this project were to:

- Identify common data quality issues in transactional sales data
- Apply systematic data cleaning techniques using Python
- Improve data consistency and reliability
- Preserve business logic during preprocessing
- Produce an analysis-ready dataset suitable for downstream analytics

## Dataset
The dataset contains transactional records from a café, with each row representing a customer purchase.
<img width="939" height="482" alt="Image" src="https://github.com/user-attachments/assets/e1774512-b0bf-494b-a2e9-3d52574efdde" />


######Column             ######Description
Transaction_ID:     Unique identifier for each transaction
Item	              Product purchased by the customer
Quantity	          Number of items purchased
Price_Per_Unit    	Cost of a single item
Total_Spent	        Total amount paid for the transaction
Payment_Method	    Payment method used by the customer
Location	          Café branch where the purchase occurred
Transaction_Date	  Date of the transaction

## Data Quality Issues Identified

The raw dataset contained several realistic data quality problems commonly encountered in production environments, including:

- Missing values
- Invalid placeholder values (UNKNOWN, ERROR)
- Incorrect data types
- Numerical fields stored as text
- Missing transaction dates
- Inconsistent categorical values
- Potential duplicate records
- Incomplete transactional information requiring reconstruction

## Data Cleaning Process

The dataset was cleaned through the following structured workflow:

1. Data Inspection
Loaded the dataset
Examined dataset dimensions
Reviewed data types
Generated descriptive statistics
Assessed missing values
 2. Data Standardisation
Standardised column names
Removed unnecessary columns
Improved dataset consistency
3. Handling Invalid Values
Replaced placeholder values such as:
UNKNOWN and ERROR with proper missing values (NaN) for accurate processing.
4. Data Type Conversion
Converted columns into their appropriate data types:
- Numeric columns → Float
- Dates → Datetime
Categorical columns → String
5. Intelligent Missing Value Treatment
Instead of immediately using statistical imputation, missing numerical values were reconstructed using business logic:
- Total_Spent = Quantity × Price_Per_Unit
- Price_Per_Unit = Total_Spent ÷ Quantity
- Quantity = Total_Spent ÷ Price_Per_Unit
Any remaining missing numerical values were then imputed using the median to minimise the influence of skewed distributions.
Categorical variables were completed using the mode, while missing dates were imputed using the median transaction date.
6. Data Validation
Performed additional quality assurance by verifying:
- Missing values
- Duplicate records
- Numerical consistency
- Logical relationships between variables
- Valid value ranges

### Technologies Used
- Python
- Pandas
- NumPy
- Jupyter Notebook

### Project Outcome
After completing the preprocessing workflow:
- All missing values were successfully handled
- Invalid placeholder entries were removed
- Data types were corrected
- Numerical inconsistencies were resolved
- Duplicate records were checked
- The dataset was validated for analytical use

The resulting dataset is clean, consistent, and ready for business analytics, dashboard creation, statistical modelling, or machine learning applications.

<img width="1108" height="483" alt="Image" src="https://github.com/user-attachments/assets/0fd7ed8b-fbfe-4032-8d3c-d084a82ead73" />

## Skills Demonstrated
This project showcases practical skills in:
- Data Cleaning
- Data Preprocessing
- Data Validation
- Data Quality Assessment
- Missing Value Imputation
- Business Rule Engineering
- Data Type Conversion
- Feature Preparation
- Python Programming
- Pandas
- NumPy
- Analytical Problem Solving
