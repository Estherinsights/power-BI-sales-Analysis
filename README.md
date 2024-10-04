# Supermarket sales Analysis
## Table of content
-[project overview](#project-overview)

-[Data source](#data-source)

-[Tools](#tools)

-[Data cleaning and preparation](#data-cleaning-and-preparation)

-[Exploratory data analysis](#exploratory-data-analysis)

-[Data Analysis](#data-analysis)

-[Visualization](#visualization)

-[Key insights](#key-insights)

-[Recommendations](#recommendations)

-[Conclusion](#conclusion)



### project overview
---

This Data analysis project aims on providing insights into the sales perfomance of a supermarket shop over the past two years .By analyzing various aspects of the sales data,i seek to identify patterns, make data driven recommendations and gain a deeper understanding of the supermarket's perfomance.

### Data source
---

from online kaggle

### Tools
---

power BI- for cleaning and analysis

### Data cleaning and preparation
---

i performed the following tasks to prepare the data for analysis
1. Data loading and inspection
2. Data cleaning and editting

### Exploratory data analysis
---
1.What are the total sales and profit?
How much revenue has been generated?
What is the overall profit percentage?

2.Which products are performing the best?
What are the top-selling products?
How much revenue do the top products generate?

3.What are the monthly and daily sales trends?
Are there any noticeable trends or patterns in sales over time?

4.What is the profit distribution across different product categories?
Which product categories are the most profitable?
Are there any categories with lower profit margins?

### Data Analysis
---
1. Add New Date Columns
   - Created new columns for Day, Year, Month, and Month Name from the existing date column in the input data.

2. Extract Month Abbreviation
   - Extracted the first three characters from the Month Name column to get the month abbreviation.

3. Match Product IDs
   - Matched the Product ID from the input data with the Product ID in the master data to perform a data lookup.

4. Clean Data
   - Removed the Product ID column after the match and retained the other relevant columns.
   - Closed and loaded the data for further transformations.

5. Add Total Buying and Selling Value Columns
- Added a new column Total Buying Value:
  
     Total Buying Value = InputData[Quantity] *(inputdata[MasterData.Buying Price])
     
   - Added another column Total Selling Value:
     
     Total Selling Value = InputData[Quantity] * MasterData[Selling Price] * (1 - InputData[Discount %])
     

6. Create Measures for Profit 
   - Created a new measure for Profit:
     
     Profit = SUM(InputData[Total Selling Value]) - SUM(InputData[Total Buying Value])
     
   - Created another measure for Profit Percentage:
     
     Profit Percentage = Profit / SUM(InputData[Total Buying Value])
     
The steps above allowed us to calculate the Total Buying Value, Total Selling Value, and generate insightful measures like Profit and Profit Percentage for further analysis of the sales data.
### Visualization
---
## Data Visualizations:

1. KPI Cards: 
   - Total Sales: 401K  
   - Total Profit: 69K  
   - Profit %: 21%

2. Bar Chart: Monthly performance of sales and profits (2021 vs. 2022).

3. Horizontal Bar Chart: Sales by product, with Product44 as the top product (23K).

4. Donut Chart:Sales breakdown by Sales Type(49% Direct Sales).

5. Line Chart:Daily sales trend.

6. Donut Chart:Payment method breakdown (Cash vs. Online).

7. KPI Cards:
   - Top Product:Product44 (23K)  
   - Top Category:Category04 (95K)
     
8. Treemap:Sales by category.
   
## Slicers:
1. Sale Type Slicer
2. Payment Mode Slicer
3. Day Slicer
4. Year Selection Slicer (2021, 2022)
   
### key insights
---

### **A. Sales and Profit Overview**
- **Total Sales:** 401K  
- **Total Profit:** 69K  
- **Profit Margin:** 21%

### **B. Monthly Sales Performance**
- Sales show a steady trend throughout the year, with a noticeable improvement in 2022 compared to 2021.
- There are fluctuations across months, with some performing significantly better in terms of profit.

### **C. Product Performance**
- **Top Product:** Product44 with 23K in sales.
- Product44 leads the sales chart, while Product39 shows the lowest performance.
- Significant gaps exist between product performances, with the top products capturing a large share.

### **D. Sales Type Breakdown**
- **Direct Sales:** 49% of total sales (112K).
- The majority of sales come from direct channels, with other channels making up 17%.

### **E. Payment Methods**
- **Cash Payments:** 23K (dominates overall payments).
- Online payment methods have lesser penetration, signaling room for growth.

### **F. Category Sales**
- **Top Category:** Category04 with 95K in total sales.
- Category04 and Category02 are high performers, while other categories lag behind.

### **G. Daily Sales Trends**
- Daily sales show an uneven pattern with some days significantly outperforming others.
- This suggests varying customer engagement on different days of the month.
  
![WhatsApp Image 2024-10-05 at 00 16 10_be68ff07](https://github.com/user-attachments/assets/fd6295b2-5548-4f63-a76b-3360154c353a)


## Recommendations

### **A. Increase Profit Margins**
- Focus on optimizing costs for low-performing products and high-cost categories to improve overall profit margins.
- Introduce strategies like bundling products or upselling higher-margin items.

### **B. Promote Online Payment Methods**
- Cash dominates payments; encouraging online payments could streamline operations and increase convenience.
- Offer incentives such as discounts or rewards for customers using digital payment options.

### **C. Focus on Low-Performing Products**
- Products such as Product39 and Product40 are underperforming. Target these with promotions, repositioning, or product analysis to identify potential improvements.
- Leverage customer feedback or market trends to optimize product offerings.

### **D. Address Slow Months**
- Sales performance varies across months, with some showing slower growth.
- Run seasonal promotions, discounts, or special campaigns during low-performing months to balance annual sales.

### **E. Diversify Sales Channels**
- Direct sales dominate, but expanding other channels like online stores or affiliate programs could provide new opportunities for growth.
- Analyze existing channels for improvement or expansion opportunities.

### Conclusion
This analysis highlights key areas of opportunity within the sales process, from increasing online payments to addressing product and category performance disparities. Implementing these recommendations can lead to improved sales, profit margins, and overall business efficiency.













