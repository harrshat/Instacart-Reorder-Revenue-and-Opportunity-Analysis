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






