
# E-commerce Data Dictionary

## Project Overview
This project simulates an e-commerce data platform
built using Databricks, PySpark, SQL, and Delta Lake.

All datasets are synthetic.

## 1. Customers

| Column | Data Type | Description |
|---|---|---|
| customer_id | STRING | Unique customer ID |
| customer_name | STRING | Synthetic customer name |
| city | STRING | Customer city |
| signup_date | DATE | Account registration date |

## 2. Products

| Column | Data Type | Description |
|---|---|---|
| product_id | STRING | Unique product ID |
| product_name | STRING | Product name |
| category | STRING | Product category |
| unit_price | DECIMAL(10,2) | Selling price |

## 3. Orders

| Column | Data Type | Description |
|---|---|---|
| order_id | STRING | Unique order ID |
| customer_id | STRING | Customer who placed the order |
| order_date | DATE | Purchase date |
| order_status | STRING | Order status |

## 4. Order Items

| Column | Data Type | Description |
|---|---|---|
| order_item_id | STRING | Unique order item ID |
| order_id | STRING | Related order |
| product_id | STRING | Purchased product |
| quantity | INT | Units purchased |
| unit_price | DECIMAL(10,2) | Price at time of purchase |

## Data Relationships

- One customer can place multiple orders.
- One order can contain multiple order items.
- One product can appear in multiple order items.

## Architecture

Bronze: Raw ingested records

Silver: Cleaned, validated, deduplicated records

Gold: Business-ready analytical tables
