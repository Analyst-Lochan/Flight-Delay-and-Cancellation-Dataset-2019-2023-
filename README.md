# Flight Delay & Cancellation Dashboard (Power BI Portfolio Project)

This project demonstrates a complete data analytics pipeline starting from raw real-world flight data to professional visual dashboards using SQL Server and Power BI. It showcases data import, cleaning, optimization, transformation, and dynamic DAX-based visual reporting.

---

## Dataset Source

- **Title:** Flight Delay and Cancellation Dataset (2019–2023)
- **Source:** https://www.kaggle.com/datasets/patrickzel/flight-delay-and-cancellation-dataset-2019-2023
- **Size:** 6+ million rows

---

## Tools Used

- **SQL Server 2022** – For data import, cleaning, transformation
- **Power BI Desktop** – For data visualization and dashboard creation
- **DAX (Data Analysis Expressions)** – For creating measures and calculated columns
- **Windows 10 Pro** – Local development environment

---

## Project Steps

### 1. Data Acquisition

- Downloaded the CSV dataset from Kaggle.
- The dataset includes millions of flight records from 2019 to 2023.

### 2. Data Import into SQL Server

- Created database and raw tables using SQL Server Management Studio (SSMS).
- Used `BULK INSERT` to load data from CSV files.
- Due to Power BI performance limitations on my system, extracted a clean 100,000 row sample into a new table: `Flights_1Lakh`.

### 3. Data Cleaning in SQL

- Removed rows where important columns like `FL_DATE`, `AIRLINE`, `FL_NUMBER`, `ORIGIN`, `DEST`, `DEP_DELAY` are null.
- Converted and standardized time formats (e.g., extracting hours from `DEP_TIME`).
- Removed unwanted characters (e.g., double quotes) from text columns.
- Used `CAST`, `TRY_CAST` to handle type mismatches.
- Dropped columns with too many nulls or less relevance.
- Removed duplicate records using composite keys.

### 4. Power BI Integration

- Connected Power BI to SQL Server.
- Imported `Flights_1Lakh` table.
- Created calculated columns and DAX measures.
- Built visuals including bar charts, KPIs, and slicers.

---

## Power BI Visualizations

### DAX Measures

- Total Flights
- Cancelled Flights
- Average Departure Delay
- Average Arrival Delay
- On-Time Departure Percentage

### Calculated Columns

- Departure Hour (extracted from `DEP_TIME`)

### Visuals Created

- Bar chart: Flights by Hour of Day
- Line chart: Average Delay by Airline
- Pie chart: Cancellations by Airline
- Table: Route performance
- KPI Cards: Total Flights, Average Delays, % On-Time, Cancellations

---

## Files Included

- `view.pbix` – Power BI project file
- `view.pdf` – Dashboard exported as PDF
- `SQLQuery1.sql` – Complete SQL data cleaning script
- `link.txt` – Kaggle dataset URL

---

## Portfolio Summary

Developed a complete data analysis pipeline using a real-world flight dataset. Cleaned over 6 million records in SQL Server and prepared a 100K row sample for Power BI. Built a fully interactive dashboard with DAX measures and data modeling, covering performance metrics, airline delays, and time-based trends.

---

## How to Use This Project

1. Clone or download this repository.
2. Open `view.pbix` in Power BI Desktop.
3. Review `SQLQuery1.sql` to understand SQL cleaning steps.
4. Connect to your own SQL Server database if you want to recreate from scratch.
5. Use `view.pdf` to preview the dashboard without opening Power BI.

---

## Future Improvements

- Add Power BI Gateway for scheduled refresh
- Create geospatial maps for airport-to-airport routes
- Add airline metadata for more filter options

---

## Contact

For feedback or collaboration:

- **Lochan Singhal**
- **www.github.com/Analyst-Lochan**

---

"Clean data fuels clean insights."  
This project highlights my ability to perform end-to-end data analysis using SQL Server and Power BI.
