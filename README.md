# Power-BI-DashBoard
# 📊 Adventure Works Sales Analysis Dashboard – Power BI Project

This Power BI project explores and analyzes sales performance data from the fictional **Adventure Works** company — a Microsoft-provided sample dataset widely used to practice business intelligence and visualization skills.

> 🎯 This project aims to demonstrate strong BI development skills by creating an executive-level dashboard that turns raw data into actionable business insights.

---

## 🧠 Project Objectives

- Visualize trends in sales, orders, and profit margins over time  
- Identify the best-performing product categories and regions  
- Support business strategy through meaningful KPIs and visuals  
- Showcase DAX proficiency and dashboard storytelling using Power BI  

---

## 🗂 What’s Included

This Power BI report includes the following pages and features:

### 📍 Dashboard Pages

Here’s a breakdown of each page included in the Power BI report:

### 1️⃣ **Main Page – Executive Overview**
- High-level KPIs: Total Sales, Total Orders, Profit, Profit Margin
- Monthly trend chart visualizing sales over time
- Interactive slicers for year and product category
- Visual cards for quick-glance performance

### 2️⃣ **Product Performance Page**
- Bar charts showing revenue by Product Category and Subcategory
- Heatmap of profit contribution per product
- Top 5 best-selling products by revenue
- Drill-through enabled for detailed product-level insights

### 3️⃣ **Geographic Sales Map Page**
- Interactive map showing total sales by country/region
- Bar chart for profit comparison by region
- Helps identify geographic patterns in performance
- Zoom and tooltip capabilities for enhanced interactivity

### 4️⃣ **Customer Insights Page**
- Customer segmentation by region, age group, and gender
- Total sales by customer type (new vs. returning)
- Visual analysis of customer purchasing behavior
- Slicers to filter customer data across multiple dimensions

---

## 📊 Dataset Used

The report is built using the **Adventure Works DW sample dataset**, which includes tables such as:

- `Sales`: Contains order details, sales amount, cost, and revenue  
- `Product`: Includes product categories, subcategories, and SKUs  
- `Customer`: Geographic and demographic customer info  
- `Date`: Full calendar table used for time intelligence  

> ✅ Note: This is a cleaned and structured version of the Adventure Works dataset used specifically for reporting.

---

## ⚙️ Key DAX Measures & Explanations

Here are some important DAX measures used in the report:

### 💰 Total Sales
```dax
Total Sales = SUM(Sales[SalesAmount])
```
🧾 Total Orders
```dax
Total Orders = COUNT(Sales[SalesOrderNumber])
```
📈 Profit
```dax
Profit = SUM(Sales[SalesAmount]) - SUM(Sales[TotalProductCost])
```
📉 Profit Margin
```dax
Profit Margin = DIVIDE([Profit], [Total Sales], 0)
```
🏆 Top Products
```dax
Top Products = 
TOPN(
    5,
    SUMMARIZE(Product, Product[ProductName], "Revenue", [Total Sales]),
    [Total Sales],
    DESC
)
```
Returns the top 5 products based on total sales using summarization and dynamic ranking.

## 💡 Sample Insights

- **Seasonality Detected**: Sales consistently peak in Q4 (especially November–December).
- **Product Performance**: Mountain Bikes generate the most revenue; Accessories have high volume but low margins.
- **Regional Opportunity**: The Western region leads in revenue; Central and Northeast regions show untapped potential.
- **Inventory Strategy**: A few top products (Pareto Principle – 80/20 rule) contribute the majority of sales; ensure these are always in stock.

---

## 📁 How to Use

1. Clone this repository or download the `.pbix` file.
2. Open the file using **Power BI Desktop**.
3. Interact with the dashboards or modify visuals to explore deeper insights.
4. Try building your own measures and visuals to customize the report.

---

## 📬 Contact

Created by **Soham Samir Gawde**  
📧 Email: [sohamsgawde10@gmail.com](mailto:sohamsgawde10@gmail.com)  
🔗 LinkedIn: [linkedin.com/in/sohamgawde10](https://linkedin.com/in/sohamgawde10)

---

## 📝 License

This project is intended for **educational and portfolio purposes only**.  
