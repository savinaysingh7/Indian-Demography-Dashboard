# Dashboard Analysis of Indian Demography

![Data Analysis](https://img.shields.io/badge/Data%20Analysis-Excel-217346)
![Dashboard](https://img.shields.io/badge/Dashboard-Demographics-0078D4)
![Status](https://img.shields.io/badge/Status-Completed-success)

A comprehensive data analysis and visualization minor project focusing on the demographic landscape of India, based on the **A-1 Number of Villages, Towns, Households, Population and Area** dataset published by the Office of the Registrar General & Census Commissioner, India. This project was completed between January and April 2025.

## 🎯 Project Overview

This project aims to convert raw demographic datasets into an interactive, visually appealing Excel dashboard. The analysis highlights key trends related to urbanization, household sizes, and population density across various states and union territories in India. It empowers policymakers, researchers, and general audiences to quickly comprehend complex demographic data without needing deep technical expertise.

## 📂 Repository Contents

- **`A-1_NO_OF_VILLAGES_TOWNS_HOUSEHOLDS_POPULATION_AND_AREA.xlsx`**: The raw Census dataset used as the foundation for the project.
- **`savinay-working-file.xlsx`**: The primary data processing file. It contains the cleaned dataset, intermediate calculations, and the base pivot tables used for the dashboard.
- **`analysis-summary.xlsx`**: The final interactive Excel Dashboard featuring custom visualizations, slicers, and aggregated demographic metrics.
- **`savinay-singh-report.docx`**: A detailed, formal project report documenting the entire data science lifecycle—from problem statement and methodology to final insights and conclusions.

## 🔬 Methodology

The project followed a structured data analysis pipeline entirely within Microsoft Excel:

1. **Data Collection & Cleaning**:
   - Imported the raw dataset (Excel `.xlsx`).
   - Standardized column names and removed extraneous/blank rows.
   - Handled anomalies and verified data types (e.g., ensuring numeric fields were correctly formatted).

2. **Data Transformation & Feature Engineering**:
   - Created a new calculated field: **`Avg_HH_Size`** (Average Household Size) by dividing the Total Population by the Number of Households utilizing Excel formulas.

3. **Data Analysis & Visualization (Pivot Tables)**:
   - Generated multiple Pivot Tables to aggregate data by State/Union Territory.
   - Created key metrics such as Total Urban Population vs. Rural Population and Average Household Sizes per region.
   - Applied sorting to identify states with the highest and lowest metrics.

4. **Dashboard Creation**:
   - Developed an interactive dashboard utilizing Pivot Charts (Bar charts, Column charts).
   - Integrated **Slicers** to allow dynamic filtering of the dashboard by metrics such as State/UT, making the tool highly interactive.

## 💡 Key Insights

- **Urbanization Variance**: The analysis revealed significant disparities in urbanization; some states showed heavy concentration in towns compared to rural villages.
- **Household Dynamics**: The generated `Avg_HH_Size` feature highlighted cultural and regional differences in average family sizes across the country.
- **Data Accessibility**: The final dashboard successfully reduced the cognitive load required to interpret the massive census dataset, converting rows of numbers into actionable visual intelligence.

## 🚀 How to Use

1. **Clone the project:**
   ```bash
   git clone https://github.com/savinaysingh7/Indian-Demography-Dashboard.git
   ```
2. **Open the Dashboard:** Open `analysis-summary.xlsx` (or `savinay-working-file.xlsx`) in **Microsoft Excel**. Note: Some interactive features like Slicers may require a modern version of Excel (Microsoft 365, Excel 2016+).
3. **Interact:** Use the provided Slicers on the dashboard sheet to filter the demographic data by specific regions or states dynamically.

---
*Developed by Savinay Singh as a Data Science Minor Project.*