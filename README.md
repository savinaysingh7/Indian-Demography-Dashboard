# 🇮🇳 Indian Demography Dashboard

> Converting 640+ districts of raw Census data into a one-click interactive Excel intelligence layer.

![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Data Analysis](https://img.shields.io/badge/Data_Analysis-Completed-0078D4?style=for-the-badge)
![Dataset](https://img.shields.io/badge/Dataset-Census_India_A--1-FF6B35?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Production_Ready-2ecc71?style=for-the-badge)
![Period](https://img.shields.io/badge/Period-Jan--Apr_2025-8e44ad?style=for-the-badge)

---

## 📋 Table of Contents

- [🌟 Overview](#-overview)
- [✨ Features](#-features)
- [📊 Key Findings](#-key-findings)
- [🛠️ Tech Stack](#️-tech-stack)
- [📁 Repository Structure](#-repository-structure)
- [⚡ Quick Start](#-quick-start)
- [🗂️ Data Pipeline](#️-data-pipeline)
- [📈 Dashboard Walkthrough](#-dashboard-walkthrough)
- [🔬 Methodology](#-methodology)
- [💡 Feature Engineering](#-feature-engineering)
- [🚀 How to Interact](#-how-to-interact)
- [📄 Report](#-report)
- [👤 Author](#-author)
- [🙏 Data Source](#-data-source)

---

## 🌟 Overview

The **Indian Demography Dashboard** is a fully interactive Excel-based analytics tool built on the **A-1 Census dataset** published by the Office of the Registrar General & Census Commissioner, India. It transforms hundreds of thousands of raw demographic rows — spanning villages, towns, households, population counts, and geographic area — into a single, filterable, visual intelligence dashboard.

Designed for policymakers, academic researchers, and data-curious audiences alike, this project demonstrates that you don't need a BI tool to build a production-grade analytical experience. By combining Excel's Pivot Tables, engineered features, and Slicer-driven interactivity, the dashboard makes India's demographic complexity accessible to any audience — without writing a single line of code.

**The problem it solves:** The raw Census A-1 file is a 36-state, 640+ district dataset with dozens of columns that is nearly impossible to interpret in flat form. This dashboard collapses that complexity into four interactive visual summaries that answer the most important demographic questions instantly.

---

## ✨ Features

- 🗺️ **State/UT-level aggregation** — Summarizes data across all 36 States and Union Territories using Pivot Tables, enabling seamless regional comparison
- ⚡ **Slicer-driven dynamic filtering** — One-click filtering by State/UT updates all charts simultaneously without manual formula edits
- 📊 **Urban vs. Rural population breakdown** — Side-by-side column charts contrasting urbanization levels across every Indian state
- 🏘️ **Village & Town count analysis** — Bar chart visualization of the administrative unit distribution (villages vs. towns) per state
- 🧮 **Engineered `Avg_HH_Size` metric** — A custom-calculated field (Total Population ÷ Households) surfacing regional household dynamics not present in the raw dataset
- 🔢 **Population density proxy** — Comparative analysis using population and area data to approximate regional density patterns
- 📐 **Sorted ranking views** — Pivot tables pre-sorted to instantly surface the highest and lowest values for any metric
- 📋 **Standalone formal report** — Companion `.docx` report covering the full data science lifecycle: problem statement → methodology → insights → conclusions
- ✅ **No-code reproducibility** — The entire pipeline from raw data to dashboard runs entirely in Microsoft Excel; zero dependencies, zero environment setup

---

## 📊 Key Findings

| Insight | Finding |
|--------|---------|
| **Urbanization variance** | Significant disparity exists between states with heavy town concentration vs. those dominated by rural villages |
| **Household size spread** | `Avg_HH_Size` reveals measurable cultural and regional differences in family sizes across India's states and UTs |
| **Data accessibility** | The dashboard reduced the cognitive overhead of interpreting the massive Census dataset by consolidating ~40 raw columns into 4 interactive visual summaries |
| **Administrative unit distribution** | Some smaller UTs have near-zero village counts, reflecting their fundamentally urban administrative structure |

---

## 🛠️ Tech Stack

| Category | Tool | Purpose |
|----------|------|---------|
| **Primary Platform** | Microsoft Excel (2016+ / Microsoft 365) | Data cleaning, transformation, analysis & dashboard |
| **Data Aggregation** | Excel Pivot Tables | State/UT-level metric aggregation and sorting |
| **Visualization** | Excel Pivot Charts (Bar + Column) | Urban/rural comparison, household and population charts |
| **Interactivity** | Excel Slicers | Dynamic cross-filtering of all dashboard views simultaneously |
| **Feature Engineering** | Excel Formulas (`=` division) | `Avg_HH_Size` calculated field creation |
| **Reporting** | Microsoft Word (.docx) | Formal project documentation |
| **Dataset Format** | `.xlsx` (Census of India) | Source data ingestion |

---

## 📁 Repository Structure

```
Indian-Demography-Dashboard/
│
├── 📊 A-1_NO_OF_VILLAGES_TOWNS_HOUSEHOLDS_POPULATION_AND_AREA.xlsx
│   └── Raw Census dataset — Office of the Registrar General & Census Commissioner, India
│       Columns: State/UT, District, Tehsil, Village/Town counts,
│                Households, Total/Male/Female Population, Area (sq.km)
│
├── 🔧 savinay-working-file.xlsx
│   └── Primary data processing workbook
│       ├── Sheet: Cleaned Dataset (standardized columns, anomalies removed, types corrected)
│       ├── Sheet: Feature Engineering (Avg_HH_Size = Population / Households)
│       └── Sheet: Base Pivot Tables (state-level aggregations, sorting applied)
│
├── 📈 analysis-summary.xlsx
│   └── Final interactive dashboard — THE PRIMARY DELIVERABLE
│       ├── Urban vs. Rural Population chart (column, slicer-connected)
│       ├── Village vs. Town count chart (bar, slicer-connected)
│       ├── Avg Household Size by State chart
│       ├── Population & Area summary metrics
│       └── State/UT Slicer panel (dynamic cross-filter control)
│
├── 📝 savinay-singh-report.docx
│   └── Formal project report
│       ├── Problem Statement
│       ├── Data Description & Source
│       ├── Methodology & Pipeline
│       ├── Analysis & Insights
│       └── Conclusions & Recommendations
│
└── 📄 README.md
    └── This file
```

---

## ⚡ Quick Start

### Prerequisites

```
Microsoft Excel 2016, 2019, 2021, or Microsoft 365
(Required for full Slicer and Pivot Chart interactivity)

Note: Google Sheets can open .xlsx files but does NOT support
Slicers or all Pivot Chart types — use Excel for the full experience.
```

### Clone and Open

```bash
# 1. Clone the repository
git clone https://github.com/savinaysingh7/Indian-Demography-Dashboard.git
cd Indian-Demography-Dashboard

# 2. Open the interactive dashboard
# → Double-click: analysis-summary.xlsx
# OR open the working/processing file:
# → Double-click: savinay-working-file.xlsx
```

### No Setup Required

> This project has **zero installation steps, zero dependencies, and zero environment variables.** If you have Excel, you have everything you need.

---

## 🗂️ Data Pipeline

```
Raw Census .xlsx
       │
       ▼
┌─────────────────────────────────┐
│  STAGE 1: Data Cleaning         │
│  • Standardize column headers   │
│  • Remove blank/extraneous rows │
│  • Correct data types           │
│  • Handle anomalies             │
└────────────────┬────────────────┘
                 │
                 ▼
┌─────────────────────────────────┐
│  STAGE 2: Feature Engineering   │
│  • Avg_HH_Size = Population /   │
│    Number of Households         │
│  (New derived column added)     │
└────────────────┬────────────────┘
                 │
                 ▼
┌─────────────────────────────────┐
│  STAGE 3: Pivot Table Creation  │
│  • Aggregate by State/UT        │
│  • Urban vs. Rural totals       │
│  • Village vs. Town counts      │
│  • Avg HH Size per region       │
│  • Sort by highest/lowest       │
└────────────────┬────────────────┘
                 │
                 ▼
┌─────────────────────────────────┐
│  STAGE 4: Dashboard Assembly    │
│  • Pivot Charts (bar + column)  │
│  • Slicer panel (State/UT)      │
│  • Layout & formatting polish   │
└─────────────────────────────────┘
```

---

## 📈 Dashboard Walkthrough

The `analysis-summary.xlsx` dashboard contains the following views, all connected to the central **State/UT Slicer**:

| View | Chart Type | X-Axis | Y-Axis / Metric |
|------|-----------|--------|----------------|
| Urban vs. Rural Population | Clustered Column | State/UT | Total Urban Population, Total Rural Population |
| Village vs. Town Distribution | Bar Chart | State/UT | Number of Villages, Number of Towns |
| Average Household Size | Column Chart | State/UT | Avg_HH_Size (engineered feature) |
| Summary KPIs | Card/Cell metrics | — | Total Population, Total Households, Total Area |

**Using the Slicer:** Click any State/UT button in the Slicer panel to instantly filter all charts to that region. Hold `Ctrl` and click to select multiple states for cross-regional comparison. Click the red `✕` to clear all filters and return to the all-India view.

---

## 🔬 Methodology

This project follows a complete data science workflow executed entirely within Microsoft Excel:

### 1. Data Collection
- Source: Official Census of India — A-1 dataset
- Publisher: Office of the Registrar General & Census Commissioner, India
- Granularity: State → District → Tehsil level

### 2. Data Cleaning
- Removed blank rows and extraneous header repetitions common in government-published `.xlsx` files
- Standardized column naming for unambiguous pivot field references
- Verified numeric columns (Population, Households, Area) were stored as numbers, not text strings
- Handled edge cases such as newly formed UTs with incomplete sub-district data

### 3. Feature Engineering
The most analytically significant transformation was the creation of **`Avg_HH_Size`**:

```excel
= [Total Population Column] / [Number of Households Column]
```

This single derived field reveals regional household composition patterns that are entirely invisible in the raw data — capturing the difference between, say, nuclear families in urbanized states vs. joint family structures in others.

### 4. Aggregation & Analysis
- Multiple Pivot Tables created, each aggregating a different metric by State/UT
- Sorting applied to surface both extremes (highest and lowest performing states)
- Urban/Rural split quantified to measure the urbanization gradient across India

### 5. Dashboard Creation
- All Pivot Tables converted to Pivot Charts with appropriate chart types
- Slicer connected to all charts simultaneously for synchronized filtering
- Dashboard layout formatted for readability and visual clarity

---

## 💡 Feature Engineering

| Feature | Formula | Insight Unlocked |
|---------|---------|-----------------|
| `Avg_HH_Size` | `Total Population / Number of Households` | Reveals nuclear vs. joint family distributions; cultural and economic proxy across regions |

This is the only engineered feature in the dataset — but its analytical value is disproportionate to its simplicity. States with higher `Avg_HH_Size` tend to correlate with lower urbanization, higher rural population proportions, and different socioeconomic profiles.

---

## 🚀 How to Interact

```
1. Open analysis-summary.xlsx in Microsoft Excel

2. Navigate to the Dashboard sheet (tab at the bottom)

3. Use the STATE/UT SLICER panel on the right side:
   • Single-click  → Filter all charts to one state
   • Ctrl + Click  → Select multiple states
   • Clear button  → Reset to all-India view

4. Hover over any chart bar/column to see exact values in tooltip

5. To explore raw data: switch to the Data or Pivot sheets in
   savinay-working-file.xlsx
```

---

## 📄 Report

The `savinay-singh-report.docx` is a formal academic project report covering:

- **Problem Statement** — Why Census data is analytically inaccessible in its raw form
- **Data Description** — Source, schema, and scope of the A-1 dataset
- **Methodology** — Step-by-step pipeline with justifications for each decision
- **Analysis & Findings** — Quantified insights with chart references
- **Conclusions** — Implications for policymakers and researchers
- **Appendix** — Data dictionary and cleaning log

---

## 👤 Author

**Savinay Singh**
B.Tech Computer Science & Engineering (Data Science Minor)
Lovely Professional University, Phagwara, Punjab — Batch 2023–27

[![LinkedIn](https://img.shields.io/badge/LinkedIn-savinaysingh-0077B5?style=flat&logo=linkedin)](https://linkedin.com/in/savinaysingh)
[![GitHub](https://img.shields.io/badge/GitHub-savinaysingh7-181717?style=flat&logo=github)](https://github.com/savinaysingh7)
[![Email](https://img.shields.io/badge/Email-savinay07singh@gmail.com-D14836?style=flat&logo=gmail)](mailto:savinay07singh@gmail.com)

> *This project was completed as a Data Science Minor Project at LPU between January and April 2025.*

---

## 🙏 Data Source

**Dataset:** A-1 Number of Villages, Towns, Households, Population and Area
**Publisher:** Office of the Registrar General & Census Commissioner, India
**Portal:** [censusindia.gov.in](https://censusindia.gov.in)

> The dataset is publicly available and published under the Government of India's open data initiative. This project is for educational and research purposes only.

---

<p align="center">
  <i>Built with Microsoft Excel · Census of India · Data Science Minor Project · LPU 2025</i>
</p>