# Amazon-Product-Review-Analysis  
---  

Unravelling price patterns of different variables across numerous Amazon products in 9 major categories using Excel, to help generate insights that can guide groduct improvement and marketing strategies, and drive customer engagement.

# 📖 Project Overview
 
This project was completed as part of the **DSA Data Analysis Capstone Projects**, following the bootcamp by **Incubator hub**. Here, i took the role of a Junior Data Analyst in a company that provides e-commerce analytics solutions to Amazon sellers. I explored product pricing, discount strategies, product ratings, and reviewed the behaviour of customers across multiple product categories to identify patterns that drive business profits.
The final deliverable is an interactive **Excel Dashboard** built from cleaned data, calculated columns and pivot table outputs.

The **Core business question** i aimed to answer was:
> *Which product categories and pricing strategies drive the highest customer engagement, and where do opportunities exist to improve ratings and revenue?*
---

## 🛠️ Tools & Features used

| Tool | Purpose |
|------|---------|
| Microsoft Excel | Data cleaning, calculated columns, pivot tables, pivot charts |
| Power Query | Data transformation and editing |
| Excel Dashboard | Final interactive visualization and report |
---

## 📂 Dataset    

**The dataset used, titled *Amazon case study.xlsx* was provided by **DSA & the Incubator hub**, as part of the requirements for my data analysis course completion with them. You can find this dataset in this repository as well.**
---

## 🔍 Methodology
 
### Step 1: Data Cleaning
*I Created a copy of dataset intitially, to use as the working area*
- Removed duplicate product entries
- Standardized price columns (removed currency symbols, converted to numeric)
- Handled blank and inconsistent values in rating and review columns, using information from *product name* and *category class2* columns
- Split *product category* column using comma-separated delimiter
- Deleted two unnecessary columns (img link, product link) for easier visibility
- Transformed data in power query

### Step 2: Calculated Columns Created
| Column | Formula Logic | Excel Formula |
|--------|---------------|---------------|
| Potential Revenue | `Actual Price × Rating Count` | `=PRODUCT([@[actual_price]],[@[rating_count]])`
| Price Range Bucket | `<₹200`, `₹200–₹500`, `>₹500` | `=IF(H19<200,"₹200",IF(OR(H19=200,H19=500),"₹200-₹500",">₹500"))`
| Number of products that have a discount of 50% and above | `1 if Discount % ≥ 50, else 0` | `COUNTIF(Amazon_copy!K:K, ">=0.5") = 751`
 
### Step 3: Pivot Table Analysis
- Built pivot tables to answer all 14 analysis questions across categories, ratings, pricing tiers, and review volumes.
- Created pivot charts using column charts, pie charts, line charts, and area charts to visualize key trends
 
### Step 4: Dashboard Creation
- Dashboard: Designed a one-page interactive summary for management insights featuring a KPI summary card, category comparison charts, rating distribution visuals by category, and an interactive slicer for filtering by product categoryand rating ranges.
---

## 🔎 Key Analysis Questions
 
This project answers the following business questions for Amazon:
 
1. What is the average discount percentage by product category?
2. How many products are listed under each category?
3. What is the total number of reviews per category?
4. Which products have the highest average ratings?
5. What is the average actual price vs. discounted price by category?
6. Which products have the highest number of reviews?
7. How many products have a discount of 50% or more?
8. What is the distribution of product ratings (3.0, 4.0, etc.)?
9. What is the total potential revenue by category?
10. How many unique products fall into each price range bucket?
11. How does rating relate to the level of discount offered?
12. How many products have fewer than 1,000 reviews?
13. Which categories have products with the highest discounts?
14. Who are the top 5 products by combined rating and review count?
---
 
## 💡 Key Findings & Insights 
 
- 🏷️ **Highest Discounts**: The *Computers&Accessories* category offered the steepest average discounts at **94%**, suggesting aggressive pricing to increase volume of sales.
- ⭐ **Top Rated**: Products in the *Office Products* category had the highest average ratings, indicating strong customer satisfaction. And a total of 1111 products across all categories were rated >4.
- 📝 **Most Reviewed**: USBCables are the products with the highest number of reviews at a count of 233 out of 1463 in total, making it the product with the highest engangement in the dataset. The highest reviewed category was *Electronics*.
- 💰 **Revenue Potential**: *Electronics* generated the highest potential revenue at **98,020,806,974**, and  *Toys&Games* had the least potential revenue at **2,380,050**. This was driven largely by price points, discount percentage, number of products in each categories, and large review volumes.
- 🔖 **Discount Threshold**: while a total of **751** products have a discount percentage of 50% or more. Also, products with the highest ratings appeared to have the highest discount rate as compared to products with the lowest ratings.
---

## 📊 Dashboard Preview

<img width="538" height="387" alt="Amazon sales2" src="https://github.com/user-attachments/assets/0dd21004-da68-4b7f-ae54-2f88761908d5" />
---

## 📬 Contact
 
**Uchechukwu Esther Okwudili**
📧 ucokwudili27@gmail.com
💼 www.linkedin.com/in/uchechukwu-okwudili-a7437933a
🌐 [Portfolio / GitHub Profile URL]
 
---


