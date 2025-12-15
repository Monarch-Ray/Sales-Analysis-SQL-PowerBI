# 📊 Sales Data Analysis Project (SQL + Power BI)

## 📌 Project Overview
This project analyzes retail sales data to evaluate overall sales performance, profitability, and customer purchasing patterns.  
The objective is to generate data-driven insights that can support better business decisions such as pricing strategy, regional focus, and product optimization.

---

## ❓ Business Questions
- What is the total sales and total profit?
- Which regions generate the highest sales and profit?
- Which product categories and sub-categories are most profitable?
- Which products consistently generate losses?
- How do discounts impact profitability?
- Are there any noticeable seasonal trends in sales?

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
);

-- Convert date format
ALTER TABLE clean_sales
ALTER COLUMN OrderDate DATE;


<img width="793" height="454" alt="profit_margin" src="https://github.com/user-attachments/assets/3f1bd08a-70f8-41c3-b64b-b51dbb6d5138" />
<img width="793" height="525" alt="profit_by_category" src="https://github.com/user-attachments/assets/e946fca9-7135-4ae6-9907-9acadb1e6125" />
<img width="793" height="523" alt="order_quantity_kpi" src="https://github.com/user-attachments/assets/3efb4544-222e-4384-9a04-30b3d714a323" />
<img width="802" height="545" alt="sales_kpi" src="https://github.com/user-attachments/assets/03d4f14f-ef2c-4204-a4fe-4ca997d2d1ca" />
## 📊 Visualizations

### KPI Overview – Sales & Orders
<img width="802" height="545" alt="sales_kpi" src="https://github.com/user-attachments/assets/03d4f14f-ef2c-4204-a4fe-4ca997d2d1ca" />
<img width="793" height="523" alt="order_quantity_kpi" src="https://github.com/user-attachments/assets/3efb4544-222e-4384-9a04-30b3d714a323" />

### Profit Analysis
<img width="793" height="454" alt="profit_margin" src="https://github.com/user-attachments/assets/3f1bd08a-70f8-41c3-b64b-b51dbb6d5138" />

### Profit by Category
<img width="793" height="525" alt="profit_by_category" src="https://github.com/user-attachments/assets/e946fca9-7135-4ae6-9907-9acadb1e6125" />
