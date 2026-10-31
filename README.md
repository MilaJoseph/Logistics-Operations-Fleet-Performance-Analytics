# Logistics Operations & Fleet Performance Analytics

## 📌 Project Overview

An interactive **Power BI Business Intelligence project** focused on analysing logistics operations and fleet performance using data from 2022–2024.

The project explores different aspects of logistics operations, including revenue, shipments, routes, customers, drivers, fuel purchases, delivery performance and vehicle maintenance.

The objective is to transform raw operational data into meaningful insights that can support business performance analysis and decision-making.

## 🎯 Project Objectives

- Analyse revenue and shipment trends.
- Compare route and customer performance.
- Monitor fuel and maintenance expenditure.
- Evaluate delivery performance and driver operations.
- Identify areas for further operational investigation.

## 📂 Dataset Overview

- **Source:** Kaggle – Logistics Operations Database (2022–2024).
- **Dataset Type:** Synthetic dataset representing a fictional trucking company.
- **Original Structure:** 14 interconnected tables.
- **Load Records:** 85,410.
- **Tables Selected:** 9 relevant tables.

The selected data covers:

- Loads and trips
- Customers and routes
- Drivers and trucks
- Fuel purchases
- Delivery events
- Maintenance records

*Note: The dataset is synthetic and does not represent an actual company's operations.*

## 🛠️ Tools & Technologies

- **Power BI Desktop** – Data modelling, DAX and report development.
- **Power Query** – Data cleaning and transformation.
- **DAX** – Measures and calculations.
- **Kaggle** – Dataset source.

## 🔄 Data Cleaning & Transformation

- Evaluated all 14 source tables and selected 9 relevant tables based on project objectives.
- Imported the selected CSV tables into Power BI.
- Reviewed column names, data types and table structures.
- Merged `Fact_Loads` and `Fact_Trips` using Power Query to create `Fact_Load_Trips`.
- Created a calculated `Dim_Date` table for time-based analysis.
- Checked missing values, duplicate records and data errors.
- Verified key columns and relationships.
- Preserved missing driver and truck IDs rather than assigning artificial values.

## 🏗️ Data Modelling

Designed a **Galaxy Schema (Fact Constellation Schema)** consisting of:

**4 Fact Tables**
- `Fact_Load_Trips` – Load, trip, revenue and distance details.
- `Fact_FuelPurchases` – Fuel transactions and expenditure.
- `delivery_events` – Delivery events and delivery status.
- `Fact_Maintenance` – Maintenance costs and downtime.

**5 Dimension Tables**
- `Dim_Date`
- `Dim_Customer`
- `Dim_Route`
- `Dim_Drivers`
- `Dim_Trucks`

Relationships were established using matching key columns, mainly one-to-many relationships with single-direction filtering for the main relationships.

## 📊 Key DAX Measures

- Total Revenue
- Total Loads
- Total Distance
- Revenue per Mile
- On-Time Delivery Rate
- Total Fuel Cost
- Total Maintenance Cost

Advanced DAX functions used:

`CALCULATE()` · `RANKX()` · `SELECTEDVALUE()` · `DIVIDE()` · `SUMX()` · `FILTER()` · `ALLSELECTED()`

## 📈 Power BI Report Pages

### 1. Executive Overview
- Overall revenue, loads, distance and delivery performance.
- Monthly revenue and load trends.
- Fuel and maintenance expenditure comparison.

### 2. Revenue, Routes & Customer Performance
- Highest and lowest revenue-generating routes.
- Dynamic Top/Bottom route analysis.
- Customer revenue contribution.
- Route-wise revenue and associated fuel purchase cost analysis.

### 3. Fleet, Drivers & Operations
- Driver revenue analysis.
- On-time and late delivery comparison.
- Late delivery investigation using a Decomposition Tree.
- Truck-wise maintenance cost analysis.

### 4. Route Details
- Route-specific performance analysis.
- Revenue, load count and distance.
- Monthly revenue trends using Drill-through.

## 💡 Key Business Insights

| KPI | Result |
|---|---:|
| Total Revenue | $262.53M |
| Total Loads | 85.41K |
| Total Distance | 122M miles |
| On-Time Delivery Rate | 44.61% |
| Fuel Cost as % of Revenue | 36.41% |
| Total Maintenance Cost | $5.73M |

- The overall on-time delivery rate was 44.61%, highlighting an opportunity to improve delivery reliability.
- Fuel purchases represented 94.34% of the combined fuel purchase and maintenance expenditure.
- Route and customer comparisons helped identify major revenue contributors.
- Driver and truck analysis provided additional visibility into operational performance.

*These findings are based on the synthetic dataset and its reporting filters.*

## 🎛️ Power BI Features

- Interactive Year and Load Type slicers.
- Bookmark-based filter panel.
- Dynamic Top/Bottom route ranking.
- Decomposition Tree.
- Drill-through analysis.
- Interactive charts and KPI cards.

## 📁 Project Files

- `PowerBI/` – Interactive Power BI report (.pbix).
- `Presentation/` – Project presentation (.pptx).
- `Dataset/` – Dataset source information.

## 👩‍💻 Author

**Mila Joseph**

B.Tech Computer Science & Engineering Graduate  
Aspiring Data Analyst | Power BI | SQL | Python | Excel

