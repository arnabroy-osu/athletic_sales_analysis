# Title
Module 5 Athletic_sales_analysis

## Source Data
The source is athletic sales data over 2 Years: 2020 & 2021 provided in the form of a csv files located in the Resources folder, 1 each for Year of Sales. Both the files have same list of columns containing Sales, Profit retailer, invoice date & geographic information. The columns are: retailer, retailer_id, invoice_date, region, state, city, product, price_per_unit, units_sold, total_sales, operating_profit, sales_method.

## Desired Outcome of the exercise
The desired outcome of the exercise is to analyze the sales data through Pandas dataframes and answer the following questions fpr the 2 years of sales data:
1. Top N-regions with most number of Products sold
2. Top N-regions with highest total sales.
3. Top N-retailers with highest total sales.
4. Top N-retailers with highest total sales for women's athletic footwear ONLY.
5. Days and weeks over 2 Years that have highest total sales for Women's Athletic Footwear ONLY.

## Data Preparation
The 2 csv files are read into 2 pandas dataframe. We used pandas concat function to combine the two DataFrames on the rows as both the csv files have same columns in same order and same data type. The combined DataFrame is then cehcked for NULL values and data types of the columns. The Invoice Date field is converted to date time datatype for efficient Data wrangling/transformation. The combined data frame is also further filtered on Product = Women's Athletic Footwear, to anwser questions 4 & 5.

## Data Analysis & Conclusion
We used both groupby & pivot function to group the combined 2 years worth of data by Retailer, Region, State, City as required to answer the questions to get the top N regions & retailers.
We also used resample function on Invoice Date Index to group the data by Days & Weeks (Daily & Weekly Bins) to get the top N Days/weeks with highest total sales for Women's Athletic Footwear ONLY. The top-N Retailer, Regions, days/Weeks with highest totals sales and number of products sold (Question 1, 2, 3, 4 & 5) will be displayed in a tabular format when you run the code (athletic_sales_analysis_starter_code.ipynb)




