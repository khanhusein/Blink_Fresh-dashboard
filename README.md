# BLINK FRESH — Sales & Operations Dashboard (Power BI)

An end-to-end **sales, outlet and delivery-operations analytics dashboard** built in Power BI, covering revenue performance, outlet and location analysis, item-level insights, customer and order behaviour, and delivery/fulfilment — all on one data model of quick-commerce grocery orders.

> 📊 Power BI Desktop | 7 report pages | 8,523 orders | 9 cities | 10 outlets | 16 item types | Jan – Jul 2026

---

## 📌 Project Overview

Quick-commerce businesses need one place to see revenue, outlet performance, product quality and delivery efficiency together instead of siloed reports. This project analyses **8,523 BLINK FRESH orders (January 2026 – July 2026)** across **9 cities and 10 outlets**, and turns them into an interactive Power BI report for business and operations teams.

Every analytical page (3–7) follows the same design: **KPI cards on top, a set of charts below, consistent colours and navigation buttons** — each page looks at a different slice of the data.

**Note:** this is a portfolio / learning project built to demonstrate Power BI skills. It is not official company data.

---

## 🖼️ Dashboard Preview

### Cover
![Cover](screenshots/01_cover.png)

### Introduction
![Introduction](screenshots/02_introduction.png)

### Sales Performance
![Sales Performance](screenshots/03_sales_performance.png)

### Outlet & Location Analysis
![Outlet & Location Analysis](screenshots/04_outlet_location.png)

### Item-Level Insights
![Item-Level Insights](screenshots/05_item_insights.png)

### Customer & Order Detail
![Customer & Order Detail](screenshots/06_customer_order.png)

### Order & Fulfillment Analysis
![Order & Fulfillment Analysis](screenshots/07_fulfillment.png)

---

## 🗂️ Data Model

A single fact table, **`blink_fresh_data`**, with one row per order line, plus DAX measures for every KPI.

| Field group | Columns |
|---|---|
| **Order** | Order ID, Order Date, Quantity, Sales, Discount %, Payment Mode, Delivery Status |
| **Customer** | Customer Name |
| **Item** | Item Identifier, Item Type, Item Category, Item Fat Content, Item Visibility (%), Item Weight |
| **Outlet** | Outlet Identifier, Outlet Type, Outlet Size, Outlet Location Type, Outlet Establishment Year |
| **Location** | City |

**Key DAX measures:** `Total_Sales`, `Total_order`, `Unique_Customer`, `Total_Quantity`, `Average_Rating`, `Avg_sales`, `Maximum_Sales`, `minimum_sales`, `Delivered_Orders`, `Cancelled_Orders`, `Returned_Orders`, `Delivery_Success_Rate_%`, `Cancelled_Order_Rate_%`, `Delivered_Sales`, `Average_Sales_per_Outlet`, `Average_Outlet_Age`, `average_discount_%`, `Total_Discount_Amount`, `Average_item_visibility`, `High_Rating_Item_count`, `Low_visibility_Item_count`, `Average_Days_Since_Order` and more.

---

## 📑 Report Pages

### 1. Cover
Landing page with the project title and navigation into the report.

---

### 2. Introduction
Project overview and headline numbers.

**KPIs:**
- Total Sales: **₹12,01,681**
- Average Rating: **3.97 / 5**
- Delivery Success Rate: **66.8%**
- Total Orders: **8,523**
- Outlet Count, Unique Customers, Total Quantity

**Visuals:** Sales by Outlet Type

**Filters:** Outlet Location Type / City / Item Category

---

### 3. Sales Performance
How much the business sells, and where it comes from.

**KPIs:**
- Average Sales
- Maximum Sales
- Minimum Sales
- Total Item Types
- Average Item Weight

**Breakdowns:** Sales by Item Type, average sales by Outlet Size, sales by Outlet, sales by Payment Mode, average sales per weight by Item Category, sales trend by Outlet Establishment Year

---

### 4. Outlet & Location Analysis
Which outlets and locations perform best.

**KPIs:**
- City Count
- Average Outlet Age
- Average Sales per Outlet
- Average Item Weight
- Newest Outlet Age

**Breakdowns:** Sales by Outlet Location Type (donut), Outlet Type × Location Type sales table, outlets by location type, average rating / outlet age / item weight by Outlet Type

---

### 5. Item-Level Insights
Which products drive sales and quality.

**KPIs:**
- Item Count
- Average Item Visibility
- Average Discount %
- High-Rating Item Count
- Low-Visibility Item Count

**Breakdowns:** Visibility vs Sales (scatter), Discount % vs Sales (scatter), sales by Fat Content, sales by Item Type (treemap), average rating by Item Type, item count by Item Category

---

### 6. Customer & Order Detail
How customers order and how orders end up.

**KPIs:**
- Delivered Orders
- Cancelled Orders
- Returned Orders
- Delivery Success Rate %
- Average Quantity per Order
- Total Orders, Unique Customers

**Breakdowns:** Sales by Customer, sales by Payment Mode, delivered vs cancelled orders by Outlet Type, sales by City

---

### 7. Order & Fulfillment Analysis
Delivery performance, payments and geography.

**KPIs:**
- Total Discount Amount
- Payment Mode Count
- Average Days Since Order
- Cancelled Order Rate %
- Delivered Sales

**Breakdowns:** Sales trend by Order Date, orders by Payment Mode, sales map by City, orders by Delivery Status, quantity by Item Type, average discount % by Outlet Type

---

## 💡 Key Insights

✅ **Business Snapshot**
- 8,523 orders generated ₹12,01,681 in sales between January and July 2026
- Spread across 9 cities, 10 outlets and 16 item types

✅ **Delivery Performance**
- Delivery success rate is 66.8%, so roughly one in three orders is cancelled, returned or otherwise not delivered
- Cancellation, return and delivery-status views on pages 6 and 7 show where the losses come from

✅ **Customer Satisfaction**
- Average rating is 3.97 out of 5, a solid but improvable score
- Item-level pages highlight high-rating items and low-visibility items to focus on

✅ **Outlet & Location Strategy**
- Outlet Type, Size and Location Type comparisons show which formats and tiers earn the most per outlet
- Outlet age vs sales helps judge whether newer outlets are catching up

---

## 🛠️ Skills Demonstrated

| Area | Evidence |
|---|---|
| **Data Modelling** | Clean order-level table with outlet, item, customer and location attributes |
| **DAX** | Sales, rate, average, min/max and count measures used across every page |
| **Dashboard/UX Design** | Consistent KPI-cards + charts layout, custom backgrounds, icons and navigation buttons |
| **Data Storytelling** | Logical flow: overview → sales → outlets → items → customers → fulfilment |
| **Domain Knowledge** | Quick-commerce KPIs: delivery success, cancellation rate, item visibility, outlet performance |
| **Visualization Range** | Cards, column/bar/clustered, line, pie/donut, treemap, scatter, map, matrix table, slicers |

---

## 🚀 Quick Start

### Prerequisites
- **Power BI Desktop** (free download from [Microsoft](https://powerbi.microsoft.com/en-us/desktop/))

### Steps
1. **Clone this repo**
   ```bash
   git clone https://github.com/khanhusein/blinkit-fresh-power-bi-dashboard.git
   cd blinkit-fresh-power-bi-dashboard
   ```

2. **Open the dashboard**
   - Double-click `Blink_Fresh_Dashboard.pbix`
   - Or open Power BI Desktop → File → Open

3. **Explore the slicers**
   - Filter by Outlet Location Type, City and Item Category, and use the navigation buttons to move between pages

---

## 📂 Project Structure

```
blinkit-fresh-power-bi-dashboard/
├── README.md
├── LICENSE
├── Blink_Fresh_Dashboard.pbix
└── screenshots/
    ├── 01_cover.png
    ├── 02_introduction.png
    ├── 03_sales_performance.png
    ├── 04_outlet_location.png
    ├── 05_item_insights.png
    ├── 06_customer_order.png
    └── 07_fulfillment.png
```

---

## 🔮 Future Enhancements

- [ ] Drillthrough pages from summary cards to order-level detail
- [ ] Reduce cancellations: root-cause view by outlet, city and payment mode
- [ ] Live/scheduled-refresh data source (replace static import)
- [ ] Mobile-optimized dashboard views
- [ ] Forecasting of sales and order volume
- [ ] Row-level security by city or outlet manager

---

## 📝 License

This project is licensed under the [MIT License](LICENSE).

---

## 👤 Author

**Mohammed Husein Khan**

🔗 **Links:**
- [LinkedIn](https://www.linkedin.com/in/mohammed-husein-khan-615645427)
- [GitHub](https://github.com/khanhusein)

---

## 💬 Questions?

Feel free to open an **Issue** on GitHub or connect via LinkedIn for questions or collaboration opportunities.

---

**Last Updated:** September 24, 2026  
**Power BI Version:** Latest Desktop  
**Data:** Quick-commerce order dataset (Jan – Jul 2026)
