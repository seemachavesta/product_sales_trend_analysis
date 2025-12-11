
---

## Tools & Technologies Used

### **Languages**
- Python (Pandas, Matplotlib)

### **Visualization**
- Tableau Public

### **Other Tools**
- Jupyter Notebook  
- Git & GitHub  

---

## Dataset Description

This project uses the **Olist Brazilian E-Commerce Public Dataset** from Kaggle.

The dataset includes:
- Orders (timestamps, status)
- Order items (price, freight cost)
- Product information (categories)
- Customer data

Only relevant tables were used:
- `orders_dataset.csv`
- `order_items_dataset.csv`
- `products_dataset.csv`

---

##  Data Cleaning & Preparation (Python)

The following steps were performed in Jupyter notebooks:

### **Orders Dataset**
- Filtered only *delivered* orders  
- Converted timestamps to datetime  
- Extracted `year`, `month`, `year_month`  
- Kept only required columns  
- Saved cleaned file as:  
  `orders_clean.csv`

### **Order Items Dataset**
- Kept required columns:  
  `order_id`, `product_id`, `price`, `freight_value`  
- Calculated **total sales = price + freight**  
- Saved cleaned file:  
  `order_items_clean.csv`

### **Products Dataset**
- Kept only: `product_id`, `product_category_name`  
- Filled missing categories with `"unknown"`  
- Saved cleaned file:  
  `products_clean.csv`

### **Merged Dataset**
- Merged all cleaned datasets  
- Created year-month period  
- Aggregated:  
  - Monthly sales  
  - Monthly order count  
  - Category-level monthly sales  

Saved files used for Tableau:
- `monthly_sales_orders.csv`
- `category_monthly_sales.csv`

---

##  Key Insights

### **1. Monthly Sales Trends**
- Highest sales occurred in **Nov 2017**  
- Lowest sales were in **Sep 2016**  
- Strong growth from **early 2017 to late 2017**  
- Decline begins in early **2018**

### **2. Monthly Order Volume**
- Follows the same pattern as sales  
- Peak order count also in **Nov 2017**  
- Lowest volume in dataset start months (2016)

### **3. Category-Level Insights**
Top-performing categories showed:
- Strong seasonal trends  
- Consistent revenue contribution  
- Some categories (e.g., health & beauty) showed stable growth

### **4. KPIs**
- **Total Sales:** 13,221,498.11(calculated from full dataset)  
- **Total Orders:** 96,478 delivered orders  


---

##  Tableau Dashboard Features

The dashboard includes:
- Monthly Sales Trend Line Chart  
- Monthly Order Volume Trend  
- Top Product Categories by Sales  
- Category Sales Trends Over Time  
- KPI Cards (Total Sales, Total Orders)

Designed for business users such as:
- E-commerce managers  
- Category managers  
- Inventory planners  

---

## Tableau Dashboard Link
https://public.tableau.com/views/OlistE-CommerceSalesDashboardBrazil20162018/OlistSalesDashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link 

