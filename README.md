# AdventureWorks-Sales-Analysis

## Project Name
**AdventureWorks Sales Analysis**

## Project Idea
An end-to-end analysis of the AdventureWorks **Internet Sales** data, from raw data cleaning to interactive dashboards. The goal is to turn transactional sales data into clear business insights about revenue, profitability, products, customers, regions, and seasonality, so decision-makers can track performance and spot growth opportunities.

The project follows a full analytics pipeline:

1. **Python**: clean and prepare the raw data.
2. **SQL Server**: build a star-schema database and run analysis queries.
3. **Power BI**: build the main dashboard on top of the SQL database.
4. **Excel**: build a sales overview workbook.
5. **Tableau**: build a year-over-year and seasonality view.

## Team Members
| # | Name | Tool |
|---|------|------|
| 1 | Ahmed Ahmed Saber Fayed | Power BI + Tableau |
| 2 | Amir Aly Mohammed Eid | Power BI |
| 3 | Engy Botros Telmeez Zekri | Power BI + SQL |
| 4 | Mahmoud Abu Elhamd Mohamed Ismail | Power BI + Excel |
| 5 | Mourine Emad Sobhy Wahba | Power BI + Python |

## Work Plan
1. **Data Cleaning (Python):** Load the raw AdventureWorks workbook, drop unneeded and sensitive columns (email, phone, address, postal code, language-specific names), build `FullName`, standardize column names, split `SizeRange` into bicycle and clothes sizes, and map codes (e.g. `M`/`S`, `M`/`F`) to readable labels. Export a clean Excel file.
2. **Database Creation (SQL Server):** Create the `AdventureWorks_Final` database with a star schema (1 fact table and 5 dimensions), primary and foreign keys, load the cleaned data, and create the views `vw_products` and `vw_sales_details`.
3. **Analysis Queries (SQL):** Calculate KPIs and analyze sales by year, month, country and region, product, color, customer segments, and shipping speed.
4. **Power BI Dashboard:** Import the data directly from SQL Server, build the data model and DAX measures, and design the dashboard pages.
5. **Excel Workbook:** Build the sales overview workbook.
6. **Tableau Dashboard:** Build the year-over-year (YoY) and seasonality page.

## Roles & Responsibilities
| Member | Responsibility |
|--------|----------------|
| Mourine Emad Sobhy Wahba | **Python**: data cleaning and preparation (`AdventureWorks.ipynb`) |
| Engy Botros Telmeez Zekri | **SQL**: database design, data loading, views, and analysis queries |
| Mahmoud Abu Elhamd Mohamed Ismail | **Excel**: sales overview workbook |
| Ahmed Ahmed Saber Fayed | **Tableau**: YoY and seasonality dashboard |
| Amir Aly Mohammed Eid | **Power BI**: dashboard development |
| **All members** | Participated in the **Power BI** dashboard in addition to their own tool |

## KPIs
Definitions used throughout the project:

- **Revenue** = `OrderQuantity × UnitPrice`
- **Cost** = `OrderQuantity × ProductCost`
- **Profit** = Revenue − Cost

| KPI | Description |
|-----|-------------|
| Total Revenue | Sum of sales revenue |
| Total Cost | Sum of product costs |
| Total Profit | Revenue minus cost |
| Profit Margin % | Profit ÷ Revenue |
| Total Orders | Distinct sales orders |
| Active Customers | Distinct customers who purchased |
| Average Order Value | Revenue ÷ number of orders |
| YoY Revenue Growth % | Year-over-year change in revenue (2005 and 2008 are partial years, so a Jan–Jul like-for-like comparison is also provided) |
| Average Days to Ship | Days between order date and ship date |

Additional breakdowns: monthly seasonality, country/region, top and bottom products, product color, top customers, gender and marital status, occupation and education, income bands, and customers by first-purchase year.

## Instructor
**Eng. Adham Osama Mohammed**

## Project Files
| File | Description |
|------|-------------|
| [Uploading AdventureWorks.ipynb…]() | Data cleaning notebook (Python / pandas) 
| [01_Build_Database.sql](https://github.com/user-attachments/files/35433331/01_Build_Database.sql) | Creates the database, tables, views, and loads the data 
| [Uploading 02_Analysis_Queries.sql…]() | Analytical SQL queries for the KPIs and breakdowns |
| https://drive.google.com/file/d/1LFaxoWtZtVxC8cHWwy5-6oYVhdvW8GVQ/view?usp=drive_link | Power BI dashboard (data imported from SQL Server) |
| https://drive.google.com/file/d/1wQBn3asJYyimvVK7cVcH3z4osla5ifBO/view?usp=drive_link | Tableau workbook: YoY and seasonality |
| [AdventureWorks Sales Overview.xlsx](https://github.com/user-attachments/files/35433655/AdventureWorks.Sales.Overview.xlsx) | Excel sales overview workbook |
| [AdventureWorks Sales Analysis.pdf](https://github.com/user-attachments/files/35434164/AdventureWorks.Sales.Analysis.pdf) | Final Presentation |

### Repository Structure
```
AdventureWorks-Sales-Analysis/
├── README.md
├── data/
│   └── AdventureWorks_Sales_Overview.xlsx
├── python/
│   └── AdventureWorks.ipynb
├── sql/
│   ├── 01_Build_Database.sql
│   └── 02_Analysis_Queries.sql
├── powerbi/
│   └── Final_project.pbix
└── tableau/
    └── Page11_YoY_Seasonality.twbx
```

### How to Reproduce
1. Run `python/AdventureWorks.ipynb` on the raw `AdventureWorks.xlsx` to produce `AdventureWorks_Clean.xlsx`.
2. Import the clean sheets into SQL Server, then run `sql/01_Build_Database.sql`.
3. Run `sql/02_Analysis_Queries.sql` to reproduce the analysis.
4. Open `Final_project.pbix` in Power BI Desktop and point the data source to your SQL Server instance.
5. Open `Page11_YoY_Seasonality.twbx` in Tableau.

## Tools
Python (pandas), SQL Server, Power BI, Excel, Tableau
