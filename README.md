# 🍕 Pizza Sales Dashboard – Power BI Project

This repository contains an interactive **Pizza Sales Dashboard** built using **Power BI** by **Sawaira**.  
It provides deep insights into pizza sales performance, customer behavior, busiest days, best/worst sellers, and trends through both **Power BI visuals** and **SQL queries**.

![Dashboard Preview](Home.JPG)  
![Dashboard Preview](BestWorstSellers.JPG)

---

## 📁 Files Included

| File Name                           | Description                                      |
|------------------------------------|--------------------------------------------------|
| `Pizza Sales Report.pbix`          | Power BI dashboard project file                  |
| `pizza_sales.csv`                   | Raw dataset used for building the dashboard      |
| `PIZZA SALES SQL Steps.docx`        | Documented SQL queries and DAX steps             |
| `Home.JPG`                          | Dashboard Home Page preview                      |
| `BestWorstSellers.JPG`              | Dashboard Best/Worst Sellers preview             |

---

## 💡 Key Features

- 📌 **KPI Tiles**:
  - 🔹 Total Revenue: `817K`
  - 🔹 Total Orders: `21K`
  - 🔹 Total Pizzas Sold: `49K`
  - 🔹 Avg Order Value: `38`
  - 🔹 Avg Pizzas per Order: `2.3`


    ## 📐 DAX Columns & Measures – Pizza Sales Dashboard

```DAX
3. order_day =
   FORMAT(DATEVALUE([order_date]), "dddd")
   // New column → returns the full weekday name (e.g., Monday)

4. Total revenue =
   SUM('pizza_sales'[total_price])
   // KPI (New Measure)

5. Total Orders =
   DISTINCTCOUNT('pizza_sales'[order_id])
   // Total number of orders

6. Avg Order Value =
   [Total revenue] / [Total Orders]
   // Average Order Value

7. Total Pizzas Sold =
   SUM('pizza_sales'[quantity])
   // Total pizzas sold

8. Avg Pizza per order =
   [Total Pizzas Sold] / [Total Orders]
   // Average pizzas per order

9. order_day_num =
   WEEKDAY(DATEVALUE([order_date]), 2)
   // Returns numeric weekday (1=Monday, 7=Sunday)

10. Month_Name =
    FORMAT([order_date], "MMM")
    // Short month name (e.g., Jan, Feb)

11. Month_Num =
    MONTH([order_date])
    // Month number (1–12)


- 📊 **Visual Insights**:
  - Top 5 & Bottom 5 Pizzas by Revenue, Quantity, and Orders
  - Daily Trends for Total Orders (Mon–Sun)
  - Monthly Trends for Orders (Jan–Dec)
  - % Sales by Pizza Category & Size

- 🎯 **Best/Worst Sellers Analysis**:
  - Highlights pizzas generating the **maximum** and **minimum** revenue, quantity, and orders.

- 📈 **SQL Integration**:
  - KPIs and trends calculated using SQL queries for validation alongside Power BI.

---

## 🎨 Visual Components

- **Bar Charts** → Top/Bottom Pizza by Sales, Daily/Monthly Orders  
- **Line Charts** → Monthly Trends  
- **Donut Charts** → % Sales by Category & Size  
- **KPI Cards** → Core business metrics  
- **Text Cards** → Business Insights (Best/Worst sellers, busiest days/months)  

---

## 🛠️ Tools & Technologies

- **Power BI Desktop**  
- **SQL (PostgreSQL)**  
- **CSV Dataset**  
- **DAX Measures**  
- **Data Transformation & Modeling**

---

## 🚀 Getting Started

To explore the dashboard:

1. Download the `.pbix` file from this repo.  
2. Open in **Power BI Desktop**.  
3. Review KPIs, slicers (Category, Date), and dynamic visuals.  
4. Use provided SQL queries for validation or database integration.  

---

## 📌 Use Case

This project is ideal for:  
- Portfolio building for **Data Analysts / BI Developers**  
- Demonstrating **SQL + Power BI integration**  
- Business stakeholders tracking product sales, seasonal patterns, and top-performing pizzas  

---

## 👩‍💻 Author

**Sawaira Iqbal**  
> Power BI & SQL Developer | Data Visualization Enthusiast  
> _Crafted with 🍕 + 💖 to turn raw data into actionable insights_

---

⭐ *If you found this project useful, don’t forget to give it a star!*  
