📊 Online Retail Data Quality Assessment & Data Cleansing
Project Overview
This project focuses on assessing and improving data quality in an online retail transaction dataset. The project identifies common data quality issues such as missing values, duplicate records, inconsistent categorical values, and format inconsistencies.
The objective of this project is to transform raw transactional data into a cleaner, more reliable dataset that can be used for further analysis and business decision-making.
The project follows a structured data quality workflow:
1. Data Profiling
2. Data Quality Assessment
3. Data Cleansing
4. Data Validation
5. Before vs After Quality Evaluation
Business Problem
In real-world business environments, transactional data often contains quality issues caused by manual input errors, inconsistent data entry formats, incomplete customer information, or duplicated records.
Poor data quality can lead to:
- Incorrect sales analysis
- Duplicate transaction calculations
- Inaccurate customer segmentation
- Misleading business insights
Therefore, a systematic data quality assessment process is required before performing further analytics.
Dataset Description
Dataset Information
| Attribute | Description |
| Dataset Type | Online Retail Transaction Data |
| Total Records | 350 rows |
| Total Attributes | 17 columns |
| Data Type | Structured CSV Dataset |
| Data Condition | Raw dataset containing quality issues |
Dataset Attributes
| Column | Description |
| order_id | Unique transaction identifier |
| order_date | Transaction date |
| customer_id | Customer identifier |
| customer_name | Customer name |
| email | Customer email |
| phone | Customer phone number |
| city | Customer city |
| province | Customer province |
| product_category | Product category |
| product_name | Product name |
| quantity | Purchased quantity |
| unit_price_idr | Product price |
| discount_pct | Discount percentage |
| payment_method | Payment method |
| order_status | Transaction status |
| shipping_days | Delivery duration |
| total_amount_idr | Total transaction amount |
Project Workflow
1. Data Profiling
The first stage analyzes the condition of raw data before any modification.
The following assessments were performed:
Missing Value Analysis
Objective:
Identify incomplete records and determine appropriate handling strategies.
Findings:
- Total missing values before cleansing: 87
- Missing values were found in:
  - email
  - phone
  - quantity
  - price
  - discount
  - shipping information
  - customer information
Duplicate Data Analysis
Objective:
Identify duplicated transaction records.
Finding:
| Metric | Result |
| Total Records | 350 |
| Duplicate Records | 15 |
Unique Value Analysis
Objective:
Identify inconsistent categorical values caused by different capitalization, spelling, or terminology.
Examples:
Before: Fashion, fashion, FASHION
After: Fashion
Analyzed attributes:
- Product Category
- Payment Method
- Order Status
- Province
Format Inconsistency Analysis
The analysis identified inconsistencies in:
- Date formats
- Email formatting
- Phone number formatting
- Currency formatting
- Percentage formatting
2. Data Cleansing Process
Duplicate Removal
| Metric | Before | After |
| Records |350|335|
| Duplicate Records|15|0|
All identical duplicate transactions were removed.
Missing Value Handling
The handling strategy was based on column characteristics.
Filled with "Tidak diketahui"
Applied to:
- city
- province
- payment_method
- customer_name
- product_name
Retained as Missing
Applied to:
- email
- phone
- quantity
- unit_price_idr
- discount_pct
- shipping_days
- invalid order_date
Reason:
Missing values were preserved when no reliable replacement value existed.
This approach prevents artificial data creation.
Category Standardization
Standardization techniques:
- Remove unnecessary spaces
- Convert capitalization format
- Map equivalent categories
Format Standardization
Applied transformations:
- Date
- Price
- Phone Number
3. Data Quality Improvement Result
Overall Comparison
| Metric | Before Cleansing | After Cleansing |
| Total Record |350|335|
| Total Column|17|17|
| Duplicate Record|15|0|
| Missing Value|87|66|
| Product Category Unique Value|28|12|
| Payment Method Unique Value|16|9|
| Order Status Unique Value|20|10|
| Province Unique Value|21|12|
Tools & Technologies
| Tool | Purpose |
| Python | Data processing |
| Google Colab | Development environment |
| Pandas | Data manipulation |
| Matplotlib | Visualization |
| CSV | Dataset format |
Conclusion
This project demonstrates a complete data quality assessment and cleansing workflow on online retail transaction data.
Through profiling and cleansing processes, the dataset quality improved by:
- Removing duplicate transactions
- Reducing inconsistent categorical values
- Standardizing data formats
- Handling missing values based on business logic
The final cleaned dataset is more reliable and ready for further analysis such as sales performance analysis, customer segmentation, and business intelligence reporting.
Future Improvement
Future development can include:
- Automated data quality monitoring pipeline
- Data validation rules before data entry
- Dashboard development using Power BI/Tableau
- Machine learning readiness assessment
Author
Tria Yunita
Data Analyst Portfolio Project