# Online Retail Data Analysis Project

## Overview
This project analyzes an online retail dataset to extract business insights, clean the data, engineer features, and segment customers using RFM (Recency, Frequency, Monetary) analysis and clustering. The analysis is performed in a Jupyter Notebook using Python, pandas, matplotlib, seaborn, and scikit-learn.

---

## Steps Performed

### 1. Data Import and Initial Exploration
- Loaded the dataset from Excel using pandas.
- Displayed the first few rows to understand the structure and columns.

### 2. Data Cleaning
- Removed administrative transactions (where `UnitPrice` is 0).
- Filtered out rows with specific `StockCode` values (e.g., 'AMAZONFEE', 'BANK CHARGES', and other non-sale codes).
- Removed rows with missing or blank `CustomerID` values.

### 3. Feature Engineering
- Split the `InvoiceDate` column into separate `Date` and `Time` columns.
- Converted the `Date` column to datetime format for time-based analysis.
- Created a `TotalCost` column as the product of `UnitPrice` and `Quantity`.

### 4. Descriptive Analysis
- Calculated total sales and average order value.
- Identified the top 10 products by quantity sold and by revenue.
- Visualized these results using bar charts.

### 5. Time Series Analysis
- Created a `YearMonth` column to aggregate sales by month.
- Plotted the sales trend over time.
- Printed the monthly sales values for reference.

### 6. Country-Level Analysis
- Counted the number of purchases (unique invoices) per country.
- Calculated and visualized total revenue per country.
- Analyzed and plotted sales by country, excluding the United Kingdom.

### 7. Customer Analysis
- Calculated purchase frequency per customer.
- Visualized the top 10 customers by purchase frequency.

### 8. RFM Segmentation
- Calculated Recency, Frequency, and Monetary values for each customer.
- Assigned RFM scores and created a composite RFM segment label.
- Segmented customers into groups such as Champions, Loyal, At Risk, and New.
- Visualized the distribution of customer segments.

### 9. Advanced RFM Clustering
- Standardized RFM features using `StandardScaler`.
- Plotted the distribution of R, F, and M values.
- Applied KMeans clustering to segment customers into 4 clusters.
- Labeled clusters with business meanings (High-value, Loyal, At-risk, Low-value).
- Visualized clusters using pair plots and PCA scatter plots.

### 10. Business Insights and Recommendations
- Summarized the number of customers per cluster.
- Described the traits of each cluster.
- Suggested marketing actions for each segment (e.g., loyalty rewards, re-engagement emails).

---

## How to Use This Notebook
1. Ensure you have Python and the required libraries installed (`pandas`, `matplotlib`, `seaborn`, `scikit-learn`, `openpyxl`).
2. Place the dataset Excel file in the specified path.
3. Run each cell in order to reproduce the analysis and visualizations.
4. Review the markdown summaries for business insights and recommendations.

---

## Key Visualizations

Below are the main visualizations generated in this analysis. You can include images (screenshots or saved plots) in your GitHub README by uploading them to your repository and referencing their paths, or by using external image links.

### 1. Top 10 Products by Quantity Sold
![Top 10 Products by Quantity Sold](top_10_products_quantity.png)
*This bar chart shows the products with the highest sales volume. It helps identify your most popular items by quantity.*

### 2. Top 10 Highest Revenue-Generating Products
![Top 10 Revenue Products](images/top_10_products_revenue.png)
*This bar chart highlights the products that generate the most revenue, which may differ from those with the highest quantity sold.*

### 3. Sales Trend by Month
![Sales Trend by Month](images/sales_trend_month.png)
*This line plot displays total sales for each month, revealing seasonality, growth, or dips in sales over time.*

### 4. Scatter Plot of UnitPrice vs Quantity
![UnitPrice vs Quantity](images/unitprice_vs_quantity.png)
*This scatter plot visualizes the relationship between product price and quantity purchased per transaction. It helps spot outliers and understand purchasing patterns.*

### 5. Number of Purchases per Country
![Purchases per Country](images/purchases_per_country.png)
*This bar chart shows the number of unique purchases (invoices) from each country, highlighting your most active markets.*

### 6. Revenue Generated per Country
![Revenue per Country](images/revenue_per_country.png)
*This bar chart displays total revenue by country, helping you identify your most valuable geographic markets.*

### 7. RFM Clusters Pair Plot
![RFM Clusters Pair Plot](images/rfm_pairplot.png)
*This pair plot visualizes the distribution and separation of customer clusters based on Recency, Frequency, and Monetary values.*

### 8. RFM Clusters PCA Scatter Plot
![RFM Clusters PCA](images/rfm_pca.png)
*This scatter plot uses PCA to reduce RFM features to two dimensions, making it easy to see how customer clusters are separated.*

---

> **Note:**
> - To display these images on GitHub, save your plots as PNG files (e.g., using `plt.savefig('images/plot_name.png')`) and upload them to an `images` folder in your repository.
> - The explanations below each image help viewers quickly understand the business insight each chart provides.

---

## Business Value
This analysis helps the business:
- Identify best-selling products and high-revenue items.
- Understand sales trends over time and across countries.
- Segment customers for targeted marketing and retention strategies.
- Visualize and interpret customer behavior for data-driven decision making.

---

## Author
Generated with the help of GitHub Copilot and Python data science libraries.
