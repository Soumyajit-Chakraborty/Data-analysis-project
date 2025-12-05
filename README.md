# Retail Data Analysis
This project demonstrates the entire workflow of Data Cleaning, Explorartory Data Analysis and Dashboarding. The project is done in Python, and written originally in a Kaggle Notebook. The main goal of this project was to take raw, unclean data, then clean it, and draw actionable insights from the data. The raw data was taken from Kaggle. Follow the given link for the raw data : https://www.kaggle.com/datasets/ahmedmohamed2003/retail-store-sales-dirty-for-data-cleaning

## Data Cleaning
The data had a lot of missing values, which needed to be imputed. **Custom imputation** strategies were used, instead of regular mean, median or mode imputation. Strategies for imputation were based on data relationships, mentioned in data documentation. Imputation code can be found in the Python notebook. The following columns in the data consisted of missing data:
1. **Price Per Unit** : Filled by dividing total price by quantity
2. **Item** : Filled from price and category
3. **Quantity and Total Price** : Less than 5%, so dropped records having missing values
