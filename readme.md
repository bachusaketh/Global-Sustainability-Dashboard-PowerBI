# Global Sustainability & Emissions Dashboard in Power BI

## 🎯 Project Objective

To develop an end-to-end business intelligence solution to analyze the correlation between CO₂ emissions and renewable energy adoption on a global scale. The goal was to visualize historical trends and forecast future emissions.

---

## 🛠️ Tools & Technologies

- **BI Tool:** Power BI Desktop
- **ETL:** Power Query Editor
- **Data Modeling:** Star Schema
- **Language:** DAX (Data Analysis Expressions)

---

## ⚙️ Project Walkthrough

### 1. Data Cleaning and Transformation (ETL)
The raw data from 'Our World in Data' required significant cleaning in Power Query Editor. Key steps included:
- Resolving data type errors in the main CO₂ column (converting from text to decimal).
- Replacing errors with null values and trimming whitespace to ensure data integrity.
- Merging the CO₂ and renewable energy datasets using a Left Outer Join on a composite key of `country` and `year`.

### 2. Data Modeling
A Star Schema model was implemented to improve performance and enable time intelligence calculations.
- A dedicated `Years` dimension table was created using DAX.
- A one-to-many relationship was established between the `Years` table and the main fact table.

### 3. DAX Measures
Several DAX measures were authored to calculate key performance indicators (KPIs):
- `Total CO2 Emissions`: Simple aggregation using `SUM`.
- `Renewable Energy %`: Correctly aggregated using `AVERAGE`.
- `YoY CO2 Change %`: A complex measure to calculate the percentage change in emissions compared to the previous year, providing deep insights into national performance.

### 4. Dashboard Design
The final interactive dashboard was designed to provide at-a-glance insights. It features:
- **KPI Cards:** For high-level summaries.
- **Combination Chart:** To visualize the core relationship between emissions and renewables over time.
- **Treemap:** To show top contributing nations.
- **Slicers:** For dynamic, user-driven filtering by country and year.
- **Forecasting:** To project future emission trends based on historical data.

---

## 📊 Final Dashboard

Here are some screenshots of the final report.

<img width="959" height="503" alt="Image" src="https://github.com/user-attachments/assets/a18b62a8-bcce-48bc-8286-08e265d84fb6" />
<img width="958" height="506" alt="Image" src="https://github.com/user-attachments/assets/4115d0a9-a430-428b-bb37-d0b5dd45002f" />
