## Adventure Works Dashboard

**Business Situation**

Adventure Works is a fictional cycling equipment and accesories manufacturing company.
Management needs a dasbboard to track KPIs (sales, revenue, profit, returns), compare regional performance, analyze product-level trends, and identify high-value customers.
We have a folder of raw csv files, contaning Transactions, Returns, Products, Customers, and Sales Territories.

**Data Analysis Objectives**
Deploy PowerBi to:
1. Connect and transform the raw data.
2. Build a relational data model.
3. Create calculated columns and measures with DAX.
4. Design an interactive dashboard to visualize the data.
   
**Skills & Concepts Demonstrated**
- Power Query: Loading and Cleaning, Profiling, Quality Assurance, Unpivoting data...
- DAX :Calculated Coumns, Measures (Implicit, Explicit), Rolling Calendar, Modelling- Snowflake Schema ( One to Many Cardinality, Hierarchies, Active and Inactive Relationships, Bi-directional filtering, Data Formats and Categories

 ## Executive Summary
![](Adventure_Works_Executive_Summary.png)

**Overall Performance**
1.  Business recorded Total Revenue of $24M from Jan 2020 to Jan 2022 and a Gross Profit of $10M Gross Profit, a healthy 41% Gross Margin.
2.  Return rate was 2.2% Return which is within benchmark target.
   
**Monthly Revenue Trend**
1.  Monthly revenue was trended around $600K from Jan 2020 but sharly declined to 300K in Nov 2020,
2.  Picking up from June 2021 at $560K, and surging to $800k in July 2021, and Phenomenal upward trend to $1.8M ever since and projected to hit max of $1.9M.
 
 ### Data Model  
1. The Adventure Works dataset is complex as it came with 2 fact tables- Sales Transactions and Returns fact tables and 6 Dimension Tables, 2 of which had 2 subcategory level.
2. Owing the its dual fact tables and the subrelationships in the dimensions tables to enable cross filtering between both fact tables, a Snowflake data model was built rather than a Star Schema model.
3. 43 explicit measures were built using DAX, rather implicit measures. Unlike implicit measures (by drag and drop and limited to one visual), explicit measures are DAX formula based and can be used anywhere in the model, hence more versatile and efficient.

![](PowerBi_Snow_flake_Data_Model.png2.png)


 ### Data Visualization
 Data Viz Best Practices including:
1. **Gestalt pricinples** were use to position data cards of Revenue, Profit and Return from Left to right and keep them together (Proximity)
2. **Bookmarks** capturing the current state of a page, so users can return to it in its initial state (ease of navigation)
3. **User Roles** (for the right level security access/restrictions)
4. **KPI Cards** to instantly visualize KPIs against targets.
5. **Drill Through, Drill Down and Custom Tooltips**: to intuively navigate from one report to the other.
6.**Top N Cards**:to highlights Top Customer and Top Product names.
7. **Field parameters**: to allow users to dynamically change the metrics or dimensions in the report visual
8. **Numeric Range parameters**: for simulation and Scenario analysis to assess for instance impact of different price points or discounts.

**Customer Dashboad** 
- highlightsTop Customer by Revenue, Number of Customers, Average Revenue by Customer and Orders by Income levels and Occupations Categories.
- Maurice Shan is No.1 Top Customer, presenting opportunity to potentially cross fertilize his business model to other customers for growth.
- Also, Number of customers increased to 17 thousand, revenue by customer is on decline, presenting opportunities to improve customer quality.

![](Adventure_Works_Customer_Details.png)

**Product Dashboard**
1.  Field parameters of Distinct orders, Revenue, Profit, Returns and Return Rate allow users to dynamically change the metrics or dimensions in the report visual for various insights
2.  Nunmeric Range parameters of enable scenario analysis of impact of prices changes in adjusted Profit vs total Profit.
3.  Gauge charts were also used to vizualize Monthly Targets for Orders, Revenue and Profit vs Actuals.
   
![](Adventure_Works_Product.png)

**Revenue Size by Georaphy Map**
1.  US tops Revenue contribution chart, followed by Australia, UK, Germany, France and Canada.
![](Adventure_Works_Maps.png)

