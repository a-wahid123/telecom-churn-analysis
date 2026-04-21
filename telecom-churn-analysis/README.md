# Customer Success Operations: Data-Driven Churn Prevention & Account Health System

End-to-end Customer Success analytics project featuring predictive churn modelling, customer health scoring, and operational playbooks enabling CS teams to proactively retain at-risk accounts and drive expansion revenue.

---

## 🎯 Project Overview

Comprehensive churn analysis and retention strategy for a telecom company, combining data analytics with Customer Success strategy. This project demonstrates how a data-literate CSM can translate raw customer data into actionable retention playbooks, revenue impact analysis, and executive-ready business cases.

---

## 📊 Business Context

- **Dataset:** 7,043 telecom customers
- **Problem:** 26.54% churn rate resulting in $1,452,475 annual revenue loss
- **Goal:** Identify churn drivers, quantify revenue impact, and build a CS intervention framework to recover an estimated $1,016,355 in annual revenue

---

## 🛠️ Tech Stack

- Python (pandas, matplotlib, seaborn, scikit-learn)
- Power BI
- Jupyter Notebooks

---

## 📁 Project Structure

```
telecom-churn-analysis/
├── data/
│   ├── raw/
│   │   └── Telco-Customer-Churn.csv
│   └── processed/
│       ├── telecom_churn_cleaned.csv
│       ├── health_scores.csv
│       └── cleaning_log.txt
├── notebooks/
│   ├── 01_business_context.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_eda_demographics.ipynb
│   ├── 04_eda_services_contracts_CS_FOCUSED.ipynb
│   └── 05_predictive_modelling & customer_health_score.ipynb
├── dashboard/
│   ├── telecom_churn_dashboard.pbix
│   └── telecom_churn_dashboard.pdf
├── images/
└── README.md

```

---

## 🚀 Status

🔄 🎉 COMPLETE — April 2026

```
Week 1  ✅ Setup + Business Context
Week 2  ✅ Data Cleaning
Week 3  ✅ EDA — Demographics
Week 4  ✅ EDA — Services, Contracts & CS Business Case
Week 5  ✅ Predictive Modelling
Week 6  ✅ Customer Health Score System
Week 7  ✅ Power BI Dashboard

Progress: 7/7 weeks complete 🎯
```

---

## 📅 Project Log

---

### Week 1 — February 2026 ✅ COMPLETE

**Accomplishments:**
- ✅ Set up project folder structure and GitHub repository
- ✅ Loaded and explored raw dataset (7,043 rows × 21 columns)
- ✅ Documented business context and problem statement
- ✅ Identified initial data quality issues for Day 2

**Files Created:**
- `notebooks/01_business_context.ipynb`
- `data/raw/Telco-Customer-Churn.csv`

---

### Week 2 — February 7, 2026 ✅ COMPLETE
**Time spent:** 2 hours (including debugging)

**Accomplishments:**
- ✅ Fixed TotalCharges data type (object → float64)
- ✅ Handled 11 missing values (new customers with 0 tenure → filled with $0.00)
- ✅ Created binary target variable (Churn_Binary: 0/1 for modelling)
- ✅ Validated all data types and ranges — no errors found
- ✅ Saved cleaned dataset to `data/processed/telecom_churn_cleaned.csv`
- ✅ Documented all cleaning decisions in `cleaning_log.txt`
- ✅ Implemented professional relative paths for portability

**Data Cleaning Results:**
- Final dataset: **7,043 rows × 22 columns**
- Missing values fixed: **11 customers** (filled with 0.00)
- Churn rate maintained: **26.54%**
- All data quality issues resolved ✅

**Key Learnings:**
- Importance of working from the correct directory
- Relative vs absolute file paths
- Systematic data cleaning methodology and documentation

**Files Created:**
- `data/processed/telecom_churn_cleaned.csv`
- `data/processed/cleaning_log.txt`
- `notebooks/02_data_cleaning.ipynb`

---

### Week 3 — February 15, 2026 ✅ COMPLETE
**Time spent:** 2 hours

**Accomplishments:**
- ✅ Completed demographic churn analysis across 5 variables
- ✅ Identified tenure as the #1 churn risk factor (47.7% first-year churn)
- ✅ Identified senior citizens as a high-risk segment (41.7% churn)
- ✅ Identified high-risk profile: Senior + No Partner + Tenure < 12 months (60%+ churn)
- ✅ Calculated annual revenue loss from churn: $1,452,475
- ✅ Built CS playbooks for three demographic risk segments
- ✅ Added CS implications section to all findings

**Key Findings:**
- First-year customers churn at **47.7%** — 5x higher than loyal customers (49+ months at 9.5%)
- Senior citizens churn at **41.7%** vs 23.6% for non-seniors
- Annual revenue at risk from first-year churn alone: **$1.48M**

**Key Learnings:**
- `groupby().mean()` as the core pattern for churn rate analysis
- `.agg()` for multi-metric grouped summaries
- How to translate data findings into CS playbooks
- Framing analysis through a Customer Success lens rather than pure analytics

**Files Created:**
- `notebooks/03_eda_demographics.ipynb`

---

### Week 4 — March 22, 2026 ✅ COMPLETE
**Time spent:** 5+ hours across multiple sessions

**Accomplishments:**
- ✅ Completed services and contracts churn analysis (4 investigations)
- ✅ Built revenue impact analysis across 3 variables
- ✅ Discovered critical cross-variable pattern: Electronic Check × Month-to-month overlap
- ✅ Produced 6 professional visualisations with insight-driven titles
- ✅ Wrote CS playbooks for all service and contract segments
- ✅ Completed full Executive Summary and CS Business Case

**Key Findings:**
- Fiber Optic customers churn at **42%** — driving **$1,424,108** in annual revenue loss
- Month-to-month contracts churn at **42.7%** — **15x higher** than two-year contracts — driving **$1,318,674** in annual revenue loss
- Electronic check customers churn at **45%** — **78.2%** are also on month-to-month contracts, compounding the same retention problem
- Customers without Online Security and Tech Support churn at **~42% each** — nearly 3x those with add-ons

**Revenue Impact Summary:**

| Segment | Annual Revenue Loss |
|---|---|
| Fiber Optic | $1,424,108 |
| Month-to-month contracts | $1,318,674 |
| Electronic check payments | $980,040 |
| **Total annual churn loss** | **$1,452,475** |

**CS Business Case — Projected Recovery:**

| Intervention | Target Reduction | Customers Retained | Revenue Recovered |
|---|---|---|---|
| Fiber Optic retention programme | 42% → 30% | 368 | $407,929 |
| Month-to-month conversion strategy | 43% → 30% | 492 | $392,000 |
| Electronic check friction resolution | 45% → 33% | 236 | $216,426 |
| **Total projected recovery** | | **1,096** | **$1,016,355** |

*Combined interventions recover approximately **70% of total annual churn revenue loss.***

**Technical Skills Developed:**
- `pd.crosstab()` with `normalize='index'` and `normalize='columns'`
- Dictionary-based `.agg()` for multi-column grouped analysis
- Revenue impact calculations as derived columns
- Horizontal bar charts with `axvline` baseline reference
- Subplot creation with `plt.subplots()` for side-by-side charts
- Bar value annotations using `ax.patches` loop
- Segment-specific colour palettes for visual emphasis

**CS Strategy Skills Developed:**
- Translating churn data into prioritised CS intervention recommendations
- Quantifying retention savings to build executive business cases
- Identifying cross-variable patterns (converging signals)
- Perceived value analysis for premium customer segments
- Framing findings as CSM-actionable playbooks

**Files Created:**
- `notebooks/04_eda_services_contracts_CS_FOCUSED.ipynb`

---

## 💡 Key Takeaway — Week 4

> *"Data without a business case is just numbers. The real skill is knowing which segments to prioritise, why they matter in revenue terms, and what a CS team should actually do about it — starting tomorrow morning."*

---

### Week 5 — March 28 2026 ✅ COMPLETE
**Time spent:** 3 sessions across multiple days
**Accomplishments:**

✅ Learned core predictive modelling concepts — feature selection, target variable, train/test split, model training and evaluation
✅ Encoded categorical variables using .map() for binary columns and pd.get_dummies() for multi-category columns
✅ Applied StandardScaler to normalise features before modelling
✅ Built, trained and evaluated a Logistic Regression model using scikit-learn
✅ Conducted full model evaluation — accuracy, precision, recall and classification report
✅ Extracted and visualised feature importance using model coefficients
✅ Produced professional feature importance chart with red/green colouring distinguishing churn risk from churn protection
✅ Wrote CS insight connecting model findings to actionable CSM priorities

**Model Performance:**

Accuracy: 81.90%
Precision: 68.67% — when the model flags a customer as at-risk, it is correct 69% of the time
Recall: 58.18% — the model correctly identifies 58% of customers who will churn

**Key Findings:**

Fiber Optic service is the strongest positive churn driver (coefficient: +0.627) — confirming and quantifying the Day 4 finding
Tenure is the strongest churn protection factor (coefficient: -0.799) — long-tenure customers are the most insulated from churn regardless of other factors
Two-year contracts provide the second strongest churn protection (coefficient: -0.604)
At 81.9% accuracy, the model gives CS teams a significantly more reliable at-risk account prioritisation tool than manual identification alone

**Technical Skills Developed:**

Categorical variable encoding — .map({'Yes': 1, 'No': 0}) for binary columns and pd.get_dummies(drop_first=True) for multi-category columns
Feature scaling with StandardScaler — fit_transform on training data, transform only on test data
Train/test split with train_test_split(test_size=0.2, random_state=42)
Logistic Regression training and prediction with scikit-learn
Model evaluation using accuracy_score, precision_score, recall_score, and classification_report
Feature importance extraction from model.coef_ and visualisation with conditional colour palettes
List comprehension for dynamic colour assignment based on coefficient sign

**Key Concepts Learned:**

Data leakage — why the target variable must never be included as a feature
Class imbalance — why models perform better on the majority class (no churn) than the minority class (churn)
Confounding variables — why multivariate modelling can reveal relationships that contradict simple univariate analysis
fit vs transform — the scaler learns parameters from training data only and applies them to test data
Precision vs recall tradeoff — and how CSM capacity constraints influence which metric to optimise for

**CS Strategy Skills Developed:**

Translating model accuracy metrics into plain business language for non-technical CS stakeholders
Connecting feature importance coefficients to revenue impact and CSM prioritisation decisions
Understanding the human-in-the-loop principle — using model predictions as a starting point, complemented by CSM judgment and customer relationship context

**Files Created:**
- `notebooks/05_predictive_modelling.ipynb`


---

### Week 6 — April 4, 2026 ✅ COMPLETE
**Time spent:** Multiple sessions

**Accomplishments:**
- ✅ Generated churn probability scores for all 7,043 customers using the Day 5 logistic regression model
- ✅ Built a three-component Customer Health Scoring system combining churn probability (50%), tenure risk (30%), and contract risk (20%)
- ✅ Normalised tenure and contract risk into comparable 0-1 scales for consistent weighting
- ✅ Classified all customers into three health categories — 🔴 Critical, 🟡 At Risk, 🟢 Healthy
- ✅ Built a CSM Action Table with recommended intervention for every customer
- ✅ Produced a CS Team Daily Priority List identifying the top 10 highest-risk accounts
- ✅ Produced professional health score distribution chart with threshold reference lines
- ✅ Wrote CS insight connecting health score findings to onboarding and expansion strategy

**Health Score Distribution:**

| Category | Score Range | Customers | Percentage |
|---|---|---|---|
| 🔴 Critical | 0 - 40 | 2,319 | 32.9% |
| 🟡 At Risk | 41 - 70 | 2,167 | 30.8% |
| 🟢 Healthy | 71 - 100 | 2,557 | 36.3% |

**Top 3 Most At-Risk Accounts:**

| Customer ID | Health Score | Churn Probability |
|---|---|---|
| 5178-LMXOP | 7.2 | 86.4% |
| 7216-EWTRS | 7.3 | 86.3% |
| 9497-QCMMS | 7.4 | 86.0% |

**Key Findings:**
- Nearly a third of the customer base (32.9%) falls in the critical zone — requiring immediate CS intervention
- A significant spike of healthy customers scoring near 100 confirms that long-tenure, committed customers become highly stable and extremely unlikely to churn over time
- The health score distribution reinforces the core finding across Days 3, 4 and 5 — the earliest stage of the customer journey is where churn risk is highest and CS investment has the greatest impact
- CS interventions should be heavily concentrated on onboarding and first-to-second year success programmes; as customers stabilise, the focus should shift toward renewal, expansion, and upgrade conversations tailored specifically to each client's organisational context

**Technical Skills Developed:**
- `model.predict_proba()` to extract churn probability scores for all customers
- `scaler.transform()` vs `scaler.fit_transform()` — applying existing scaler parameters to new data without refitting
- Feature normalisation — converting tenure to a 0-1 risk scale using `1 - (tenure / max_tenure)`
- Weighted scoring formula combining multiple components into a single health score
- `pd.cut()` for binning continuous scores into categorical health bands
- `.map()` for assigning recommended actions based on category labels
- `sns.histplot()` for distribution visualisation with vertical threshold reference lines

**Key Concepts Learned:**
- Weighted scoring systems — why different components deserve different weights based on predictive strength
- Health score inversion — converting a risk score to a health score so higher always means healthier
- Traffic light classification — translating continuous scores into actionable CS categories
- Human-in-the-loop principle — model scores as a starting point, complemented by CSM judgment and client-specific context
- Expansion and upgrade conversations require client research and contextual tailoring, not a one-size-fits-all approach

**CS Strategy Skills Developed:**
- Translating raw churn probability into an operational daily priority tool for CS teams
- Designing a health scoring framework that balances model predictions with business-relevant factors
- Connecting health score findings to specific CSM actions — from 24-hour outreach for critical accounts to expansion conversations for healthy accounts
- Understanding that the CS team's highest leverage point is the early customer journey, and that long-term retention is built through consistent early engagement

**Files Created:**
- `notebooks/06_customer_health_score.ipynb`

---

**Key Takeaway — Week 6**

> *"A churn probability tells you who might leave. A health score tells you who to call first thing Monday morning. The difference between analysis and operations is turning a number into an action."*

---

### Week 7 — April 12, 2026 ✅ COMPLETE
**Time spent:** Multiple sessions

**Accomplishments:**
- ✅ Built a complete 4-page interactive Power BI dashboard presenting the full project story from executive summary to operational CS tool
- ✅ Loaded and connected two data sources (`telecom_churn_cleaned.csv` and `health_scores.csv`) with a One-to-One relationship on `customerID`
- ✅ Created 7 DAX measures including dynamic churn rate, revenue loss, category counts, and recovery projections
- ✅ Created a calculated `Score Band` column using DAX `SWITCH()` for health score binning
- ✅ Built Page 1 — Executive Overview with 4 KPI cards and health category donut chart
- ✅ Built Page 2 — Churn Drivers with 4 horizontal bar charts highlighting critical segments in red
- ✅ Built Page 3 — Revenue Impact with 3 revenue loss charts and projected recovery KPIs
- ✅ Built Page 4 — Customer Health Monitor with traffic light KPI cards, score distribution chart, revenue-weighted priority account table, and interactive health category slicer
- ✅ Exported dashboard as PDF for GitHub portfolio

**Dashboard Pages:**

| Page | Title | Purpose |
|---|---|---|
| 1 | Executive Overview | Headline KPIs and health distribution |
| 2 | Churn Drivers | What is causing churn |
| 3 | Revenue Impact | What churn is costing the business |
| 4 | Customer Health Monitor | Who needs CS attention now |

**Key Design Decisions:**
- Red highlighting on critical bars across all chart pages — visual emphasis on the highest-risk segments
- Revenue-weighted priority table on Page 4 sorts by `annual_revenue_at_risk` rather than health score alone — ensuring CSMs call the highest-value at-risk customers first, not just the most statistically at-risk
- Traffic light colour coding (red/yellow/green) applied consistently across donut chart and KPI cards for instant readability
- Interactive slicer on Page 4 allows CSMs to filter the entire health monitor by category

**Technical Skills Developed:**
- DAX measure creation — `COUNTROWS`, `SUM`, `DIVIDE`, `SUMX`, `FILTER`, `AVERAGEX`
- DAX calculated columns — `SWITCH(TRUE())` for conditional binning
- Power BI data modelling — table relationships, cardinality, cross-filter direction
- Visual formatting — conditional bar colours, display unit formatting, slicer configuration
- Dashboard layout and design — consistent colour schemes, insight-driven titles, purposeful page structure

**Key Learnings:**
- DAX measures are dynamic — they recalculate automatically based on filter context, which is fundamentally different from static Python calculations
- `DIVIDE()` is safer than `/` in DAX because it handles zero division gracefully without crashing the dashboard
- Colour consistency across pages creates a professional, cohesive feel that signals analytical maturity
- The difference between a notebook and a dashboard is the difference between analysis and operations — a dashboard requires no technical knowledge to use, which is what makes it valuable to CS teams
- DAX syntax and logic requires further practice to write independently — identified as a development area for continued learning

**CS Strategy Skills Developed:**
- Translating six notebooks of analysis into a four-page narrative that a non-technical CS leader can navigate in under 60 seconds
- Designing an operational tool (Page 4) that a CSM can open every Monday morning and immediately know who to call first
- Revenue-weighting the priority list — recognising that churn risk alone is insufficient for prioritisation without considering the revenue value of each customer

**Files Created:**
- `dashboard/telecom_churn_dashboard.pbix`
- `dashboard/telecom_churn_dashboard.pdf`

---

**Key Takeaway — Week 7**

> *"A dashboard is not a prettier version of a notebook. It is a decision-making tool. Every design choice — colours, layout, sorting, filtering — should make it faster and easier for a CS team to take the right action. The question is always: what does someone need to do after looking at this?"*

---

**🎉 PROJECT COMPLETE**

---




## 👨‍💻 Author

**Abdul Wahid Sekyere** | [LinkedIn](https://www.linkedin.com/in/abdul-wahid-sekyere)

*Customer Success professional building data analytics expertise to drive retention, expansion, and customer health through evidence-based CS strategy.*
