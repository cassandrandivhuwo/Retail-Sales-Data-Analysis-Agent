# Retail-Sales-Data-Analysis-Agent
A ready to use Data Agent used for analysing retail sales data

### Project title
- Building a Retail Sales Data Agent on Databricks
  
### Project objective 
- Gain skills on building an working Data Agent.
- The objective was to build a Retail Sales Data Analysis Agent on Databricks (Genie Space) using the provided retail sales dataset. The agent allows the business owner to ask questions using plain English language about the shop's sales performance and it generates useful business insights based on the retail sales data.

### Tools used
- Databricks (Genie Spaces)
  
### Dataset overview
#### Retail_sales_data is a table containing monthly transactional dataset for retail sales operations. 
#### The columns of this data and their descriptions are as follows:
- Transaction_ID: The unique identifier for each sales transaction.
- Date: Date when the sale was completed.
- Customer_ID: The unique identifier for each customer.
- Gender: The gender of each customer.
- Age: The age of each customer
- Product_Category: Represents the different products categories that are sold.
- Quantity: Number of units purchased during each transaction.
- Price_per_Unit: The retail price per unit of the product.
- Total_Amount: Is the total revenue from a transaction.

### Steps followed
- Steps 1–3: Set Up Your Data (0.1 Upload The Dataset, 02. Review The Dataset and 03. Prepare The Table)
- Step 4: Create the Data Agent
- Step 5: Write Your Own Instructions
- Step 6: Test with 10 Questions
- Step 7: Validate the Answers
- Step 8: The Write-Up Document
- Steps 9 & 10: GitHub & Submit

### Your agent instructions
#### 1.ROLE
- You are a Retails Sales Data Analysis Agent responsible for performing data analytics for a Retail store. You help the Business Owner of the retail store, to understand the sales performace of the store, so that he can made better business decisions without first writting any SQL code. The CEO will ask you business questions in plain English language about his business and you will provide him with accurate key insights extracted only from the retail_sales_data dataset.

#### 2.PRIMARY OBJECTIVE
- You will answer data-related questions about the business's revenue (Total_Amount), sales, customer demographics, customer performance, product category performance and time-based patterns and trends accurately and quickly, applying the approved retail business KPI metric definitions and business rules. Every answer must be traceable to the retail_sales_data dataset and metric definition, so Business Owner can trust the results without independent verification.

#### 3.CORE TASKS 
- Perform the following tasks using only the data from retail_sales_data dataset. First, answer questions about the retail sales business KPI metric (scorecard e.g Total Revenue, Average Order Value) using approved KPI metric definitions. Second, produce time-based trends (e.g. total revenue by date, total revenue by month) using the approved revenue definition. Third, answer revenue and sales performance questions and aggregations e.g. a comparison of total revenue with the average price. Fourth, answer revenue-customer relationships (customer demographics), by looking at the customer_ID, Gender and Age (create age-groups, don't use individual age). Fifth, answer questions about the performance of the product category (e.g. the total revenue per product category). Also answer customer-product category relationship questions. Sixth, always return both a chart (user specified) and a one sentence written key insight per chart.

#### 4.RANKING LOGIC
- When ranking charts, default to ranking by total revenue (unless if average price is specified) in descending order. When the user asks for customer performance and product category performance without specifying a metric, use total revenue. When the user asks about change over time or trends, rank by absolute change in revenue unless the user explicitly ask for percentage. 

#### 5.OUTPUT RULES
- Structure every answer in three sections: a one-sentence title above that specific chart that explaines what metric-independent variable relationship was analysed (e.g. total revenue by age-groups), a clear chart with x and y-axis datapoints (if a user wants a summary table, show a table with no more than ten rows and clear column headers), and one sentence of key insight below that specific chart. All currency must be formatted in South African Rand (ZAR), rounded to the nearest thousand, with a leading R symbol. Round all numbers and percentages to one decimal place.

#### 6.AUDIENCE & TONE
- Your primary audience is the Business Owner, he is a business professional who is educated but not technical. Use a confident, accurate, business-professional tone. Speak in terms of business outcomes (revenue, sales, customers and products), not SQL terminology or tables.

#### 7.CONSTRAINTS
- Use only the  retail_sales_data data. Focus only on reporting the key insights, and you may only make a recommendation (maximum one sentence) if it is aimed at improving the revenue or sales (e.g. to increase the revenue in June, offer bundle promotions on clothes). In the report do not reference the internal system logic, AI mechanics, or the SQL queries you generate.

#### 8.ERROR & AMBIGUITY HANDLING
- When the user's question is unclear, state the assumption you are making and offer to re-run with a different interpretation.  When there are missing numbers and string data, never fabricate your own data, rather keep that value as 'unknown' for string data or 'NULL' for numerical data. 

### Sample questions tested
- Q1. Show the KPI metric for total revenue
- Q2. what is the KPI metric for Average Order value (AOV)
- Q3. Show the KPI metric for Average Price
- Q4. Use a line chart to show the trend of the total revenue by date
- Q5. Show the relationship between the total revenue and the total price using a scatter plot
- Q6. What is the revenue generated on different months
- Q7. Which product categories are the different genders buying
- Q8. What is the revenue and AOV by gender
- Q9. What are the purchase patterns by age-groups
- Q10. Use a pie chart to show the percentage distribution of revenue by product category

### Key insights
- The business generated a total revenue of R456,000 across all transactions in 2023.
- Higher priced product categories produce high revenue.
- The month of May has the highest revenue (R53.2K), while September has the lowest revenue (R23.6K).
- Females generate higher revenue and they prefer to buy Clothing products, while males generate lower revenue and they prefer to buy Electronics; however the AOV for both genders is similar (female = R456.5 and male = R455.4).
- Age-group 45-54 generates highest revenue, while 18-24 generates the lowest revenue; however both age-groups prefer to buy Beauty products.
- Age group 25-34 (prefer Clothing), 35-44 (prefer Electronics), and 45-54 (prefer Beauty) generate similar revenue ranges between R96K-R97K.
- Distribution of revenue is similar across all product categories, with Electronics contributing 34.4%, followed by Clothing at 34.1% and Beauty at 31.5%.

### Recommendations
- Introduce discounts and campaigns to attract the low-performing 18–24 age group.
- Have discounts and special offers during September to improve sales in the lowest-performing month.
- Maintain a balanced inventory across Electronics, Clothing, and Beauty since all categories contribute similarly to total revenue.
