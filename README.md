# 📊 Customer Shopping Behavior Analysis – Data Analytics Project

**Status:** ✅ Completed  
**Date:** 2026  
**Author:** [parasdelhi1-prog](https://github.com/parasdelhi1-prog)  
**Dataset:** 3,900 customer transactions  
**Tools Used:** Excel, Python, SQL, Power BI  

---

## 🎯 Project Overview

I completed an end-to-end **Data Analytics Project** analyzing customer shopping behavior across 3,900 transactions in multiple product categories. The objective was to uncover customer spending patterns, product preferences, and subscription behavior to generate insights that guide strategic business decisions.

This is a **comprehensive analytics workflow** demonstrating proficiency in Python, SQL, and Power BI.

---

## 📊 Key Business Insights

### 1. **Customer Revenue Comparison**
- Male vs. Female spending patterns analyzed
- Identified high-value customer segments
- *Insight:* Revenue distribution shows opportunities for targeted marketing

### 2. **Premium Customer Behavior**
- High-spending customers who still use discounts identified
- Discount sensitivity varies by customer segment
- *Insight:* Premium customers may need exclusive benefits instead of discounts

### 3. **Product Preferences**
- Top-rated products across categories identified
- Shipping preference analysis (express vs. standard)
- *Insight:* Product quality and logistics impact customer satisfaction

### 4. **Customer Lifecycle Segmentation**
- **New Customers:** First-time buyers (onboarding opportunities)
- **Returning Customers:** Repeat buyers (loyalty programs)
- **Loyal Customers:** High-frequency purchasers (retention focus)
- *Insight:* Different segments need different engagement strategies

### 5. **Demographics & Spending**
- Revenue contribution by age group
- Subscription impact on purchase behavior
- *Insight:* Subscription model drives predictable revenue and higher lifetime value

### 6. **Discount Dependency**
- Products most dependent on discounts identified
- Repeat buyer patterns analyzed
- *Insight:* Some products need pricing strategy review; others show strong organic demand

---

## 🛠️ Technologies & Skills Demonstrated

### **Python (Pandas)**
- Exploratory Data Analysis (EDA)
- Data cleaning and standardization
- Feature engineering (age_group, purchase_frequency_days)
- Missing value handling
- Data quality assessment

### **SQL (PostgreSQL)**
- Revenue analysis and comparison queries
- Customer segmentation logic
- Aggregation and grouping
- Business metrics calculation
- Complex JOIN operations

### **Power BI**
- Interactive dashboard design
- Multi-dimensional analysis
- Drill-down capabilities
- KPI visualization
- Stakeholder-friendly reporting

### **Data Skills**
✅ Data Preparation & Cleaning  
✅ Feature Engineering  
✅ Exploratory Data Analysis (EDA)  
✅ SQL-based Business Analysis  
✅ Data Visualization  
✅ Customer Segmentation  
✅ Business Intelligence  

---

## 📁 Project Structure & Files

```
Customer-Shopping-Behavior-Analysis/
├── README.md                                 # This file
├── data/
│   └── customer_shopping_data.csv            # 3,900 transaction records
├── notebooks/
│   ├── 01_Data_Exploration.ipynb             # EDA with Pandas
│   └── 02_Data_Cleaning.ipynb                # Data prep & feature engineering
├── sql_queries/
│   ├── 01_Revenue_Analysis.sql               # Male vs Female spending
│   ├── 02_Customer_Segmentation.sql          # Customer lifecycle segmentation
│   ├── 03_Product_Analysis.sql               # Top products & ratings
│   └── 04_Subscription_Analysis.sql          # Subscription impact analysis
├── dashboards/
│   ├── Customer_Shopping_Dashboard.pbix      # Power BI interactive dashboard
│   └── dashboard_screenshots/
│       ├── overview.png
│       ├── customer_segmentation.png
│       ├── spending_patterns.png
│       └── product_analysis.png
├── reports/
│   ├── Project_Summary.md                    # High-level overview
│   ├── Executive_Summary.md                  # Business insights
│   └── Methodology.md                        # Technical approach
└── docs/
    └── Feature_Engineering_Details.md        # Feature creation documentation
```

---

## 🔍 Data Workflow

### **Phase 1: Data Preparation (Python)**

**Tasks:**
- Explored dataset structure (3,900 rows, multiple columns)
- Generated summary statistics
- Identified and handled missing values in review ratings
- Standardized column names for consistency
- Engineered features: `age_group`, `purchase_frequency_days`
- Removed redundant columns
- Validated data quality

**Output:** Clean, analysis-ready dataset

### **Phase 2: Data Analysis (SQL)**

**Key Analyses:**
1. **Revenue Comparison**
   ```sql
   SELECT Gender, SUM(Purchase_Amount) as Total_Revenue
   FROM customers
   GROUP BY Gender
   ```

2. **Customer Segmentation**
   ```sql
   SELECT 
     Customer_ID,
     CASE 
       WHEN Purchase_Count = 1 THEN 'New'
       WHEN Purchase_Count BETWEEN 2 AND 5 THEN 'Returning'
       ELSE 'Loyal'
     END as Customer_Type
   FROM customer_summary
   ```

3. **High-Value Premium Customers**
   ```sql
   SELECT Customer_ID, Total_Spent, Discount_Usage
   FROM customers
   WHERE Total_Spent > [threshold] AND Discount_Used = 'Yes'
   ```

4. **Product Performance**
   ```sql
   SELECT Product_Category, AVG(Rating) as Avg_Rating, COUNT(*) as Sales
   FROM transactions
   GROUP BY Product_Category
   ORDER BY Avg_Rating DESC
   ```

5. **Subscription Impact**
   ```sql
   SELECT Subscription_Status, AVG(Purchase_Frequency) as Avg_Frequency
   FROM customers
   GROUP BY Subscription_Status
   ```

### **Phase 3: Visualization (Power BI)**

**Dashboard Features:**
- **Customer Overview:** Total customers, segments, lifetime value
- **Revenue Analysis:** By gender, age group, subscription status
- **Customer Segmentation:** New vs. Returning vs. Loyal breakdown
- **Product Performance:** Top products, ratings, category analysis
- **Spending Patterns:** Trends, seasonality, purchase frequency
- **Subscription Impact:** ROI, retention metrics
- **Discount Analysis:** Dependency products, pricing recommendations

---

## 📈 Key Findings Summary

| Metric | Finding | Business Impact |
|--------|---------|-----------------|
| **Gender Revenue Split** | Analyzed spending by gender | Targeted marketing opportunities |
| **Premium + Discount Users** | Identified high-value price-sensitive segment | Review discount strategy |
| **Top Products** | Best-rated items across categories | Stock and promote winners |
| **Customer Lifecycle** | 3 segments (New/Returning/Loyal) | Segment-specific strategies |
| **Subscription Value** | Higher purchase frequency with subscription | Expand subscription offerings |
| **Discount Dependency** | Some products overly reliant on discounts | Pricing review needed |
| **Shipping Preferences** | Express vs. Standard analysis | Optimize logistics strategy |
| **Age Demographics** | Revenue by age group | Age-targeted campaigns |

---

## 🚀 How to Use This Project

### **For Recruiters & Hiring Managers:**
1. Read this README for project overview
2. Check `dashboards/dashboard_screenshots/` for visuals
3. Review Jupyter notebooks for Python skills
4. Review SQL queries for database expertise
5. View Power BI dashboard for visualization capabilities

### **For Learning/Replication:**
1. Start with `notebooks/01_Data_Exploration.ipynb`
2. Follow `notebooks/02_Data_Cleaning.ipynb`
3. Run SQL queries against your own data
4. Explore Power BI dashboard structure

### **For Business Use:**
1. Import dataset into your PostgreSQL database
2. Run SQL queries to generate insights
3. Open Power BI dashboard
4. Filter and drill-down by customer segment, time period, etc.

---

## 💡 Key Skills Demonstrated

### **Python & Data Science**
- ✅ Data cleaning and preprocessing
- ✅ Feature engineering (creating new variables)
- ✅ Exploratory data analysis (EDA)
- ✅ Handling missing values
- ✅ Working with Pandas DataFrames

### **SQL & Databases**
- ✅ Complex SELECT queries
- ✅ GROUP BY aggregations
- ✅ CASE statements for segmentation
- ✅ JOIN operations
- ✅ Window functions (if used)

### **Business Intelligence**
- ✅ Dashboard design and layout
- ✅ Multi-dimensional analysis
- ✅ KPI tracking
- ✅ Interactive filters and slicers
- ✅ Data storytelling

### **Analytics & Problem-Solving**
- ✅ Customer behavior analysis
- ✅ Segmentation strategy
- ✅ Revenue analysis
- ✅ Trend identification
- ✅ Actionable recommendations

---

## 📊 Business Value

### **For Marketing Teams:**
- Understand customer segments for targeted campaigns
- Identify high-value customers for retention
- Analyze product preferences by demographic

### **For Sales Teams:**
- Identify premium customer behavior
- Understand discount sensitivity
- Focus on high-margin products

### **For Product Teams:**
- Discover top-performing products and categories
- Understand customer preferences
- Identify products needing strategy review

### **For Finance:**
- Revenue analysis by segment
- Subscription revenue impact
- Discount ROI analysis

---

## 🎓 Project Learning Outcomes

This end-to-end project strengthened expertise in:

✔ **Data Cleaning and Preparation** – Making raw data analysis-ready  
✔ **Exploratory Data Analysis (EDA)** – Finding patterns and insights  
✔ **SQL-based Business Analysis** – Answering complex business questions  
✔ **Data Visualization with Power BI** – Communicating insights visually  
✔ **Complete Analytics Workflows** – From raw data to actionable recommendations  
✔ **Feature Engineering** – Creating meaningful variables for analysis  
✔ **Customer Segmentation** – Dividing customers into actionable groups  
✔ **Business Acumen** – Translating data into strategy  

---

## 📈 Impact & Results

- Analyzed **3,900 customer transactions** across multiple categories
- Identified **3 distinct customer segments** with different behaviors
- Discovered **top-performing products** and underperformers
- Quantified **subscription model ROI**
- Provided **9+ actionable business recommendations**
- Created **self-serve dashboard** for stakeholder decision-making

---

## 🔗 Connect With Me

- **GitHub:** [parasdelhi1-prog](https://github.com/parasdelhi1-prog)
- **LinkedIn:** [linkedin.com/in/paras-rewariya-34b62426a]

---

## 📄 License

This project is shared for educational and demonstration purposes.

---

## 📞 Questions?

Explore the notebooks, SQL queries, and Power BI dashboard. Feedback and questions are welcome!

---

**Last Updated:** March 2026

---

*This project demonstrates how data analytics transforms customer transaction data into strategic business insights, enabling smarter, data-driven decision-making.*
