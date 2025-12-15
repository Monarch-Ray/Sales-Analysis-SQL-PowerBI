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
  Key Takeaway:
  . Sales are healthy, but growth can be accelerated by prioritizing top-performing regions.
  
- How profitable is the business?
   Answer:
  . The business is profitable overall, with a positive profit margin.
  . Profitability varies significantly by product category.
 Key Takeaway:
  . There is an opportunity to improve margins by optimizing underperforming categories.
  
- Which categories generate the most profit?
   Answer: 
  . Technology is the most profitable category.
  . Office Supplies perform moderately well.
  . Furniture generates high sales but low profit margins.
 Key Takeaway:
  . High-margin categories should be prioritized to maximize profitability.
  
- Which areas negatively impact profitability?
   Answer:
  . Certain sub-categories consistently generate losses.
  . Losses are driven by high discount rates and cost structures.
Key Takeaway:
  . Loss-making products require pricing, discount, or cost review.
  
- What is the impact of discounts on profit?
  Answer:
  . Higher discounts are strongly associated with lower profit.
  . Discounting is most harmful in Furniture and Office Supplies.
 Key Takeaway:
  . Discount strategies should be optimized to protect profit margins.
  
- What should management prioritize?
  Answer
  . Focus on high-performing regions and categories.
  . Reduce excessive discounting.
  . Improve or eliminate consistently loss-making products.
 Key Takeaway:
  . Targeted optimization will improve both revenue growth and profitability.

---

## 📂 Data Source
- Dataset: Sample Superstore Dataset (Kaggle)  
- Region, Category, Sub-Category, Sales, Profit, Discount, Quantity  
- [Insert Dataset Link Here]

---

## 🧹 Data Cleaning (SQL)
Data cleaning was performed entirely using SQL. Steps included:
- Removing duplicates
- Handling missing values
- Standardizing text fields (Region, Category, Sub-Category)
- Filtering invalid or zero-value sales records

**Example SQL Queries**
```sql
-- Remove duplicates
DELETE FROM clean_sales
WHERE id NOT IN (
  SELECT MIN(id)
  FROM clean_sales
  GROUP BY OrderID
)

## Visualisation

