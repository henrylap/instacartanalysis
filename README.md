# :
## Table of Contents
- [Project Background](#project-background)
- [Data Description](#data-descrption)
- [Executive Summary](#executive-summary)
- [Key KPIs](#key-kpis)
- [Dashboard Insights](#dashboard-insights)
- [SQL-Driven Exploratory Analysis](#sql-driven-exploratory-analysis)
  - [Customer Retention](#customer-retention)
  - [Basket Dynamics](#basket-dynamics)
  - [Product & Category Insights](#product--category-insights)
- [Recommendations](#recommendations)
- [Conclusion](#conclusion)

## Project Background
Instacart is a U.S.-based online grocery delivery and pickup platform, partnering with over 1,800 retailers and servicing more than 100,000 individual stores.  
This project analyzes a combined dataset of ~1.4 million orders across ~120,000 users, created by joining the **prior** and **train** order subsets.  
The analysis focuses on market basket behavior, including basket size, reorder rates, product and department frequency, and temporal ordering patterns.  

## Data Description
1. **Orders** – Contains information on each order placed, including order ID, user ID, order number, evaluation set (prior/train/test), day of week, hour of day, and days since prior order.  
2. **Order_Products** – Line-item detail linking orders to products purchased, including product ID, add-to-cart order, and whether the product was reordered. Provided in two subsets:  
   - `order_products__prior` (historical orders)  
   - `order_products__train` (final orders with released products)  
3. **Products** – Contains product-level details, including product ID, product name, aisle ID, and department ID.  
4. **Aisles** – Describes aisle IDs and aisle names.  
5. **Departments** – Describes department IDs and department names.
   
*Entity–Relationship Diagram (ERD) of the Instacart dataset*
<img width="584" height="357" alt="instacart RS" src="https://github.com/user-attachments/assets/4b13e6ee-a591-4d98-a717-e6796a613061" />

## Executive Summary
Instacart’s basket analysis of ~1.4M orders from ~120k users showed an average basket size of 3 items and an overall reorder rate near 80%. Order volume peaked on Sundays and Mondays, with most activity between 9 AM and 4 PM. Produce was the leading department, accounting for ~1.4M items purchased and the highest reorder rate at 84%. In terms of retention, 93% of users placed at least two orders, but that share dropped to 64% at five orders and 37% at ten.
