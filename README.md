# Dmart-Analysis
D-Mart Retail Data Analysis with PySpark
This project demonstrates the use of PySpark for analyzing a retail dataset that includes sales, product, and customer data. The objective is to clean, transform, and analyze the data to gain business insights such as total sales, customer behavior, and profitability.

📁 Dataset Description
Three CSV files are used:

Customer.csv: Customer information (e.g., Customer ID, Name, Age, Segment, Region)

Product.csv: Product details (e.g., Product ID, Category, Sub-Category)

Sales.csv: Sales records (e.g., Product ID, Sales, Quantity, Profit, Discount)

🛠️ Technologies Used
Apache Spark (PySpark)

Python 3

Databricks / Jupyter Notebook / VSCode

CSV files

🔧 Setup Instructions
Install PySpark

nginx
Copy
Edit
pip install pyspark
Clone this repository

bash
Copy
Edit
git clone https://github.com/your-username/dmart-pyspark-analysis.git
cd dmart-pyspark-analysis
Run the Notebook or Python Script

Ensure the Customer.csv, Product.csv, and Sales.csv are placed in /mnt/data/ or adjust the paths accordingly in the script.

Launch using Jupyter or any PySpark-compatible environment.

 Data Cleaning and Preparation
Cleaned column names by replacing spaces with underscores

Casted numerical columns to appropriate types (FloatType, IntegerType)

Joined the datasets using common keys (Product_ID, Customer_ID)

📊 Analytical Queries Performed
Total sales per product category

Customer with the highest number of purchases

Average discount across all sales

Unique products sold by region

Total profit per state

Top sub-category by sales

Average customer age by segment

Total orders shipped by mode

Total product quantity sold per city

Most profitable customer segment

📌 Sample Query
python
Copy
Edit
# Total profit generated in each state
full_df.groupBy("State").agg(sum("Profit").alias("Total_Profit")) \
    .orderBy(desc("Total_Profit")).show()
📈 Output
The output includes various statistics such as:

Highest selling product categories

Regions with most product diversity

Most profitable states and customer segments
