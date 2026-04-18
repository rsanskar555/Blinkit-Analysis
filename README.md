# 🛒 Blinkit Grocery Sales — Exploratory Data Analysis

> An exploratory data analysis (EDA) of Blinkit's grocery sales data using Python — uncovering patterns in customer preferences, product performance, and outlet efficiency through KPI computation and data visualization.

---

## 📑 Table of Contents

- [Overview](#-overview)
- [Tech Stack](#-tech-stack)
- [Dataset](#-dataset)
- [Data Cleaning](#-data-cleaning)
- [KPIs Computed](#-kpis-computed)
- [Charts & Visualizations](#-charts--visualizations)
- [Key Highlights](#-key-highlights)
- [Business Impact](#-business-impact)
- [Dashboard Preview](#-dashboard-preview)
- [Getting Started](#-getting-started)

---

## 📌 Overview

An exploratory data analysis (EDA) of Blinkit's grocery sales data using Python. The project analyzes sales performance across product types, outlet characteristics, and geographic tiers — uncovering patterns in customer preferences and outlet efficiency through KPI computation and data visualization.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|-----------|---------|
| ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) | Core analysis language |
| ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white) | Data loading, cleaning, and aggregation |
| ![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white) | Numerical computations |
| ![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat&logo=python&logoColor=white) | Custom chart plotting |
| ![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=flat&logo=python&logoColor=white) | Statistical visualizations |

---

## 📂 Dataset

**File:** `BlinkIT Grocery Data.csv`

**Key columns:**

| Column | Description |
|--------|-------------|
| `Item Fat Content` | Fat content label (Regular / Low Fat) |
| `Item Type` | Product category (e.g., Fruits, Snacks, Dairy) |
| `Sales` | Revenue generated per entry ($) |
| `Rating` | Customer rating for the item |
| `Outlet Size` | Size of the outlet (Small / Medium / Large) |
| `Outlet Location Type` | City tier (Tier 1 / Tier 2 / Tier 3) |
| `Outlet Establishment Year` | Year the outlet was established |

---

## 🧹 Data Cleaning

Standardized inconsistent label values in the `Item Fat Content` column before analysis:

| Raw Value | Cleaned Value |
|-----------|--------------|
| `LF` | `Low Fat` |
| `low fat` | `Low Fat` |
| `reg` | `Regular` |

```python
df['Item Fat Content'] = df['Item Fat Content'].replace({
    'LF': 'Low Fat',
    'low fat': 'Low Fat',
    'reg': 'Regular'
})
```

---

## 📊 KPIs Computed

| KPI | Description |
|-----|-------------|
| **Total Sales** | Sum of all sales (`$`) across the dataset |
| **Average Sales** | Mean sales value per entry |
| **No. of Items Sold** | Total count of sales transactions |
| **Average Rating** | Mean customer rating across all outlets |

---

## 📈 Charts & Visualizations

| Chart | Type | What It Shows |
|-------|------|---------------|
| Sales by Fat Content | Pie Chart | Revenue share between Regular vs. Low Fat items |
| Total Sales by Item Type | Bar Chart | Top-performing grocery categories ranked by revenue |
| Fat Content by Outlet Tier | Grouped Bar Chart | Low Fat vs. Regular sales split across Tier 1 / 2 / 3 cities |
| Sales by Outlet Establishment Year | Line Chart | Revenue trend correlated with outlet age/maturity |
| Sales by Outlet Size | Pie Chart | Revenue distribution across Small, Medium, and Large outlets |
| Sales by Outlet Location Type | Horizontal Bar Chart | City-tier wise total sales comparison |

---

## ✨ Key Highlights

- Conducted end-to-end EDA: raw CSV ingestion → data profiling (`shape`, `dtypes`, `unique()`) → cleaning → KPI computation → multi-chart visualization.
- Handled real-world data quality issues with targeted Pandas `replace()` operations before any aggregation.
- Added inline data labels on bar and line charts for immediate readability.
- Structured the notebook as a clean, reproducible analytical workflow — from exploration to insight delivery.

---

## 📈 Business Impact

- Pinpoints which **item types and fat content categories** drive the most revenue, directly informing procurement and shelf-space allocation decisions.
- Reveals how **outlet tier and size** correlate with sales, supporting data-driven expansion strategy and resource planning.
- The **establishment year trend** highlights an outlet maturity curve, helping operations teams benchmark performance of new vs. established stores.

---

## 📊 Dashboard Preview

![Dashboard](blinkit.png)

🔗 **[View Live Dashboard](https://app.powerbi.com/view?r=eyJrIjoiNWI3MThiZWItYzliMC00YTg5LTg0ZjAtMjgyMWZlZTE4MGIxIiwidCI6IjJmM2ViMmYzLTIwNjItNGRlOS04MmM5LTA3ZGIzZmFkMGJhNCJ9)**

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/blinkit-grocery-eda.git
cd blinkit-grocery-eda
```

### 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn
```

### 3. Run the Notebook

```bash
jupyter notebook
```

Open the EDA notebook and run all cells top to bottom.

---

## 👤 Author

Built as part of a hands-on data analytics learning journey, applying real-world business scenarios to develop skills in data cleaning, visualization, and insight delivery.

**Tools & Technologies across portfolio:** Excel · Power Query · DAX · Power BI · SQL (MySQL) · DAX Studio · Python · Pandas · NumPy · Matplotlib · Seaborn · GitHub LFS

---

## 📄 License

This project is open-source for educational and portfolio purposes.

---

<p align="center">
  <b>Python &nbsp;•&nbsp; Pandas &nbsp;•&nbsp; Matplotlib &nbsp;•&nbsp; Seaborn</b><br>
  <i>From raw grocery data to outlet performance insights</i>
</p>
