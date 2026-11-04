# Zepto – Exploratory Data Analysis

## Project Overview

This project focuses on performing Exploratory Data Analysis (EDA), Financial Analysis, Statistical Hypothesis Testing, and Prediction & Forecasting on Zepto's business data using Python.

The objective is to understand Zepto's financial performance, customer purchasing behaviour, city-wise and store-wise operations, product and brand performance, and promotional strategies. The analysis also explores statistical relationships between business variables and uses predictive modelling to estimate future financial performance and customer growth.

## Dataset Description

The project uses **six CSV files** containing information about different aspects of Zepto's business.

| Dataset | Records | Description |
|---|---:|---|
| `Sales_Data.csv` | 313,480 | Contains order-level information, including Order ID, Order Date, Customer ID, Product ID, Store ID, Quantity, Unit Price, Gross Amount, Discount Amount, Net Amount, Delivery Minutes, Order Status, Operation Charges and Order Profit. |
| `Customers_Information.csv` | 25,000 | Contains Customer ID, Customer Name, City, Signup Date, Customer Segment and First Order Date. |
| `Products_Information.csv` | 2,200 | Contains Product ID, Product Name, Category, Brand, MRP and Buying Price. |
| `Stores_Information.csv` | 180 | Contains Store ID, Store Name, City, Opening Year and Employee Count. |
| `Payments_Information.csv` | 5 | Contains Payment ID and Payment Method. |
| `Promotions_Information.csv` | 120 | Contains Promotion ID, Promotion Type and Discount Percentage. |

The datasets were combined using their respective IDs to create a consolidated dataset for analysis.

## Data Preprocessing

The following preprocessing steps were performed:

- Imported all six CSV files using Pandas.
- Examined the structure, dimensions and data types of each dataset.
- Checked for missing values across all datasets.
- Handled missing numerical values using mean and median imputation, depending on the column.
- Handled missing categorical values using the maximum-frequency value.
- Filled missing identifier values using designated placeholder values.
- Rechecked the datasets to verify the missing-value treatment.
- Converted `OrderDateTime`, `SignupDate` and `FirstOrderDate` into appropriate datetime formats.
- Converted `OpeningYear` into a numeric format.
- Performed individual joins using Customer ID, Product ID, Store ID, Payment ID and Promotion ID.
- Created a consolidated dataset by merging all six datasets.

## Exploratory Data Analysis (EDA)

### 1. Initial Data Exploration and Financial Analysis

- Analysed the distribution of the Quantity variable.
- Examined mean, median, distribution and outliers across Gross Amount, Discount Amount, Net Amount and Order Profit.
- Identified high-value outlier transactions and examined their impact on average revenue and profitability.
- Calculated total Buying Price, Gross Revenue, Operation Charges, Discount Amount and Net Amount.
- Compared the final recorded profit with the remaining expenses and adjustments.
- Analysed monthly financial performance by grouping records by year and month.
- Calculated month-over-month growth rates for Buying Price, Gross Amount, Operation Charges, Net Amount and Discount Amount.
- Created bar plots to visualize monthly financial growth trends.

### 2. City-wise and Store-wise Analysis

Analysed customer behaviour, financial performance, store efficiency and promotional activities across different cities and stores.

The analysis included:

- Compared customer count, total Gross Amount, average Delivery Minutes and average Discount Amount across cities.
- Examined customer segments across different cities.
- Identified the number of stores operating in each city.
- Analysed customer distribution across individual stores.
- Calculated average delivery time for each store in every city.
- Identified stores with the highest and lowest Gross Amount, Net Amount and Discount Amount.
- Examined the most frequently ordered product category across cities.
- Compared Gross Amount, Net Amount and Discount Amount across product categories.
- Analysed store-level financial performance along with store opening years.
- Examined payment-method usage across cities and stores.
- Identified the number of distinct SKUs recorded across product categories, stores and cities.
- Analysed promotion types across different cities and stores.
- Examined customer-segment distribution at the individual store level.
- Compared transactions and Gross Amount across payment methods.
- Analysed Buying Price, Operation Charges and Order Profit across customer segments and stores.
- Identified the top five and bottom five customers based on the number of orders placed in each city.

### 3. Product and Brand-wise Analysis

Analysed product categories, brand performance, discounts, profitability and promotional activities.

The analysis included:

- Examined order status distribution across brands and product categories.
- Compared delivery fulfilment, cancellation and return rates across brands within individual categories.
- Analysed the impact of discounts on brand revenue.
- Calculated Average Order Value (AOV) across brands and product categories.
- Compared Buying Price, Operation Charges, Discount Amount and Order Profit across brands and categories.
- Identified brands and categories with the highest and lowest promotional activity.
- Analysed the monthly and yearly trends in Gross Amount, Profit, Revenue and Buying Price.
- Calculated month-over-month growth rates for financial variables.
- Examined average operational charges per employee for each store.
- Identified stores with the highest and lowest average operational charges per employee.
- Calculated average operational charges across product categories and identified the highest and lowest categories.

### 4. Statistical Hypothesis Testing

Performed statistical hypothesis testing at a **5% significance level (α = 0.05)** to investigate relationships and differences between business variables.

The following tests were conducted:

**A. Independent Samples t-tests**

- Compared delivery times between Delivered and Cancelled orders.
- Compared delivery times between Delivered and Returned orders.

**B. Pearson Correlation Tests**

- Examined the relationship between Quantity and Delivery Minutes.
- Examined the relationship between City and Gross Amount using city-wise binary encoding.
- Examined the relationship between Quantity and Gross Amount.
- Examined the relationship between Discount Amount and Net Amount.
- Examined the relationship between Delivery Minutes and Net Amount.
- Examined the relationship between Buying Price and Order Profit.

**C. Two-way ANOVA**

- Examined whether Gross Amount differs across Customer Segments and Promotion Types.
- Investigated the interaction effect between Customer Segment and Promotion Type.

**D. Chi-square Test of Independence**

- Examined whether a statistically significant association exists between Product Category and Brand.

For each test, the null and alternative hypotheses were defined, test statistics and p-values were calculated, and conclusions were drawn based on statistical significance.

### 5. Prediction and Forecasting Analysis

Applied Linear Regression to estimate financial performance and future customer growth.

The analysis included:

- Predicted Gross Amount, Discount Amount and Net Amount across cities based on the number of stores.
- Predicted Revenue, Discount and Profit for individual stores across cities based on transaction counts.
- Predicted Operation Charges and Buying Price for individual stores based on transaction counts.
- Predicted Gross Amount, Discount Amount and Net Amount across brands based on the number of products.
- Predicted Gross Amount, Discount Amount, Net Amount and Operation Charges across product categories.
- Predicted Gross Amount across different payment methods.
- Forecasted cumulative customer growth for the next six years using Signup Date information.
- Compared actual and predicted values using percentage differences.
- Evaluated model performance using R² scores.

## Key Insights

### 1. Initial Exploration and Financial Insights

- The Sales dataset contained 313,480 records, while the Customers dataset contained 25,000 records and the Products dataset contained 2,200 records.
- Most orders contained relatively small quantities, with the highest frequency occurring at a quantity of 2.
- The typical customer transaction generated an average Net Amount of ₹106.63 and an average Order Profit of ₹5.19 based on the median values reported in the analysis.
- More than 33,000 high-value outlier transactions significantly influenced the averages, increasing average Net Amount to ₹252.75 and average Order Profit to ₹12.31.
- Total Buying Price amounted to approximately ₹304.46 lakhs, while Gross Revenue reached approximately ₹959.38 lakhs.
- Operation Charges amounted to approximately ₹41.70 lakhs, while Discount Amount accounted for approximately ₹125.35 lakhs.
- After discounts, Net Amount stood at approximately ₹792.33 lakhs. Further expenses and adjustments of approximately ₹753.75 lakhs reduced Profit Before Tax to approximately ₹38.57 lakhs.
- Monthly financial growth showed considerable fluctuations, particularly during 2023 and early 2025, indicating the need for better expense and revenue planning.

### 2. City-wise and Store-wise Insights

- Kolkata and Chennai emerged as high-value markets where customers demonstrated a willingness to spend higher amounts despite comparatively lower discounting.
- Mumbai and Gurgaon showed greater dependence on discounts and faster delivery, indicating the need for more targeted customer-retention strategies.
- Pune and Bangalore represented potential growth opportunities because of their customer base and delivery performance.
- Every city operated with an identical physical retail footprint of 180 stores.
- Delhi's store STR3EXW9S52LG recorded the highest customer count, with 235 customers.
- Kolkata's store STRWP2NB254TW recorded the fastest average delivery time at 19.09 minutes.
- Gurgaon's store STREPZ5MPJMHA recorded the slowest average delivery time at 22.56 minutes.
- Noida's store STRMK2G05ZNOJ recorded the highest Gross Amount of ₹91,223.63 and Net Amount of ₹77,764.09.
- UPI dominated payment activity, accounting for approximately 65% of transactions.
- Flat Discounts and Free Delivery were the most frequently used promotional methods across cities and stores, while BOGO promotions recorded comparatively lower order volumes.
- The highest number of orders placed by an individual customer was 29, recorded in Hyderabad.

### 3. Product and Brand-wise Insights

- Brands such as Aashirvaad, Coca-Cola, Fortune and ITC operated in individual product categories, while Amul, Britannia, Dabur, Local, Nestle and Pepsi were present across multiple categories.
- Dabur recorded the highest aggregate sales footprint across the portfolio due to its presence in seven product categories.
- Aashirvaad generated approximately ₹7.52 million in Gross Sales within the Grocery category.
- The Local brand generated approximately ₹7.57 million in Gross Revenue through Dairy and Beverages, accounting for approximately 97.2% of its total performance. However, heavy discounts, particularly in Dairy, reduced its Net Amount.
- Dabur recorded the highest overall brand-level AOV at ₹5,540.43, followed by Amul at ₹3,208.55.
- Dairy and Beverages recorded relatively high AOV values compared with several other product categories.
- Beverages and Dairy were among the largest loss-making categories, with substantial operating expenses and discount expenditure.
- Coca-Cola required particular financial attention because of its substantial investment and reported losses.
- Health & Wellness demonstrated comparatively better profitability despite having the highest average operational charge of approximately ₹56.92.
- Britannia recorded the highest promotional activity across major promotion types, while Fortune and Aashirvaad maintained comparatively conservative promotional strategies.
- Beverages and Dairy recorded the highest frequency of promotional campaigns across product categories.

### 4. Hypothesis Testing Insights

The statistical tests produced the following key findings:

- Delivery time did not show a statistically significant difference between Delivered and Cancelled orders (p = 0.6019).
- Delivery time also did not show a statistically significant difference between Delivered and Returned orders (p = 0.6058).
- Quantity and Delivery Minutes showed an almost zero negative correlation (r ≈ -0.0016), indicating no meaningful linear relationship.
- City-wise binary correlation tests with Gross Amount did not show statistically significant relationships for the nine cities.
- Quantity and Gross Amount showed a statistically significant positive correlation (r ≈ 0.2925).
- Discount Amount and Net Amount showed a statistically significant but weak negative correlation (r ≈ -0.0218).
- Delivery Minutes and Net Amount showed no statistically significant linear correlation (r ≈ 0.0012).
- Buying Price and Order Profit showed a strong positive correlation (r ≈ 0.8628).
- The Two-way ANOVA showed no statistically significant standalone effect of Customer Segment (p ≈ 0.8448) or Promotion Type (p ≈ 0.8195). The interaction effect was also not statistically significant at the 5% level (p ≈ 0.0678).
- The Chi-square test identified a statistically significant association between Product Category and Brand (p = 0.0 as displayed by the notebook).

### 5. Prediction and Forecasting Insights

- City-level financial predictions showed strong performance for Discount Amount (R² = 0.9990), Gross Amount (R² = 0.7393) and Net Amount (R² = 0.6576).
- City-level Net Amount prediction differences were reported within approximately -1.34% to +0.65%.
- Store-level Operation Charges forecasting showed weak performance, with an overall R² of approximately 0.3807 and a particularly low Pune R² of 0.0504.
- Brand-level forecasting performed poorly for Gross Amount (R² = -0.9593) and Net Amount (R² = -0.9438), despite a high Discount Amount R² of 0.9974.
- Category-level forecasting showed stronger overall performance for Gross Amount (R² = 0.7727), Operation Charges (R² = 0.6836) and Net Amount (R² = 0.6836). However, predictions varied considerably across individual categories.
- Payment-method forecasting produced an R² of approximately -0.0001, indicating that payment method was not a useful predictor of Gross Amount despite small differences between predicted and actual totals.
- UPI accounted for approximately ₹62.72 million in Gross Amount, followed by Wallet at ₹9.51 million and Cash at ₹4.77 million.
- Customer growth forecasting produced an R² of approximately 0.7082. However, actual new customer acquisition declined from 11,306 in 2022 to 1,791 in 2023 and just 17 in 2024, making the linear forecast of future customer growth unreliable.

## Recommendations

### A. Data Value Recommendations

- Identify and verify placeholder values used during missing-value treatment against original records before using the data for business decisions.
- Maintain proper documentation of missing information and distinguish between genuine business values and placeholders.
- Regularly validate customer, product, store, payment and promotion identifiers to ensure accurate dataset integration.

### B. Initial Exploration Recommendations

- Focus on optimising operational charges while managing discount expenditure effectively.
- Consider Strategic Workforce Planning (SWP) to align employee requirements with changing business demand.
- Explore flexible workforce arrangements to avoid maintaining unnecessarily high staffing levels during periods of lower demand.
- As the business matures, gradually shift attention from customer acquisition through discounts towards profitability, customer retention and repeat purchases.
- Introduce loyalty programmes, referral programmes, BOGO offers and subscription-based free-delivery programmes where commercially viable.
- Explore collaborations with product companies to introduce product samples and encourage product discovery.

### C. City-wise and Store-wise Recommendations

1. **Prioritise Kolkata and Chennai:** Focus on customer retention, product availability and maintaining their existing spending patterns.

2. **Improve Mumbai and Gurgaon:** Introduce targeted promotional offers while investigating store-level delivery performance and customer expectations.

3. **Develop Pune and Bangalore:** Focus on customer acquisition and converting Regular and Occasional customers into Premium customers through personalised offers and loyalty programmes.

4. **Replicate High-performing Store Practices:** Study successful stores, particularly Delhi's STR3EXW9S52LG and Kolkata's STRXICBFBJCFO, and identify operational practices that can be implemented across other locations.

5. **Improve Gurgaon Delivery Efficiency:** Investigate staffing, order allocation and fulfilment processes at the slowest-performing store.

6. **Optimise Store Expansion:** Since every city operates with an identical physical footprint of 180 stores, future expansion should be based on individual store performance, customer demand and revenue potential rather than simply increasing store count.

### D. Brand and Product-wise Recommendations

1. **Focus on High-performing Brands:** Continue prioritising Dabur, Amul, Nestle, Coca-Cola and Haldiram's in their respective high-performing categories, while evaluating profitability, operating expenses and discount expenditure.

2. **Improve Local Brand Profitability:** Optimise discounting and procurement costs, particularly in Dairy and Beverages, where the Local brand generates substantial revenue but experiences significant discount expenditure.

3. **Develop Local Brands Through Strategic Partnerships:** Identify promising local brands and explore exclusive partnerships before considering acquisitions. This can help develop an exclusive product portfolio and improve long-term control over procurement and margins.

4. **Review Coca-Cola's Financial Performance:** Investigate procurement costs, operational expenses, discount expenditure and inventory movement to identify the reasons behind its reported losses.

5. **Evaluate Dabur's Individual Categories:** Examine less-profitable product categories, monitor demand and optimise inventory levels to avoid unnecessary inventory costs.

6. **Optimise Beverages and Dairy:** Improve cold-chain infrastructure, inventory rotation, demand forecasting and stock replenishment to reduce wastage and operational costs.

7. **Introduce a Prepaid Milk Subscription Model:** Consider a flexible prepaid milk subscription with daily skip options and appropriate refunds or credits to encourage repeat purchases and improve working capital.

8. **Continue Supporting Health & Wellness:** Maintain investment in this comparatively profitable category while exploring opportunities to reduce storage, transportation and handling expenses.

9. **Improve Aashirvaad's Order Fulfilment:** Investigate its comparatively high cancellation rate and improve order fulfilment processes.

10. **Review Snacks Category Discounting:** Evaluate individual brands, product demand and profitability to ensure that heavy discounts are generating sustainable sales rather than reducing margins.

11. **Optimise Promotion Types:** Introduce promotional strategies based on order value, customer segment, location and purchase occasions instead of relying on uniform discounts.

### E. Prediction and Forecasting Recommendations

1. **Use City-level Forecasts:** Utilise the comparatively strong city-level predictions to support financial planning, promotional budgets and resource allocation.

2. **Prioritise Pune and Bangalore:** Monitor these markets closely because the forecasts indicate potential opportunities for additional inventory, marketing and localised promotions.

3. **Improve Store-level Cost Forecasting:** Develop localised forecasting models using individual store expenses and operational requirements instead of relying entirely on centralised estimates.

4. **Develop Brand-specific Forecasting Models:** Improve brand-level predictions by incorporating historical sales, individual brand demand and product performance.

5. **Improve Category-level Forecasting:** Develop separate category-specific models to reduce large prediction differences and improve inventory and operational budget allocation.

6. **Use Payment-channel Forecasts Carefully:** Use transaction distribution to plan payment-processing requirements, but do not treat payment methods as reliable predictors of customer spending.

7. **Replace Linear Customer Growth Forecasting:** Avoid relying entirely on linear customer acquisition projections. Consider market-saturation models that account for declining acquisition trends, the existing customer base and realistic growth opportunities.

8. **Validate Models Before Implementation:** Models with negative or low R² scores should be refined and tested using additional historical data before being used for important financial or operational decisions.

## Tools and Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Statsmodels
- Scikit-learn
- Exploratory Data Analysis
- Statistical Hypothesis Testing
- Pearson Correlation
- Independent Samples t-test
- Two-way ANOVA
- Chi-square Test
- Linear Regression
- Predictive Modelling

## Conclusion

This project provides a comprehensive analytical view of Zepto's business operations by combining six datasets and examining financial performance, customer behaviour, city-wise and store-wise performance, product and brand profitability, promotional strategies and delivery operations.

The analysis highlights the importance of controlling operational expenses, optimising discount strategies, improving category-level profitability and developing more reliable forecasting models.

The insights and recommendations aim to support better financial planning, operational efficiency, customer retention and sustainable business growth.
