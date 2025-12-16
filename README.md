# 📊 Sales Data Analysis Project (SQL + Power BI)

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
### KPI Overview
<img width="802" height="545" alt="sales_kpi" src="https://github.com/user-attachments/assets/a46cf370-f766-41f8-b9ae-a38123892053" />
<img width="793" height="523" alt="order_quantity_kpi" src="https://github.com/user-attachments/assets/bd409467-2989-4a70-9776-9a44a793d0be" />
<img width="793" height="525" alt="profit_by_category" src="https://github.com/user-attachments/assets/b52bdb4c-9a74-4b45-bc58-b1f125075044" />
<img width="793" height="454" alt="profit_margin" src="https://github.com/user-attachments/assets/7c0e38c8-9678-4193-b691-ce5a762f788f" />

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




