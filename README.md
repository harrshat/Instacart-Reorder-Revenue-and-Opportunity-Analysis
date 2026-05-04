# 🛒 Instacart Reorder Revenue & Opportunity Analysis

<p align="center">
<img width="557" height="83" alt="image" src="https://github.com/user-attachments/assets/2087b505-c859-49ce-a33b-be77ae9a79f6" />
</p>

## 📌 About Instacart
**Instacart** is a grocery delivery marketplace.  
Its revenue model depends heavily on **order frequency** — the more often customers reorder, the more revenue per user over time.

## 🎯 Problem Statement
The growth team observed that many customers place their first order but do not continue ordering regularly. Due to the structure of the dataset, the earliest point where repeat behavior and drop-off can be analyzed is from the third order onward.

Amongst those who do reorder, a meaningful portion go quiet after a few orders. At which step in the reorder journey are we losing the most customers, and which product categories show the highest drop-off? What behaviors in the first few orders separate high-value customers from at-risk ones — and how large is the gap between them?

## Link to the dataset:
https://www.kaggle.com/datasets/psparks/instacart-market-basket-analysis/data 

## 🗃️ Data Description
- orders.csv — One row per order. Contains user_id, order_number (1st, 2nd, 3rd order, etc.), order_dow (day of week), order_hour_of_day, and days_since_prior_order.
- order_products__prior.csv — One row per product per order, for all orders in a user’s history. Contains order_id, product_id, add_to_cart_order, and reordered (1 if the product was in a previous order).
- products.csv — Product names and their department and aisle IDs.
- departments.csv — Maps department_id to department name (e.g., produce, dairy eggs, beverages).

## Key Findings:
1 - **Reorder Funnel:** The steepest single-step drop-off is at Order 4 → 5. 11.63% drop-off at Order 4 → 5 largest single step drop.

<p align="center">
<img width="570" height="351" alt="image" src="https://github.com/user-attachments/assets/f8536185-dcae-440d-aeee-4ad1fc1d0639" />
</p>

2 - ** Revenue gap - Customer Segments: ** -  Both segments buy the same amount per order (median 8 items). High-Value customers order every 7 days vs every 19 days for At-Risk. Interventions should target reorder timing and order frequency — not cart size.

<p align="center">
<img width="601" height="271" alt="image" src="https://github.com/user-attachments/assets/857b880a-3046-4f70-ac60-4018d3225988" />
</p>

3- ** Category Leakage -  At-Risk Customers: ** - Personal Care - Only 3,830 of 13,372 (28.6%) At-Risk customers who bought from this dept in Order 1 came back by Order 3 — the lowest absolute reorder rate among high-volume departments. Consumables like shampoo and toothpaste should drive repeat purchases; low reorder rates signal Instacart is losing this volume to competitors.
<p align="center">
<img width="554" height="333" alt="image" src="https://github.com/user-attachments/assets/ce10098f-5629-4a42-9931-d859a5738504" />
</p>

## Business Recommendation: 
Flag customers whose days_since_prior_order exceeds the median (7 days for High-Value) after Order 1. This identifies at-risk customers at the earliest actionable moment. A personalised in-app prompt at Order 2 featuring the top-dropped department from their Order 1 basket. 

Priority departments: Personal Care (lowest absolute reorder rate, 28.6%) and Alcohol (largest gap vs High-Value, 15 percentage points).







