# 📊 Sample-Store-Sales-Analysis (SQL + Power BI)

## 📌 Project Overview
This project analyzes retail sales data to evaluate overall sales performance, profitability, and customer purchasing patterns.  
The objective is to generate data-driven insights that can support better business decisions such as pricing strategy, regional focus, and product optimization.

---

## ❓ Business Questions
- What is the overall sales performance?
  Answer:
  . The business demonstrates strong overall sales performance across all regions.
  . Revenue is driven primarily by a few high-performing regions.
  
- How profitable is the business?
   Answer:
  . The business is profitable overall, with a positive profit margin.
  . Profitability varies significantly by product category.
  
- Which categories generate the most profit?
   Answer: 
  . Technology is the most profitable category.
  . Office Supplies perform moderately well.
  . Furniture generates high sales but low profit margins.
  
- Which areas negatively impact profitability?
   Answer:
  . Certain sub-categories consistently generate losses.
  . Losses are driven by high discount rates and cost structures.

- What is the impact of discounts on profit?
  Answer:
  . Higher discounts are strongly associated with lower profit.
  . Discounting is most harmful in Furniture and Office Supplies.
  
- What should management prioritize?
  Answer
  . Focus on high-performing regions and categories.
  . Reduce excessive discounting.
  . Improve or eliminate consistently loss-making products.


---

## 📂 Data Source
- Dataset: Sample Superstore Dataset (Kaggle)  
- Region, Category, Sub-Category, Sales, Profit, Discount, Quantity

## Tools Used
- SQL
- Powe BI

## 🧹 Data Cleaning (SQL)
Data cleaning was performed entirely using SQL. Steps included:
- Removing duplicates
- Handling missing values
- Standardizing text fields (Region, Category, Sub-Category)
- Filtering invalid or zero-value sales records

**Example SQL Queries**
## Data Cleaning

The following SQL query was used to remove duplicate records.

```sql
DELETE FROM clean_sales
WHERE id NOT IN (
    SELECT MIN(id)
    FROM clean_sales
    GROUP BY OrderID
);
```


## Exploratory Data Analysis (EDA)

During exploratory analysis, the dataset was analyzed to understand overall sales performance, profitability, and trends. Key areas explored included:

- Overall sales and profit distribution
- Sales performance across regions
- Profitability by product category
- Impact of discounts on profit

## Visualisation
<img width="893" height="501" alt="Screenshot (46)" src="https://github.com/user-attachments/assets/c075a111-e021-453e-84a5-c5e095c85a0b" />








## Key Insights
- Technology products contribute the highest profit margins.
- Furniture shows strong sales volume but weaker profitability.
- High discount levels correlate with reduced profit.

## Recommendations
- Prioritize high-margin product categories in sales strategy.
- Review discount policies to protect profitability.
- Align inventory planning with seasonal demand patterns.
- Investigate and optimize loss-making product segments.


---
## Project Structure
├── data/
├── sql/
├── powerbi/
├── visuals/
└── README.md




