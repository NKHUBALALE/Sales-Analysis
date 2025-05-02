# AAL Sales Analysis - Q4 2020 (Applied Data Science with Python Final Project)

## Project Overview

**AAL (Australian Apparel Limited)**, established in 2000, is a recognized clothing brand in Australia. As the company experiences a surge in business and plans expansion, the **CEO has tasked the Sales & Marketing (S&M) department** to analyze sales performance across states. The objective is to identify high-revenue areas and support underperforming ones with targeted sales programs.

This project delivers a **data-driven analysis of AAL’s fourth-quarter sales (2020)** using applied data science techniques. The analysis spans from data wrangling to report generation — providing actionable insights for the upcoming year.

---

## Problem Statement

Analyze state-wise sales data of AAL from the fourth quarter of 2020, focusing on:

1. **Identifying states generating the highest revenue**
2. **Developing strategies for states with lower revenues**

---

## Dataset

- **File**: `AusApparalSales4thQrt2020.csv`
- **Contents**: Sales transaction records across states, time periods, and customer groups.

---

## Steps Performed

### 1. Data Wrangling

- **Missing Values**: Handled using `isna()` and `notna()` functions.
- **Data Treatment**: Null values were filled or dropped based on logical assumptions (e.g., sales/units of zero were considered invalid).
- **Normalization**: Applied Min-Max Normalization to scale numerical features between 0 and 1.
- **Grouping Strategy**:
  - `groupby()` was used to segment data by State, Group (Kids, Women, Men, Seniors), and Time.
  - Recommended for both **data chunking** (e.g., weekly/monthly analysis) and **aggregation** (e.g., total sales per state).

### 2. Data Analysis

- **Descriptive Statistics**:
  - Used `mean`, `median`, `mode`, and `std` to summarize Sales and Units columns.
- **Revenue Insights**:
  - Identified states and groups with highest and lowest revenue.
- **Time-based Reports**:
  - Created **weekly, monthly, and quarterly summaries** using `resample()` and date parsing in Pandas.

### 3. Data Visualization

#### Dashboard Highlights:
- **State-wise Sales by Group** (Kids, Women, Men, Seniors)
- **Group-wise Sales by State**
- **Peak vs Off-peak sales hours** to support marketing timing decisions

#### Tools Used:
- **Seaborn**: Preferred for statistical plotting (box plots, distribution plots)
- **Plotly**: Used for interactive dashboard visualizations
- **Matplotlib**: Supplementary plots

#### Key Visuals:
- Box plots for outlier detection
- Bar plots for categorical comparisons
- Line charts for time series analysis
- Heatmaps for peak sales analysis by hour and state

> Recommended tool: Seaborn for its integration with Pandas and rich statistical capabilities.

### 4. Report Generation

- **Platform**: JupyterLab
- **Features**:
  - Inline Markdown explanations
  - Combined code + plots + interpretation
  - Exported to PDF/HTML for business reporting

---

## Key Findings

- States **NSW** and **VIC** contributed the most to Q4 revenue.
- Groups with highest sales: **Women**, followed by **Men**.
- Off-peak states like **TAS** and **NT** need localized marketing programs.
- Peak sales occurred during **midday hours (11AM - 2PM)**.

---

## Recommendations

- Focus marketing investments in **underperforming states** such as NT and TAS.
- Launch **targeted promotions for Men and Seniors** in high-population states.
- Align advertising campaigns with **peak shopping hours**.
- Consider **inventory adjustments** based on group-wise demand per state.

---

## Tools & Technologies

- **Python Libraries**: Pandas, NumPy, Seaborn, Matplotlib, Plotly, SciPy
- **IDE**: JupyterLab
- **Version Control**: Git & GitHub

---


