# Retail Data Analysis
This project demonstrates the entire workflow of Data Cleaning, Exploratory Data Analysis and Dashboarding. The project is written in Python, originally in a Kaggle Notebook. The main goal of this project is to take raw, unclean data, then clean it, and draw actionable insights from the data. The raw data was sourced from Kaggle, and can be found at the link provided below. The following sections illustrate the main highlights of the project:

## Dataset Description
The dataset simulates real world sales data, spanning across 25 individual customers and 8 product categories. The data is recorded in the form of individual transactions over 4 years. It comes with intentionally skipped and often noisy values, to mimic the dirtiness of real data.

### Technical Description
1. **Number of rows** : 12,575
2. **Number of columns** : 11

#### Columns and their description
1. Transaction ID : Primary key. Uniquely identifies each transaction
2. Customer ID : Identifies each of the 25 customers
3. Category : Category of the item purchased
4. Item : The actual item purchased. Stored as unique Item numbers dependent on category and price
5. Price Per Unit : Price of one unit of the item
6. Quantity : How many of that item was purchased
7. Total Spent : Total amount spent on the purchase. Product of quantity and price per unit
8. Payment Method : Method of payment, such as cash, card or online wallet
9. Location : Location of purchase, in-store or online
10. Transaction Date : Date of the transaction
11. Discount Applies : Whether or not a discount was applied to the transaction.

#### Dataset link : https://www.kaggle.com/datasets/ahmedmohamed2003/retail-store-sales-dirty-for-data-cleaning

## Tools & Technologies
- Python (Pandas, NumPy, Matplotlib)
- Kaggle Notebook
- Power BI
- GitHub
  
## Data Cleaning
The data had a lot of missing values, which needed to be imputed. **Custom imputation** strategies were used, instead of regular mean, median or mode imputation. Strategies for imputation were based on data relationships, mentioned in data documentation. Imputation code can be found in the Python notebook. The following columns in the data consisted of missing data:
1. **Price Per Unit** : Filled by dividing total price by quantity
2. **Item** : Filled from price and category
3. **Quantity and Total Spent** : Less than 5% of total data, so records having missing values were dropped.
4. **Discount applied** : Missing values may indicate no discounts being applied, so imputed with `False`.

Data types of `Transaction date` and `discount applied` were changed from object to _Datetime_ and _boolean_, respectively

## How to Run
1. Open `Data_cleaning_and_EDA.ipynb` in Jupyter or Kaggle to view the full workflow.
2. Open `Retail Sales Dashboard.pbix` in Power BI Desktop to explore the dashboard.
3. Cleaned dataset is available as `Retail_data_cleaned.csv`.

## Results
The cleaned dataset (available here) was used to extract insights about the sales made. The key findings were visualised as a three-page PowerBI dashboard, having categorical, customer oriented, and chronological analysis. Some of the main observations made were:

1. Category wise popularity
2. Total expenditure contributed by each category
3. Average sales per category
4. Customer wise monthly purchase trends (filtered by category)
5. Decomposition of total expenditure by other factors
6. Top paying customers
7. Trends of location and payment methods over months or years

## License
This cleaned dataset is licensed under **CC BY-SA 0.4**
