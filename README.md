# Adventure Works – Global Sales Dashboard (Excel + Power Query + VLOOKUP)

## 📌 Project Overview
This project analyzes global sales data for **Adventure Works Cycles** using **Microsoft Excel** with **Power Query** for data transformation and **VLOOKUP** for dimension enrichment.  
The dashboard provides a clear snapshot of key business metrics, sales trends, and top performers.

### 📈 Key Metrics
| KPI | Value |
|-----|-------|
| **Total Sales** | **$29.4M** |
| **Total Profit** | **$12.1M** |
| **Total Orders** | **60.4K** |
| **Profit Margin** | **41%** |

## 🎯 Business Problem
Adventure Works had raw sales data scattered across multiple files. Management needed:
- A unified view of global sales across regions.
- A centralized dashboard to track revenue, profit, and returns.
- Visual insights on seasonal trends and top performers.

## 🛠️ Tools Used
| Tool | Purpose |
|------|---------|
| **Excel (Power Query)** | Data cleaning, combining files, date extraction, custom columns (Cost & Profit) |
| **Excel (VLOOKUP)** | Fetching Product Names and Customer Full Names from dimension tables |
| **Excel (PivotTables / Charts)** | Data modeling and dashboard visualization |
| **Excel (Slicers)** | Interactive filtering |

## 🔄 Data Transformation Pipeline

**Step 1: Connect & Combine Data (Power Query)**
- Connected to raw sales files (`factinternetsales` and `factinternetsalesnew`).
- Used **Append Queries** to combine both tables into a single master dataset.

**Step 2: Enrich with Dimensions (VLOOKUP)**
- Used **VLOOKUP** to fetch `EnglishProductName` from `dimproduct` using `ProductKey`.
- Used **VLOOKUP** to fetch `CustomerFullName` (First + Middle + Last) from `dimcustomer` using `CustomerKey`.

**Step 3: Create Date Dimensions (Power Query)**
- Converted `OrderDateKey` to proper date format using Power Query.
- Extracted **Year** and **Month** using Power Query's date functions.

**Step 4: Calculate Cost & Profit (Power Query - Custom Columns)**
- Added custom columns in Power Query:
  - `ProductionCost = ProductionStandardCost × OrderQuantity`
  - `Profit = SalesAmount - ProductionStandardCost`

**Step 5: Load & Build Dashboard**
- Loaded cleaned data into Excel Data Model.
- Created **PivotTables** and **PivotCharts** for all visualizations.
- Designed a static dashboard with **Slicers** for filtering by Region, Year, and Product.

## 📊 Dashboard Features

### 1. Overall KPIs (Top Section)
- **Total Sales:** $29.4M
- **Total Profit:** $12.1M
- **Total Orders:** 60.4K
- **Profit Margin:** 41%

### 2. Sales by Quarter (Donut Chart)
| Quarter | % of Total Sales |
|---------|------------------|
| Q1 | 25% |
| Q2 | 26% |
| Q3 | 26% |
| Q4 | 25% |

> Sales are evenly distributed across all quarters.

### 3. Sales by Month (Bar Chart)
| Month | Revenue |
|-------|---------|
| January | 1.87M |
| February | 1.74M |
| March | 1.91M |
| April | 1.95M |
| May | 2.21M |
| June | 2.94M |
| July | 2.41M |
| August | 2.69M |
| September | 2.54M |
| October | 2.92M |
| November | 2.98M |
| **December** | **3.21M (Peak)** |

> **December is the highest peak month at 3.21M** — strong holiday season performance. Sales show a clear upward trend from June onwards.

### 4. Sales by Country (Bar Chart)
- United States
- Australia
- Canada
- France
- Germany
- North America
- South America
- United Kingdom

### 5. Top 10 Products
| Product Name |
|--------------|
| Road-250 Black, 52 |
| Road-250 Red, 58 |
| Road-250 Red, 42 |
| Road-250 Red, 48 |
| Road-250 Red, 46 |
| Road-150 Red series |

> **Road-250 Black, 52** is the top-selling product.

### 6. Top 10 Customers
| Customer Name | Sales |
|---------------|-------|
| Nichole Nara | 13.3K |
| Kaitlyn Henderson | – |
| Margaret He | – |
| Randall M Dominguez | – |
| Adriana Gonzalez | – |
| Rosa H Hu | – |
| Brandi D Ogi | – |
| Brad She | – |
| Francisco A Sara | – |
| Maurice M Shan | 12.91K |

> **Nichole Nara** is the highest-spending customer at **13.3K**.

### 7. Sales by Year (Bar Chart)
| Year | Revenue |
|------|---------|
| 2010 | ~0.04M |
| 2011 | ~7.08M |
| 2012 | ~5.84M |
| **2013** | **~16.35M** |
| 2014 | ~0.05M (Partial Data) |

> **Massive 180% growth from 2012 to 2013!**

### 8. Region (Slicer Filter)
- Australia
- Canada
- Central
- France
- Germany
- North America
- South America
- United Kingdom

## 📌 Key Insights & Recommendations

| Insight | Recommendation |
|---------|----------------|
| **December is the peak month at 3.21M** | Stock up on popular items before December. Run holiday campaigns in Nov–Dec. |
| **Sales grow steadily from June to December** | Plan promotions to sustain momentum through the second half of the year. |
| **Road-250 Black, 52** is the top product | Ensure sufficient stock, feature in marketing. |
| **Nichole Nara** is the top customer (13.3K) | Offer loyalty rewards to retain. |
| **180% growth from 2012 to 2013** | Investigate what drove this success and replicate. |
| **Sales are evenly distributed by quarter** | Maintain consistent marketing year-round. |

## 📁 Repository Structure
Adventure-Works-Sales-Dashboard/
├── README.md
├── screenshots/
│ └── Adventure_Works_Dashboard.png
└── Adventure_Works_Dashboard.xlsx

## 📊 Dashboard Preview
![Adventure Works Sales Dashboard]((https://github.com/PratikshaBhosale8997/Adventure_works_analysis_excel_project/blob/main/Snapshot_of_Adventure_works_sales_dashboard_Excel.png))


## 👩‍💻 Author
**Pratiksha Subhash Bhosale**  

## 📧 Contact
pratikshabhosale1501@gmail.com
- 💼 LinkedIn: [linkedin.com/in/profile](https://www.linkedin.com/in/pratiksha-bhosale-6b433837b/)



---
⭐ If you find this useful, give it a star!
