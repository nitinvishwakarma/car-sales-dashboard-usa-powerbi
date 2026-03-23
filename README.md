# Car Sales Dashboard – USA | Power BI & Star Schema

## Project Overview
This project involved developing a comprehensive Power BI solution for automotive sales performance tracking, analyzing a portfolio of **$371.2M in total sales** with a focus on inventory trends and year-over-year growth.

## Key Technical Features
* **Dimensional Modelling:** Built a **Star Schema** data model with multi-table relationships across Car, Dealer, Customer, and Date tables.
* **Advanced Calculations:** Implemented YTD ($371.2M), MTD ($5.43M), and **23.59% YOY growth** DAX measures.
* **Report Interactivity:** Designed **drillthrough reports** linking executive summaries to granular transaction detail pages (Car ID, Dealer, Model).
* **Advanced Visuals:** Created a geographic dealer region bubble map and a company-wise sales trend matrix using %GT calculated measures.

---

## Data Model — Star Schema
```
dim_Car ────────┐
dim_Dealer ─────┤
dim_Customer ───┼──── fact_Sales
dim_Date ───────┘
```

---

## Features Built

- Star schema model with Car, Dealer, Customer, Date tables
- YTD, MTD, and YOY DAX time intelligence measures
- Drillthrough reports for dealer-level analysis
- Cascading filters across brand, region, and time
- Dealer region map visual across USA
- Percentage of grand total matrix across 20+ brands

---

## DAX Measures Used
```dax
-- Year to Date Sales
YTD Sales = TOTALYTD(SUM(Sales[Amount]), Calendar[Date])

-- Month to Date Sales
MTD Sales = TOTALMTD(SUM(Sales[Amount]), Calendar[Date])

-- Year over Year Growth
YOY Growth % = 
DIVIDE(
    [YTD Sales] - [PYTD Sales],
    [PYTD Sales]
) * 100

-- % of Grand Total
% GT = DIVIDE([Total Sales], CALCULATE([Total Sales], ALL(Cars)))
```

---

### Dashboard Overview
![Dashboard Overview](Screenshot(1)-Car%20Sales%20Dashboard%20Overview.jpg)

### Dashboard Details
![Dashboard Details](Screenshot(1)-Car%20Sales%20Dashboard%20Details.jpg)

---

## Live Report

> Power BI Service embedding is restricted on this account.
> Full dashboard screenshots are available below and in this repository.

---

## Tools Used
* Power BI Desktop
* DAX (Time Intelligence & Star Schema relationships)
* Power Query for data transformation

---

# Car Sales Dashboard — USA
### Tools: Power BI | DAX | Star Schema

---
  
## Files in This Repository

| File | Description |
|---|---|
| car_sales_dashboard.pbix | Power BI dashboard file |



# Car Sales Dashboard – USA | Power BI & Star Schema

## Project Overview
This project involved developing a comprehensive Power BI solution 
for automotive sales performance tracking, analyzing a portfolio of 
**$371.2M in total sales** with a focus on inventory trends and 
year-over-year growth.

---

## Key Technical Features

- **Dimensional Modelling:** Built a Star Schema data model with 
multi-table relationships across Car, Dealer, Customer, and Date tables
- **Advanced Calculations:** Implemented YTD ($371.2M), MTD ($5.43M), 
and **23.59% YOY growth** DAX measures
- **Report Interactivity:** Designed drillthrough reports linking 
executive summaries to granular transaction detail pages
- **Advanced Visuals:** Created a geographic dealer region bubble map 
and a company-wise sales trend matrix using %GT calculated measures

---

## Data Model — Star Schema
```
dim_Car ────────┐
dim_Dealer ─────┤
dim_Customer ───┼──── fact_Sales
dim_Date ───────┘
```

---

## DAX Measures Used
```dax
-- Year to Date Sales
YTD Sales = TOTALYTD(SUM(Sales[Amount]), Calendar[Date])

-- Month to Date Sales
MTD Sales = TOTALMTD(SUM(Sales[Amount]), Calendar[Date])

-- Year over Year Growth
YOY Growth % = 
DIVIDE(
    [YTD Sales] - [PYTD Sales],
    [PYTD Sales]
) * 100

-- % of Grand Total
% GT = DIVIDE([Total Sales], CALCULATE([Total Sales], ALL(Cars)))
```

---

## Screenshots

### Dashboard Overview
![Dashboard Overview](Screenshot(1)-Car%20Sales%20Dashboard%20Overview.jpg)

### Dashboard Details
![Dashboard Details](Screenshot(1)-Car%20Sales%20Dashboard%20Details.jpg)

---

## Live Report

> Power BI Service embedding is restricted on this account.
> Full dashboard screenshots are available in this repository.

---

## Tools Used

- Power BI Desktop
- DAX — Time Intelligence and Star Schema relationships
- Power Query for data transformation

---

## Files in This Repository

| File | Description |
|---|---|
| Car_sales_dashboard.pbix | Power BI dashboard file |
| Car Sales.xlsx | Raw car sales dataset |
| Problem Statement.docx | Project requirements and problem statement |
| Screenshot(1)-Car Sales Dashboard Overview.jpg | Overview page screenshot |
| Screenshot(1)-Car Sales Dashboard Details.jpg | Details page screenshot |

---

*Project by Nitin Vishwakarma | Power BI Developer | March 2026*
| dataset.csv | Raw car sales dataset |
| screenshots/ | Dashboard screenshots |

---

*Project by Nitin | Power BI Developer*
