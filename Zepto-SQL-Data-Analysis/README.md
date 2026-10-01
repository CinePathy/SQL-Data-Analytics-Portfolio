# 🛒 Zepto SQL Data Analysis

## 📌 Project Overview

This project analyzes Zepto product data using **PostgreSQL and SQL**.

The objective is to explore product categories, pricing, discounts, stock availability, inventory value, product weight, and product-level pricing to generate useful business insights.

The project follows the complete SQL workflow:

**Data Exploration → Data Cleaning → Data Transformation → Data Analysis → Business Insights**

---

# 📊 Dataset

The dataset contains product-level information from Zepto.

## Columns

| Column | Description |
|---|---|
| `sku_id` | Unique identifier for each product SKU |
| `category` | Product category |
| `name` | Name of the product |
| `mrp` | Maximum Retail Price |
| `discountPercent` | Discount percentage offered on the product |
| `availableQuantity` | Number of units currently available |
| `discountedSellingPrice` | Selling price after applying the discount |
| `weightInGms` | Product weight in grams |
| `outOfStock` | Indicates whether the product is out of stock |
| `quantity` | Product/pack quantity |

---

# 🛠️ Technology Used

- PostgreSQL
- SQL
- Git
- GitHub

---

# 🔍 Operations Performed

## 1. Database & Table Creation

Created a PostgreSQL table named `zepto` with appropriate:

- Data types
- Primary key
- `NOT NULL` constraint
- Numeric fields
- Boolean stock-status field

---

## 2. Data Exploration

Performed initial exploration to understand the dataset.

### Operations performed:

- Counted total number of records
- Viewed sample records
- Identified unique product categories
- Checked for NULL values
- Analyzed in-stock vs out-of-stock products
- Identified product names appearing multiple times

# 💡 Business Insights

The Zepto SQL analysis provides insights into **product availability, pricing, discounts, inventory value, product value, and category-level inventory distribution**.

---

## 📦 1. Product Availability

After data cleaning, the dataset contains **3,731 product/SKU records**.

- **3,278 products (87.86%)** are in stock.
- **453 products (12.14%)** are out of stock.

This shows that the majority of products are available, while around **12% of the product catalog is unavailable**.

The out-of-stock products can be further investigated to identify potential inventory replenishment requirements and stock-management issues.

---

## 🛍️ 2. Product Catalog Diversity

The dataset contains:

- **14 product categories**
- **1,680 unique product names**

Multiple SKUs are associated with some product names, indicating that the catalog contains repeated product listings or different SKU-level representations.

This highlights the importance of analyzing products at both the **product-name level and SKU level**.

---

## 🏷️ 3. Discount Analysis

The average discount across the cleaned dataset is approximately **7.62%**.

The maximum discount observed is **51%**.

This shows that discounting varies significantly across products, with some products receiving substantially higher discounts than the overall average.

The category with the highest average discount is:

**Fruits & Vegetables — approximately 15.46%**

followed by:

**Meats, Fish & Eggs — approximately 11.03%**

This indicates that discount strategies differ across product categories.

---

## 🔥 4. Highly Discounted Products

The analysis identified products with discounts of up to **51%**.

Examples of highly discounted products include:

- Dukes Waffy Chocolate Wafers
- Chef's Basket Durum Wheat Pasta
- Ceres Foods Instant Liquid Masala products

Highly discounted products may be associated with promotional campaigns, competitive pricing, customer acquisition strategies, or inventory clearance.

---

## 💰 5. High-MRP Products That Are Out of Stock

The analysis identified relatively expensive products that are currently unavailable.

Examples include:

- Patanjali Cow's Ghee — ₹565
- MamyPoko Pants Standard Diapers, Extra Large — ₹399
- Aashirvaad Atta With Multigrains — ₹315

These products may require closer inventory monitoring because their unavailability can potentially result in missed sales opportunities.

---

## 📊 6. Estimated Inventory Value by Category

The project estimates inventory value using:

```text
Estimated Inventory Value
=
Discounted Selling Price × Available Quantity
