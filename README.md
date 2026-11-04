# Zepto – Exploratory Data Analysis

## Project Overview

This project focuses on performing Exploratory Data Analysis (EDA), Statistical Hypothesis Testing, and Prediction & Forecasting on Zepto's business data using Python. The objective is to understand the company's sales performance, financial trends, customer behaviour, store operations, and product and brand performance to derive meaningful business insights and recommendations.

## Datasets Used

The analysis uses six CSV files containing information about different aspects of Zepto's business:

| Dataset | Description |
|---|---|
| `Sales_Data.csv` | Contains order-level information, including quantity, unit price, gross amount, discounts, net amount, delivery time, order status, operating charges and profit. |
| `Customers_Information.csv` | Contains customer details, city, signup date, first order date and customer segment. |
| `Products_Information.csv` | Contains product information, including product name, category, brand, MRP and buying price. |
| `Stores_Information.csv` | Contains store details, opening year and employee count. |
| `Payments_Information.csv` | Contains payment-related information and payment methods. |
| `Promotions_Information.csv` | Contains promotion types and discount percentages. |

## Data Preprocessing

The following preprocessing steps were performed before analysis:

- Loaded all six CSV files using Pandas.
- Checked for missing values across the datasets.
- Handled missing values using mean, median, maximum-frequency values and designated placeholders, wherever applicable.
- Examined dataset structures, data types and descriptive statistics.
- Converted date-related columns into appropriate datetime formats.
- Converted the store opening year into a numeric format.
- Joined the datasets using their respective customer, product, store, payment and promotion IDs to create a consolidated dataset for analysis.

## Analysis Performed

### 1. Initial Data Exploration

- Examined the distribution of order quantities.
- Analysed mean, median, distribution and outliers across Gross Amount, Discount Amount, Net Amount and Order Profit.
- Calculated total Buying Price, Gross Revenue, Operating Charges, Discount Amount, Net Amount and Final Profit.
- Analysed monthly financial performance and month-over-month growth rates.

### 2. City-wise and Store-wise Analysis

- Analysed customer counts, gross spending, average delivery time and discounts across cities.
- Examined customer segments across different cities and stores.
- Compared store performance based on customer count, delivery time, revenue, net amount and discounts.
- Identified the highest and lowest performing stores.
- Analysed product categories, payment methods and promotion types across cities and stores.
- Examined store-level profitability across different customer segments.
- Identified the top five and bottom five customers based on order counts in each city.

### 3. Product and Brand-wise Analysis

- Examined order status distribution across brands and product categories.
- Analysed the impact of discounts on brand revenue.
- Calculated Average Order Value (AOV) across brands and categories.
- Compared Buying Price, Operating Charges, Discounts and Profit across brands and categories.
- Identified brands and categories with the highest and lowest promotion counts.
- Analysed monthly and yearly financial trends.
- Calculated average operational charges per employee across stores.
- Compared average operational charges across product categories.

### 4. Statistical Hypothesis Testing

Performed statistical hypothesis testing to investigate relationships and differences across business variables, including:

- Delivery time differences between delivered, cancelled and returned orders.
- Relationship between order quantity and delivery time.
- Correlation between city and Gross Amount.
- Correlation between Quantity and Gross Amount.
- Correlation between Discount Amount and Net Amount.
- Correlation between Delivery Minutes and Net Amount.
- Correlation between Buying Price and Order Profit.
- Differences in order amounts across customer segments and promotion types, including interaction effects.
- Association between product categories and brands.

### 5. Prediction and Forecasting

Applied Linear Regression and predictive modelling to estimate:

- Gross Amount, Discount Amount and Net Amount across cities.
- Revenue, Discounts and Profit across individual stores.
- Operating Charges and Buying Price across stores.
- Gross Amount, Discount Amount and Net Amount across brands.
- Financial performance and Operating Charges across product categories.
- Gross Amount across different payment methods.
- Cumulative customer growth for the next six years using signup dates.

Evaluated predictions by comparing actual and predicted values, percentage differences and R² scores wherever applicable.

## Key Insights and Recommendations

The analysis generated business insights and recommendations across five major areas:

1. **Data Quality:** Identified missing information and the importance of validating placeholder values before making business decisions.
2. **Financial Performance:** Examined revenue, discounts, operating expenses, investment and profitability to identify opportunities for cost optimisation.
3. **City and Store Performance:** Identified differences in customer spending, discount dependency, delivery efficiency and store-level performance across cities.
4. **Brand and Product Performance:** Evaluated brand and category performance to identify profitable opportunities and areas requiring cost optimisation.
5. **Prediction and Forecasting:** Evaluated forecasting performance and identified opportunities to improve financial planning, operational cost estimation and future customer growth predictions.

## Tools and Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Statistical Hypothesis Testing
- Linear Regression

## Conclusion

This project provides an analytical view of Zepto's business operations by combining multiple datasets and examining financial performance, customer behaviour, store efficiency, product and brand performance, and statistical relationships.

The findings are used to develop actionable business recommendations and explore predictive models that can support financial planning, operational improvements and future business decisions.
