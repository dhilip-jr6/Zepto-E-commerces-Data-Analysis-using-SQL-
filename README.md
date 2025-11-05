🛒 Zepto SQL Data Analysis

This project performs data exploration, cleaning, and analysis on Zepto e-commerce data using SQL.
It helps understand product performance, stock status, discount strategies, and revenue generation.

📊 Project Overview

The project uses a dataset containing product details such as category, MRP, discount percentage, stock status, and quantity.
Through SQL queries, it explores, cleans, and analyzes the data to extract meaningful business insights.

⚙️ Tech Stack

SQL (PostgreSQL / MySQL compatible)

Dataset: Zepto Product Data

Tools: Any SQL IDE (e.g., PostgreSQL, MySQL Workbench, DBeaver, VS Code SQL Tools)

🧩 Key Steps
1. Data Exploration

Count total records

View sample data

Check for null values

Identify distinct product categories

Analyze stock availability

2. Data Cleaning

Remove products with invalid (zero) prices

Convert prices from paise to rupees

Handle duplicates and missing values

3. Data Analysis

Top 10 best-value products (by discount %)

Products with high MRP but out of stock

Estimated revenue per category

Top 5 categories by average discount

Price per gram calculation

Group products by weight category

Total inventory weight per category

📈 Example Queries
-- Top 10 best-value products
SELECT DISTINCT name, mrp, discountPercent
FROM zepto
ORDER BY discountPercent DESC
LIMIT 10;

-- Estimated Revenue by Category
SELECT category,
SUM(discountedSellingPrice * availableQuantity) AS total_revenue
FROM zepto
GROUP BY category
ORDER BY total_revenue DESC;

🚀 How to Run

Open your preferred SQL environment

Create a new database (e.g., zepto_db)

Run the provided SQL file:

\i Zepto_SQL_data_analysis.sql

Execute queries section by section to explore and analyze the data

🧠 Insights You Can Derive

Which categories contribute the most to total revenue

Discount trends across different product segments

Stock and supply management indicators

Best-performing product categories

📁 File Included

Zepto_SQL_data_analysis.sql — Complete SQL script (creation, cleaning, and analysis)

👨‍💻 Author

Dhilip Kumar
GitHub: https://github.com/dhilip-jr6

🏷️ Tags

#SQL #DataAnalysis #Zepto #ECommerce #Analytics #DataCleaning
