# Walmartsales_analysis
This project analyzes Walmart sales data to:
- Which branches and products are perofroming the best,
- Sales trends over time,
- Coustumer behaviour,
- And how sales strategies can be improved
The dataset is souced from [Kaggle Walmart Sales Forecasting Competition](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting), which provides historical sales data from 45 walmart stores across multiple region.

# About data
| Column                  | Description                             | Data Type      |
| :---------------------- | :-------------------------------------- | :------------- |
| invoice_id              | Invoice of the sales made               | VARCHAR(30)    |
| branch                  | Branch at which sales were made         | VARCHAR(5)     |
| city                    | The location of the branch              | VARCHAR(30)    |
| customer_type           | The type of the customer                | VARCHAR(30)    |
| gender                  | Gender of the customer making purchase  | VARCHAR(10)    |
| product_line            | Product line of the product solf        | VARCHAR(100)   |
| unit_price              | The price of each product               | DECIMAL(10, 2) |
| quantity                | The amount of the product sold          | INT            |
| VAT                 | The amount of tax on the purchase       | FLOAT(6, 4)    |
| total                   | The total cost of the purchase          | DECIMAL(10, 2) |
| date                    | The date on which the purchase was made | DATE           |
| time                    | The time at which the purchase was made | TIMESTAMP      |
| payment_method                 | The total amount paid                   | DECIMAL(10, 2) |
| cogs                    | Cost Of Goods sold                      | DECIMAL(10, 2) |
| gross_margin_percentage | Gross margin percentage                 | FLOAT(11, 9)   |
| gross_income            | Gross Income                            | DECIMAL(10, 2) |
| rating                  | Rating                                  | FLOAT(2, 1)    |

### Step in the analysis
1. Data Wrangling
> Cleaning the data and checking for missing values.
2. Feature Engineering
> Creating new columns for better insights:
   > time_of_day: Morning, Afternoon, Evening
   > day_name: Day of the week
   > month_name: Month of the transaction
3. Exploratory Data Analysis (EDA)
> Exploring patterns and answering key business questions such as best-selling products and busiest sales times.

# Key business question
# Product Analysis
1. Which product line sells the most?
2. What is the most common payment method?
3. Which month has the highest sales?
4. Which city or branch generates the most revenue?

# Sales Analysis
1. What time of day has the highest sales?
2. Which customer type contributes the most revenue?

# Customer Analysis
1. What are the main customer types and payment methods?
2. Which gender buys more?
3. On which day do customers give the highest ratings?

# Revenue & profit formula
Basic calculations:
$ COGS (Cost of Goods Sold) = unit_price × quantity $

$ VAT (Tax) = 5% × COGS $

$ Total Sales = COGS + VAT $

$ Gross Income = Total − COGS $

$ Gross Margin (%) = Gross Income ÷ Total Revenue $

> Example:

> If a product costs $45.79 and 7 units are sold:

> COGS = 45.79 × 7 = 320.53

> VAT = 5% × 320.53 = 16.03

> Total = 336.56

> Gross Margin = 16.03 / 336.56 = 4.76%
