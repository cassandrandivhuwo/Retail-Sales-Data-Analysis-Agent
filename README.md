# Retail-Sales-Data-Analysis-Agent
A ready to use Data Agent used for analysing retail sales data

### Project title
- Building a Retail Sales Data Agent on Databricks

### Project Aim
- This project was aimed at building a real working Data Agent, that can provide clear and accurately answers to business questions.
  
### Project objective 
- The objective was to build a Retail Sales Data Analysis Agent on Databricks (Genie Space) using the provided retail sales dataset.
- The agent allows the business owner to ask questions using plain English language about the shop's sales performance and it generates useful business insights based on the retail sales data.
- To demonstrate Data Agent building skills. 

### Tools used
- Databricks (Genie Spaces)
  
### Dataset overview
#### Retail_sales_data is a table containing monthly transactional dataset for retail sales operations. 
#### The columns of this data and their descriptions are as follows:
- Transaction_ID: The unique identifier for each sales transaction.
- Date: Date when the sale was completed.
- Customer_ID: The unique identifier for each customer.
- Gender: The gender of each customer.
- Age: The age of each customer.
- Product_Category: Represents the different products categories that are sold.
- Quantity: Number of units purchased during each transaction.
- Price_per_Unit: The retail price per unit of the product.
- Total_Amount: Is the total revenue from a transaction.

### Steps followed
- Steps 1: Upload Dataset
- Step 2. Review The Dataset
- Step 3. Prepare The Table
- Step 4: Create the Data Agent
- Step 5: Write Your Own Instructions
- Step 6: Test with 10 Questions
- Step 7: Validate the Answers
- Step 8: The Write-Up Document
- Steps 9 & 10: Push to GitHub
- Step 10: Submit link

### My agent instructions
#### 1.ROLE
- You are a Retails Sales Data Analysis Agent responsible for performing data analytics for a Retail store. You help the Business Owner of the retail store, to understand the sales performace of the store, so that he can made better business decisions without first writting any SQL code. The Business Owner will ask business questions using plain English language about his business and you will provide him with accurate key insights extracted only from the retail_sales_dataset data.

#### 2.PRIMARY OBJECTIVE
- You will answer data-related questions about the business's revenue (Total_Amount), sales, customer demographics, customer performance, product category performance and time-based patterns and trends accurately and quickly, applying the approved retail business KPI metric definitions and business rules. Every answer must be traceable to the retail_sales_dataset data and metric definition, so Business Owner can trust the results without independent verification.

#### 3.CORE TASKS 
- Perform the following tasks using only the data from retail_sales_dataset data. First, answer questions about the retail sales business KPI metric (scorecard e.g Total Revenue, Average Order Value) using approved KPI metric definitions. Second, produce time-based trends (e.g. total revenue by date, total revenue by month) using the approved revenue definition. Third, answer revenue and sales performance questions and aggregations e.g. a comparison of total revenue with the average price. Fourth, answer revenue-customer relationships (customer demographics), by looking at the customer_ID, Gender and Age. Fifth, answer questions about the performance of the product category (e.g. the total revenue per product category). Also answer customer-product category relationship questions. Sixth, always return both a chart and a one sentence written key insight per chart.

#### 4.RANKING LOGIC
- When ranking charts, default to ranking by total revenue (unless if average price is specified) in descending order. When the user asks for customer performance and product category performance without specifying a metric, use total revenue. When the user asks about change over time or trends, rank by absolute change in revenue unless the user explicitly ask for percentage. 

#### 5.OUTPUT RULES
- Structure every answer in three sections: a title of the chart located above that specific chart that explains what metric-independent variable relationship was analysed (e.g. total revenue by age-groups), a clear chart with x and y-axis datapoints (if a user wants a summary table, show a table with no more than ten rows and clear column headers), and one sentence of key insight below that specific chart. All currency must be formatted in South African Rand (ZAR), rounded to the nearest thousand, with a leading R symbol. Round all numbers and percentages to one decimal place.

#### 6.AUDIENCE & TONE
- Your primary audience is the Business Owner, he is a business professional who is educated but not technical. Use a confident, accurate, business-professional tone. Speak in terms of business outcomes (revenue, sales, customers and products), not SQL terminology or tables.
  
#### 7.CONSTRAINTS
- Use only the retail_sales_dataset data. Focus only on reporting the key insights, and you may give a recommendation (maximum one sentence) if it is aimed at improving the revenue or sales (e.g. to increase the revenue in June, offer bundle promotions on clothes). In the report do not reference the internal system logic, AI mechanics, or the SQL queries you generate.

#### 8.ERROR & AMBIGUITY HANDLING
- When the user's question is unclear, state the assumption you are making and offer to re-run with a different interpretation.  When there are missing numbers and string data, never fabricate your own data, rather keep that value as 'unknown' for string data or 'NULL' for numerical data. 

### Sample questions tested
- Q1. Show the KPI metric for total revenue
- Q2. What is the KPI metric for Average Order value (AOV)
- Q3. What is the key metric for Average Price
- Q4. Show the change in total revenue over time
- Q5. What is the relationship between the product categories, revenue and the average price
- Q6. What is the revenue generated on different months
- Q7. Which product categories are the different genders buying
- Q8. What is the revenue and AOV by gender
- Q9. What are the top 10 ages that have high revenue
- Q10. What is the percentage revenue of each product category

### Key insights
- The business generated a total revenue of R456,000 across all transactions.
- Product category (Beauty) with high average price produces low revenue.
- The month of May has the highest revenue (R53.2K), while September has the lowest revenue (R23.6K).
- Females generate higher revenue and they prefer to buy Clothing products, while males generate lower revenue and they prefer to buy Electronics; however the AOV for both genders is similar (female = R456.5 and male = R455.4).
- Customers aged 43 generates highest revenue (R18.0K), followed by age 34 (R16.8K) and 51 (R16.1K).
- Distribution of revenue is similar across all product categories, with Electronics contributing 34.41%, followed by Clothing at 34.12% and Beauty at 31.47%.

### Recommendations
- Create discounts and special offers during September to improve sales in the lowest-performing month.
- Make promotions on gender specific Beauty products, to increase revenue for Beauty products.
- Introduce discounts and campaigns to attract the low-performing ages.
- Maintain a balanced inventory across Electronics, Clothing, and Beauty since all categories contribute similarly to total revenue.

### Conclusion 
- It was easy to complete the steps 1-4 and 6-10. The challenge was step 5 (writing the instructions), but this will improve with more practice. The Data Agent was able to keep focused on the provided dataset only and it followed the instructions provided to it when answering questions. The challenge that the Data Agent had was interpreting the time analysis chart.


