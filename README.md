# AnyoneAI-Technical-Challenge

---

# 📊 Customers and Orders Analysis

## Overview

This project analyzes customer and order data using Python to extract key business insights. The goal is to process CSV files (`customers.csv` and `orders.csv`) and answer analytical questions related to customer distribution and sales performance.

---

## 📁 Datasets

* **customers.csv**

  * CustomerID, FirstName, LastName, City, State
* **orders.csv**

  * CustomerID, OrderID, Date, OrderTotal, ProductName, Price

---

## ⚙️ Approach

* Used Python standard libraries (`csv`, `os`)
* Processed data using:

  * Dictionaries for aggregation
  * Sets to avoid duplicate orders
* Applied data cleaning:

  * `.strip()` for whitespace
  * `.upper()` for consistency

---

## 🔍 Key Logic

* **Unique orders:** handled with `set(OrderID)`
* **Items per order:** counted occurrences per order
* **Customer spending:** aggregated using `OrderTotal` (avoiding duplicates)
* **Time analysis:** extracted month from date (`YYYY-MM`)

---

## 📈 Results

### Customers

* Total customers: **602**
* Different states: **14**
* State with most customers: **CA**
* States with least customers: **ID, IN, MA, NH, OR, WA**
* Most common last name: **Smith**

### Orders

* Unique orders: **16672**
* Average items per order: **1.76**
* Max items in a single order: **35**
* Orders in October 2021: **267**
* Top customer (2021): **Brandon Divas (5172443)**
* Best month for sales: **January**

---

## 🧠 Notes

* Orders contain multiple rows per order (one per product), so deduplication is required.
* `OrderTotal` must be used instead of `Price` to avoid incorrect aggregation.
* Some inconsistencies exist between dataset results and quiz options, but calculations were validated directly from data.

---

