Home Sales Analysis with PySpark

In this challenge, I utilized PySpark and SparkSQL to analyze home sales data, compute key metrics, and optimize data processing through techniques like caching and partitioning. 

Following steps are taken to complete the assignment.
The tasks involved:
 Creating a temporary table from home sales data.
 Running several SQL queries to derive insights.
 Using caching to improve performance.
 Partitioning data for optimized querying.
 Verifying caching and uncaching operations.

Files
The following files were used to complete this project:
 home_sales_revised.csv (Home sales data)
 Home_Sales.ipynb (Jupyter Notebook where the assignment was completed)

Instructions for Completion
1. The starter notebook Home_Sales_starter_code.ipynb was renamed to Home_Sales.ipynb.
2. Importing PySpark Functions: Imported the necessary PySpark SQL functions to execute SQL-like operations on the DataFrame.
3. Loading Data into a DataFrame: Read the home_sales_revised.csv data into a Spark DataFrame for
further analysis.
4. Creating a Temporary Table: Created a temporary table named home_sales from the loaded
DataFrame to run SQL queries.

SQL Queries and Analysis: Using SparkSQL, I answered the following questions:

1. Average price for four-bedroom houses sold for each year: Calculated the average price for homes with four bedrooms, rounding off to two decimal places.

2. Average price of homes by year built (three bedrooms, three bathrooms): Found the average price of homes for each year they were built, with the condition of three bedrooms and three bathrooms. Results were
rounded to two decimal places.

3. Average price for homes by year built (three bedrooms, three bathrooms, two floors, ≥ 2,000 sq ft):
Calculated the average price of homes with three bedrooms, three bathrooms, two floors, and a minimum of 2,000 square feet, and rounded off the result.

4. Found the  average price of a home per "view" rating having an average home price greater than or equal to $350,000

Caching for Optimization
5. Caching the Temporary Table:
o Cached the home_sales temporary table to optimize repeated queries.
6. Checking Cache Status:
o Verified if the table was successfully cached.
7. Query Execution on Cached Data:
o Re-ran the query to calculate the average price per &quot;view&quot; rating for
homes priced $350,000 or more using cached data. Compared the
runtime with the uncached version.

Data Partitioning
8. Partitioning by Date Built:
o Partitioned the home sales data by the date_built field and saved it in
parquet format.

9. Creating a Temporary Table for Partitioned Data:
o Created a temporary table from the partitioned parquet data.
10. Executing Queries on Partitioned Data:
Ran the query to calculate the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determined the runtime and compare it to uncached runtime. Compared the
runtime to both the cached and uncached versions.

11. Uncaching the Temporary Table: Uncached the home_sales temporary table to free up memory resources.
12. Verifying Uncaching:  Verified that the table had been uncached using PySpark commands.