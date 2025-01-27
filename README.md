# Pizza Store Sales Analysis

## 1. Introduction
This report presents the findings from an analysis of a pizza store’s annual sales data. The dataset includes details about orders, pizzas served, their sizes, prices, and ingredients. The primary goal of the analysis was to extract actionable insights and identify trends to improve business strategies.

## 2. Objectives
The analysis aimed to answer the following key questions:
- How many customers visit the store daily, and what are the peak hours?
- How many pizzas are typically ordered in a single transaction? What are the bestselling pizzas?
- What are the total sales for the year, and are there any seasonal trends?
- Are there any pizzas that should be removed from the menu, or any promotional opportunities?

---

## 3. Analysis Steps and Findings

### **3.1 Daily Customer Count and Peak Hours**
- **Assumption:** One pizza equals one customer.
- **Steps:**
  - Added `Date` (from Orders) to columns and `Quantity` (from Order Details) to rows.
  - Calculated daily average customers as **1,599.16 per day**.
  - Added `Time` (from Orders) to columns and `Quantity` (from Order Details) to rows, revealing **12 PM to 1 PM as the peak hour**.

**Analysis Image:**
![Daily Customer Count and Peak Hours](images/daily_customer_count.png)

### **3.2 Typical Order Size and Bestsellers**
- **Typical Order Size:**
  - Added `Order ID` (from Orders) to columns and `Pizza ID` (from Order Details) to rows.
  - Found that an average order contains **2.28 pizzas**.

- **Bestselling Pizzas:**
  - Added `Pizza ID` (from Order Details) to columns and `Quantity` (from Order Details) to rows.
  - Filtered for top 10 bestselling pizzas based on descending order of sales.

**Analysis Image:**
![Typical Order Size and Bestsellers](images/typical_order_size.png)

### **3.3 Total Sales and Seasonality**
- **Total Sales:**
  - Created a calculated field `Total Sales = Quantity * Price`.
  - Found total annual sales to be **$817,860**.

- **Seasonal Trends:**
  - Added `Total Sales` to rows and `Date` (from Orders) to columns, grouped by month.
  - Identified seasonal trends via a line graph.

**Analysis Image:**
![Total Sales and Seasonality](images/total_sales_seasonality.png)

### **3.4 Menu Optimization and Promotions**
- **Category Performance:**
  - Added `Category` (from Pizza Types) to columns and both `Total Sales` and `Quantity` to rows.
  - Results:
    - Sales: Classic > Supreme > Chicken > Veggie.
    - Quantity: Classic > Supreme > Veggie > Chicken.

- **Size Performance:**
  - Added `Size` (from Pizza Types) to columns and both `Total Sales` and `Quantity` to rows.
  - Results:
    - Sales: L > M > S > XL > XXL.
    - Quantity: L > M > S > XL > XXL.
  - Observed low sales for XL and XXL sizes; recommend promotional strategies for these sizes.

- **Promotions for Larger Orders:**
  - Created a calculated field `No. of Pizzas per Order = {FIXED [Order ID] : COUNTD([Pizza ID])}`.
  - Found most customers order between **1 and 4 pizzas**, suggesting promotions targeted at these groups.

**Analysis Image:**
![Menu Optimization and Promotions](images/menu_optimization.png)

---

## 4. Dashboard Overview
The Tableau dashboard includes:
- **Daily Sales Analysis:** Visualizing customer count and peak hours.
- **Order and Bestseller Analysis:** Highlighting typical order sizes and top pizzas.
- **Revenue Trends:** Depicting total sales and seasonal patterns.
- **Menu and Promotion Insights:** Identifying low-performing items and promotion opportunities.

**Dashboard Image:**
![Dashboard Overview](images/dashboard_overview.png)

---

## 5. Conclusion
This analysis provided valuable insights into customer behavior, sales performance, and menu optimization opportunities. Key recommendations include:
- Introducing promotions for XL and XXL pizzas to boost sales.
- Targeting discounts for orders of 1 to 4 pizzas to encourage repeat customers.
- Leveraging peak hours (12 PM to 1 PM) with targeted marketing campaigns.

By implementing these strategies, the pizza store can enhance customer satisfaction and maximize revenue.

---

**Author:** [Your Name]  
**Project Files:** [GitHub Repository Link]  
**Tool Used:** Tableau

