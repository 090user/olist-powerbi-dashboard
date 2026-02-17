**Olist Sales Analytics Dashboard — Power BI + MySQL**

**Project Overview**
This project is an end-to-end Sales Analytics dashboard built using the Olist e-commerce dataset. The goal was to design a business-ready BI solution starting from raw data to a secure, published Power BI report with row-level security.

The workflow covers database understanding, SQL view creation, dimensional data modeling, DAX measure development, and secure report publishing in Microsoft Fabric.

**Data Source**
Dataset: Olist E-commerce Dataset
Source: Kaggle
Storage: Imported into local MySQL RDBMS
Approach: Database-first understanding before visualization

**End-to-End Workflow**
Step 1 — Data Understanding
Downloaded dataset from Kaggle
Imported raw tables into local MySQL database
Reviewed schema, keys, and table relationships
Identified fact and dimension candidates

**Step 2 — SQL Layer (View Creation)**
Created SQL views to prepare analytics-ready datasets:
Joined required tables
Cleaned fields
Standardized columns
Derived calculated fields
Reduced unnecessary attributes
These SQL views were used as the source layer for Power BI instead of raw tables.

**Step 3 — Power BI Connection**
Connected Power BI Desktop to MySQL views
Imported only required columns
Applied data type corrections
Performed additional transformations in Power Query where required

**Step 4 — Data Modeling**
Designed a dimensional model inside Power BI:
Built star schema
Central sales fact table
Dimension tables:
Customer
Product
Date
State
Created a dedicated Date table
Managed relationships and filter directions
Created helper tables where required
Model design screenshot included in /screenshots.

**Step 5 — Helper & Analytical Tables**
Created additional analytical tables in Power BI:
Customer order summary table
Order bucket segmentation
Repeat customer flag
Delivery metrics calculations
Used for customer behavior and operational analysis.

**Step 6 — DAX Measures**
Developed business measures using DAX, including:
Total Revenue
Total Orders
Total Customers
Average Order Value
Time-based revenue trends
Category performance measures
Delivery performance metrics
DAX measure list included in project docs.

**Step 7 — Row Level Security (Dynamic RLS)**
Implemented dynamic Row Level Security:
Built a User–State mapping table (Email → Customer State)
Created dynamic RLS rule based on logged-in user
Applied state-level data restriction
Tested roles locally in Power BI Desktop

**Step 8 — Publishing & Service Testing**
Published report to Microsoft Fabric
Configured RLS roles in service
Tested with user-based access
Verified dynamic filtering behavior

**Dashboard Pages**
The report contains four analytical sections:
Executive Sales Overview
KPI cards
Revenue trends
Geographic distribution
Category revenue ranking
Customer Analysis
Customer segmentation
Repeat vs new customers
State-level distribution
Product & Category Performance
Top categories
Product contribution
Revenue ranking
Delivery & Operations
Delivery time metrics
Operational performance indicators

**Screenshots**
See /screenshots folder for:
Dashboard pages
Data model (star schema)
DAX measures
Published Fabric report

**Data Model**
Star schema design
Central fact table with multiple dimensions
Separate Date table
Helper analytical tables
RLS mapping table
Model view screenshot included.

**Tools & Technologies**
MySQL
SQL (Views, joins, derived fields)
Power BI Desktop
Power Query
DAX
Microsoft Fabric (Service)
Row Level Security (Dynamic)

**How to Use**
Download the PBIX ZIP file from this repository
Extract the file
Open in Power BI Desktop
Refresh data (if database connection available)

**Key Skills Demonstrated**
SQL data preparation
Dimensional modeling
Star schema design
DAX measure development
Analytical dashboard design
Row Level Security (dynamic)
Power BI Service deployment
End-to-end BI workflow
