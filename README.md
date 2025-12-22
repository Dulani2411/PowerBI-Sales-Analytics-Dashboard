# 📊 Sales & Customer Analytics Dashboard

An interactive Power BI dashboard analyzing 3 years of sales data (2015-2017) with comprehensive insights into revenue, customer behavior, and product performance.

![Executive Dashboard](https://github.com/Dulani2411/PowerBI-Sales-Analytics-Dashboard/blob/main/Screenshot%202025-12-10%20225408.png)

---

## 🎯 Project Overview

This project demonstrates end-to-end business intelligence solution development, from data modeling to interactive visualization. The dashboard enables stakeholders to monitor KPIs, identify trends, and make data-driven decisions.

**Project Metrics:**
- 📈 **$24.9M** total revenue analyzed
- 👥 **18,000+** unique customers
- 🛍️ **56,000+** transactions
- 📊 **30+** interactive visualizations
- 🌍 **3** continents covered

---

## ✨ Key Features

### 1. Executive Dashboard
- 6 high-level KPIs (Revenue, Orders, Customers, AOV, Return Rate, Profit Margin)
- Revenue trend analysis over 3 years
- Geographic distribution with interactive map
- Top 10 products by revenue
- Sales breakdown by category and continent

### 2. Sales Performance Analysis
- Monthly revenue trends with profit margin overlay
- Product cost vs. price scatter plot analysis
- Revenue breakdown by product category and subcategory
- Product style performance waterfall chart
- Detailed matrix with drill-through capabilities

### 3. Customer & Returns Analysis
- Customer demographics (Gender, Education, Marital Status)
- Revenue analysis by customer segments
- Returns trend over time
- Top 10 returned products
- Geographic distribution of returns
- Return rate by product category

---

## 🛠️ Technical Implementation

### Data Model
- **Architecture:** Star Schema
- **Tables:** 7 (Sales, Customers, Products, Returns, Territories, Product_Categories, Product_Subcategories)
- **Relationships:** Properly configured with appropriate cardinality
- **Grain:** Transaction-level detail

![Data Model]("C:\Users\User\Pictures\Screenshots\Screenshot 2025-12-10 230326.png")

### DAX Measures (Key Examples)
```dax
// Revenue Calculation
Total Revenue = 
SUMX(
    Sales,
    Sales[OrderQuantity] * RELATED(Products[ProductPrice])
)

// Profit Margin
Profit Margin % = 
DIVIDE(
    [Total Revenue] - [Total Cost],
    [Total Revenue],
    0
) * 100

// Return Rate
Return Rate % = 
DIVIDE(
    SUM(Returns[ReturnQuantity]),
    SUM(Sales[OrderQuantity]),
    0
) * 100

// Customer Lifetime Value
Customer LTV = 
DIVIDE([Total Revenue], [Total Customers], 0)
```

[See complete Model view →]([DAX_Measures/DAX_Code.txt](https://github.com/Dulani2411/PowerBI-Sales-Analytics-Dashboard/blob/main/Model%20view.png))

### Data Sources
- Sales transactions (2015-2017)
- Customer demographics
- Product catalog
- Returns data
- Territory information

---

## 📊 Dashboard Pages

### Page 1: Executive Dashboard
![Executive Dashboard]("https://github.com/Dulani2411/PowerBI-Sales-Analytics-Dashboard/blob/main/Screenshot%202025-12-10%20225408.png")

High-level overview with critical KPIs for C-suite decision makers.

### Page 2: Sales Performance Analysis
![Sales Performance]("[C:\Users\User\Pictures\Screenshots\powerbi\Screenshot 2025-12-10 225426.png](https://github.com/Dulani2411/PowerBI-Sales-Analytics-Dashboard/blob/main/Screenshot%202025-12-10%20225426.png)")

Deep dive into sales patterns, product performance, and profitability.

### Page 3: Customer & Returns Analysis
![Customer & Returns]("https://github.com/Dulani2411/PowerBI-Sales-Analytics-Dashboard/blob/main/Screenshot%202025-12-10%20225445.png
")

Customer segmentation, demographics, and quality control insights.

---

## 💡 Key Insights Discovered

### Revenue & Profitability
- 📈 Total revenue of **$24.9M** with steady growth trajectory
- 💰 Maintained consistent **42% profit margin** across all years
- 🎯 Average order value of **$990** indicates premium customer base

### Customer Analysis
- 👥 **18K** unique customers across 3 continents
- 🌍 North America drives **39%** of total revenue
- 📊 35-44 age group represents highest revenue segment

### Product Performance
- 🚴 Bikes dominate with **95%** of revenue ($23.6M)
- ⭐ Mountain-200 series are top performers
- 🎨 Black and Silver colors most popular

### Returns & Quality
- ✅ Excellent **2.17%** return rate (industry-leading)
- 💵 Revenue lost to returns: **$54K** (minimal impact)
- 🔍 Accessories have slightly higher return rate

---

## 🛠️ Tools & Technologies

| Category | Tools |
|----------|-------|
| **BI Platform** | Microsoft Power BI Desktop |
| **Data Analysis** | DAX (Data Analysis Expressions) |
| **Data Transformation** | Power Query (M Language) |
| **Data Modeling** | Star Schema Design |
| **Visualization** | Power BI Custom Visuals |
| **Version Control** | Git, GitHub |

---

## 📈 Skills Demonstrated

- ✅ Data Modeling (Star Schema)
- ✅ DAX (Measures, Calculated Columns, Time Intelligence)
- ✅ Power Query (ETL, Data Transformation)
- ✅ Data Visualization & UX Design
- ✅ Business Intelligence Strategy
- ✅ Analytical Thinking
- ✅ Storytelling with Data

---


## 📂 Repository Structure
```
PowerBI-Sales-Analytics-Dashboard/
│
├── README.md                          # Project documentation
│
├── Screenshots/                       # Dashboard images
│   ├── 01_Executive_Dashboard.png
│   ├── 02_Sales_Performance.png
│   └── 03_Customer_Returns.png
│
├── Data_Model/                        # Data architecture
│   └── Data_Model_Diagram.png
│
├── DAX_Measures/                      # DAX code
│   └── DAX_Code.txt
│
├── Sample_Data/                       # Sample datasets
│   ├── Products.csv
│   └── Customers_Sample.csv
│
└── Dashboard.pbix                     # Power BI file (optional)
```

---

## 📊 Sample Visualizations

### Revenue Trend
Steady growth from 2015 to 2017 with slight acceleration in 2016.

### Customer Segmentation
35-44 age group with Bachelor's degree represents highest-value segment.

### Geographic Distribution
North America leads with 39%, followed by Europe (31%) and Pacific (30%).

---

## 🎓 Learning Outcomes

Through this project, I developed proficiency in:

1. **Data Modeling:** Designed normalized star schema with proper relationships
2. **DAX:** Created complex measures using CALCULATE, SUMX, DIVIDE, etc.
3. **Power Query:** Transformed and cleaned data from multiple sources
4. **Visualization:** Selected appropriate chart types for different insights
5. **UX Design:** Created intuitive, user-friendly dashboard layout
6. **Business Analysis:** Translated data into actionable business insights

---

## 🔮 Future Enhancements

- [ ] Add predictive analytics (revenue forecasting)
- [ ] Implement RLS (Row-Level Security) for multi-user access
- [ ] Create mobile-optimized layouts
- [ ] Add drill-through pages for deeper analysis
- [ ] Integrate real-time data refresh
- [ ] Add bookmarks for saved views
- [ ] Implement what-if parameters
- [ ] Create PDF report generation

---

## 📞 Connect With Me

- 💼 **LinkedIn:** [(http://linkedin.com/in/dulani-ns)]
- 📧 **Email:** dulanins3@gmail.com
---

## 🙏 Acknowledgments

- Data source: [Mention if it's a publicly available dataset]
- Inspired by real-world business intelligence requirements
- Built as part of my data analytics learning journey

---

## ⭐ Show Your Support

If you found this project helpful or interesting, please consider:
- ⭐ **Starring this repository**
- 🔄 **Sharing with others**
- 💬 **Providing feedback via Issues**

---

**Last Updated:** December 2025

**Status:** ✅ Complete


