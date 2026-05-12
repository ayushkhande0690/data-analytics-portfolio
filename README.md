<div align="center">

# Hi, I'm Ayush Khande 👋
### Data Analyst . Turning Raw Data into Business Decisions

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ayushkhande0690)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](ayushkhande66@gmail.com)

![Profile views](https://komarev.com/ghpvc/?username=your-username&color=1D9E75&style=flat-square)

</div>

---

## About Me

I'm a data analyst based in **Amravati, India**, passionate about building end-to-end analytics systems that help businesses make smarter decisions. My work spans the full analytics pipeline — from raw data generation and SQL querying to interactive dashboards and automated reporting.

- 🔭 Currently building a **Retail Chain Intelligence Platform** combining Python, SQL, Power BI, and Excel
- 🌱 Learning **advanced DAX**, **machine learning for analytics**, and **cloud data warehousing**
- 💬 Ask me about **RFM customer segmentation**, **financial modelling**, or **sports analytics**
- 🎯 Goal: Land a data analyst role where I can solve real business problems at scale
- ⚡ Fun fact: I built a win probability model for IPL matches using logistic regression on ball-by-ball data

---

## Portfolio Projects

> Five projects built from scratch — no tutorial copies, no Kaggle rehashes. Each one solves a real business problem with a full implementation.

| # | Project | Tools | Domain | Dataset Scale | Status |
|---|---------|-------|--------|--------------|--------|
| 1 | [🧮 Dynamic P&L Financial Model](#1--dynamic-pl-financial-model) | ![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoftexcel&logoColor=white) ![VBA](https://img.shields.io/badge/VBA-217346?style=flat&logo=microsoftexcel&logoColor=white) | Finance | 3-year model, 3 BUs | ✅ Complete |
| 2 | [🛒 E-commerce RFM Engine](#2--e-commerce-rfm-engine) | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white) | E-commerce | 50,000+ orders | ✅ Complete |
| 3 | [🏏 IPL Match Analytics](#3--ipl-match-analytics) | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white) | Sports | 15,000 deliveries | ✅ Complete |
| 4 | [👥 HR Attrition Dashboard](#4--hr-attrition-dashboard) | ![PowerBI](https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black) | HR Analytics | 1,470 employees | ✅ Complete |
| 5 | [🏪 Retail Intelligence Platform](#5--retail-intelligence-platform-capstone) | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white) ![PowerBI](https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black) ![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoftexcel&logoColor=white) | Retail | 100,000 transactions | ✅ Complete |

---

## Project Deep Dives

### 1 · Dynamic P&L Financial Model

![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoftexcel&logoColor=white)
![VBA](https://img.shields.io/badge/VBA-217346?style=flat&logo=microsoftexcel&logoColor=white)

**Business problem:** A retail group's finance team needed to model three strategic scenarios (Base / Bull / Bear) across three business units for FY2022–2024, with a one-click PDF report every board meeting.

**What I built:**
- Assumptions Control Panel with named ranges — the only cells anyone needs to touch
- Fully dynamic 3-year P&L (Revenue → COGS → Gross Profit → EBITDA → Net Profit) driven entirely by the Assumptions sheet
- Scenario switcher using `INDEX/MATCH` on a single dropdown — changing one cell updates the entire model instantly
- 2-variable sensitivity analysis table (revenue growth × COGS %) colour-coded as a heatmap — 36 EBITDA outcomes at a glance
- VBA macro: cycles through scenarios, updates chart titles, exports the Dashboard as a date-stamped PDF

**Key Excel concepts demonstrated:**
`INDEX/MATCH` · `Named Ranges` · `INDIRECT` · `Data Tables (What-If Analysis)` · `Scenario Manager` · `Conditional Formatting — Color Scales` · `VBA Workbook Events` · `Dynamic Chart Titles`

📁 [`project-1-excel-pl-model/`](./project-1-excel-pl-model)

---

### 2 · E-commerce Customer Intelligence Platform (RFM Engine)

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Python](https://img.shields.io/badge/Python_(data_gen)-3776AB?style=flat&logo=python&logoColor=white)

**Business problem:** An Indian e-commerce platform couldn't identify which customers were worth retaining vs which had already churned — and was spending marketing budget equally on all segments.

**What I built:**
- 6-table normalised PostgreSQL schema: `customers`, `orders`, `order_items`, `products`, `categories`, `returns`
- Python Faker script generating 2,000 customers and 50,000+ orders with realistic Indian festive season spikes (Oct–Dec 30% higher volume)
- 10 business intelligence queries covering revenue trends, product affinity, return rates, and acquisition channel analysis — all using CTEs, window functions, `LAG`, `LEAD`, `NTILE`, and `PERCENT_RANK`
- **RFM scoring model:** every customer scored 1–5 on Recency, Frequency, and Monetary value using `NTILE(5)` → labelled into 5 segments (Champions / Loyal / Promising / At Risk / Lost)
- **Cohort retention matrix:** tracks what % of each monthly acquisition cohort returned to purchase in months M1–M12
- 3 reusable `CREATE VIEW` statements consumed by downstream Power BI and Excel reports

**Key SQL concepts demonstrated:**
`CTEs` · `Window Functions (RANK, DENSE_RANK, NTILE, LAG, LEAD)` · `Self-joins` · `CASE WHEN` · `Date arithmetic` · `Correlated subqueries` · `CREATE VIEW` · `Bulk INSERT via psycopg2`

📁 [`project-2-sql-rfm-engine/`](./project-2-sql-rfm-engine)

---

### 3 · IPL Match Analytics & Player Intelligence System

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=flat&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)

**Business problem:** Cricket analysts need to evaluate player performance by match situation — not just career averages. A batsman averaging 135 SR in the powerplay means nothing if they collapse in death overs.

**What I built:**
- Synthetic ball-by-ball dataset: 15,000 deliveries across 200 IPL matches, generated with NumPy using realistic distributions — higher boundary rates in powerplay, aggression spike in death overs, wicket patterns by innings phase
- Feature engineering: `match_phase` (Powerplay/Middle/Death), cumulative runs and wickets, current and required run rates, dot ball streaks
- Phase-wise batting analysis: strike rate and boundary % by phase for top 15 batsmen (min 50 balls filter)
- Death-over bowling analysis: economy rate, wicket rate, and dot ball % for death overs specialists (min 20 overs)
- **Win probability model:** logistic regression trained on 2nd innings match state (runs needed, balls remaining, wickets fallen, CRR, RRR, phase) — **84.2% accuracy** on the test set — with per-over probability output plotted for sample chases
- 6 publication-quality visualisations saved as PNG: heatmap (SR by batsman × phase), grouped bar (team scoring by phase), scatter (economy vs wicket rate), win probability line, death-over bar, first innings box plot by venue

**Key Python concepts demonstrated:**
`pandas groupby/merge/pivot_table` · `numpy random seeding` · `seaborn heatmap` · `scikit-learn LogisticRegression` · `train_test_split + confusion_matrix` · `matplotlib subplot layouts` · `modular script architecture`

📁 [`project-3-python-ipl-analytics/`](./project-3-python-ipl-analytics)

---

### 4 · HR Workforce & Attrition Intelligence Dashboard

![PowerBI](https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-F2C811?style=flat&logo=powerbi&logoColor=black)

**Business problem:** A company's HR leadership knew attrition was high but couldn't pinpoint which departments, salary bands, or employee profiles were most at risk — or quantify the cost.

**What I built:**
- Dataset: IBM HR Analytics (1,470 employees, 35 variables) — a real public benchmark dataset used by HR teams globally
- Power Query transformations: `Age_Group` bins, `Tenure_Bucket`, `Salary_Band` by income percentile, binary attrition flag, and `Flight_Risk_Score` (composite of overtime, environment satisfaction reversed, job satisfaction reversed — scored 1–10)
- 6 DAX measures: `Attrition Rate`, `Avg Monthly Income by Dept`, `High Flight Risk Count`, `Gender Pay Gap %`, `Avg Tenure`, `Attrition Cost Estimate` (6 months salary per exit)
- **3-page interactive report:**
  - Page 1 — Executive Summary: attrition KPIs, department comparison, salary band breakdown
  - Page 2 — Department Deep Dive: satisfaction heatmap, tenure vs attrition scatter, income distribution by role
  - Page 3 — Individual Risk Profiler: high flight risk employee table, overtime correlation, top attrition predictors ranked
- Advanced UX: drill-through (click department → goes to Page 2 filtered), bookmarks (toggle between Attrition View and Salary View), custom tooltips showing avg salary + tenure on hover

**Key Power BI concepts demonstrated:**
`Power Query M transformations` · `DAX CALCULATE + FILTER` · `DIVIDE for safe division` · `Drill-through pages` · `Bookmarks + selection pane` · `Custom tooltip pages` · `Data model relationships` · `Conditional formatting by measure`

📁 [`project-4-powerbi-hr-dashboard/`](./project-4-powerbi-hr-dashboard)

---

### 5 · Retail Chain Intelligence Platform *(Capstone)*

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![PowerBI](https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoftexcel&logoColor=white)

**Business problem:** A retail chain with 45 stores across 5 Indian cities had no unified view of store performance, category trends, inventory health, or promotional ROI. Regional managers received inconsistent manual reports two weeks late.

**Full data pipeline:**

```
Python (generate) → PostgreSQL (store + analyse) → Power BI (visualise) → Excel VBA (deliver)
```

| Layer | Tool | What it does |
|-------|------|-------------|
| **Ingest** | Python + NumPy | Generates 100,000 POS transactions: 45 stores, 250 SKUs, 8 categories, 2 years, festive season spikes, promotional campaigns |
| **Store** | PostgreSQL | 5 tables (`transactions`, `stores`, `products`, `inventory`, `campaigns`) + bulk load via `psycopg2` |
| **Analyse** | SQL Views | `v_store_performance` (YoY ranking), `v_category_trends` (MoM growth), `v_inventory_health` (stockout risk), `v_promo_effectiveness` (revenue lift) |
| **Visualise** | Power BI | Live connection to PostgreSQL views — 2-page exec dashboard with store ranking, category heatmap, MoM trend, and inventory alerts |
| **Deliver** | Excel + VBA | Auto-imports `store_performance.csv`, formats regional manager report with sparklines and conditional arrows, exports weekly PDF |

**Key business insights surfaced:**
- Premium stores (BKC, Connaught Plaza) account for 31% of revenue on 8% of transaction volume — basket size 3× standard stores
- Electronics spikes 188% in Oct–Dec; Groceries remain flat — category-specific inventory buffers needed
- 34 SKUs flagged as stockout risk: high weekly velocity + <2 weeks remaining stock
- Promotional campaigns drove only 8% revenue lift net of discount cost — below the 15% threshold to justify continuation

📁 [`project-5-capstone-retail/`](./project-5-capstone-retail)

---

## Tech Stack

<div align="center">

### Languages & Querying
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![VBA](https://img.shields.io/badge/VBA-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)

### Libraries & Frameworks
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

### Tools & Databases
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

</div>

---

## Repository Structure

```
data-analytics-portfolio/
│
├── README.md                          ← You are here
│
├── project-1-excel-pl-model/
│   ├── RetailChain_PL_Model.xlsm      ← Main workbook (macros enabled)
│   ├── screenshots/                   ← Dashboard, P&L, sensitivity heatmap
│   └── README.md                      ← Project documentation
│
├── project-2-sql-rfm-engine/
│   ├── schema.sql                     ← CREATE TABLE + indexes
│   ├── data_generator.py              ← Python script: 50K orders
│   ├── business_queries.sql           ← 10 analytical queries
│   ├── rfm_scoring.sql                ← RFM CTE + segment labels
│   ├── cohort_retention.sql           ← Month-0 to Month-12 matrix
│   ├── views.sql                      ← 3 reusable CREATE VIEW statements
│   ├── screenshots/                   ← Query results, cohort matrix
│   └── README.md
│
├── project-3-python-ipl-analytics/
│   ├── data/
│   │   └── ipl_deliveries.csv         ← 15,000-row synthetic dataset
│   ├── src/
│   │   ├── data_generator.py          ← Synthetic data with numpy
│   │   ├── feature_engineering.py     ← Phase, RRR, CRR columns
│   │   ├── analysis.py                ← Batting, bowling, phase analysis
│   │   ├── win_probability.py         ← Logistic regression model
│   │   └── visualise.py               ← All 6 matplotlib/seaborn charts
│   ├── outputs/
│   │   └── *.png                      ← 6 saved visualisations
│   ├── notebooks/
│   │   └── EDA.ipynb                  ← Exploratory analysis notebook
│   ├── requirements.txt
│   └── README.md
│
├── project-4-powerbi-hr-dashboard/
│   ├── HR_Attrition_Dashboard.pbix    ← Power BI report file
│   ├── data/
│   │   └── WA_Fn_UseC_HR_Employee_Attrition.csv  ← IBM HR dataset
│   ├── dax_measures.md                ← All 6 DAX measures documented
│   ├── screenshots/                   ← All 3 report pages
│   └── README.md
│
└── project-5-capstone-retail/
    ├── python/
    │   └── data_generator.py          ← 100K POS transactions
    ├── sql/
    │   ├── schema.sql
    │   ├── load_data.py               ← psycopg2 bulk loader
    │   └── views.sql                  ← 4 analytical views
    ├── powerbi/
    │   └── Retail_Intelligence.pbix
    ├── excel/
    │   └── Regional_Manager_Report.xlsm
    ├── screenshots/                   ← All 4 tools shown
    └── README.md
```

---

## GitHub Stats

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=your-username&show_icons=true&theme=default&hide_border=true&title_color=1D9E75&icon_color=1D9E75)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=your-username&layout=compact&theme=default&hide_border=true&title_color=1D9E75)

</div>

---

## Let's Connect

I'm actively looking for **data analyst** or **business analyst** roles where I can bring these skills to real business problems.

<div align="center">

| Platform | Link |
|----------|------| |
| 📧 Email | [ayushkhande66@gmail.com](mailto:your.email@gmail.com) |
| 📍 Location | Maharashtra, India |
| 🕐 Open to | Full-time · Contract · Remote |

</div>

---

<div align="center">

*If any of these projects helped you, consider leaving a ⭐ on the repo — it genuinely helps!*

**Built with curiosity, late nights, and zero copied tutorials.**

</div>