# ⚙️ Automated Performance & Audit Intelligence (Python / ETL)

![Z-Score Analysis](zscore_analysis.png)

*(Above: The final automated output, utilizing NumPy to identify statistical outliers based on Z-Score thresholds.)*

## 🎯 The Goal & Business ROI
In corporate operations and EdTech, the manual auditing of performance records is highly susceptible to human error, with raw datasets often arriving with missing values and inconsistent data types.

*   **The Objective:** Build a repeatable Python-driven ETL (Extract, Transform, Load) pipeline to clean messy records, engineer composite KPIs, and execute a "Relative Performance" audit using Sample Standard Deviation.
*   **The ROI:** Reduced manual reporting time by an estimated **80%**, enabling management to shift focus from administrative data-entry to targeted, data-validated risk mitigation.

---

## 💡 Strategic Recommendations & ROI Roadmap
*Summary: Moving from "Subjective Auditing" to "Algorithmic Precision."*

<details>
<summary><b>▶ Click to expand: Data-Validated Business Solutions</b></summary>

### Solution 1: Operational Efficiency (Automated Feedback)
**The Problem:** Managers spend hours manually reviewing metrics and writing status updates.
*   **The Action:** Integrate Python conditional statements (`if/else` loops) to generate automated status reports based on final scores (e.g., "High Performer" vs. "Intervention Required").
*   **The ROI:** Eliminates bottlenecking in the reporting phase, generating an **80% time-saving** in administrative overhead.

### Solution 2: Targeted Intervention (Risk Mitigation)
**The Problem:** Support resources are often distributed evenly, which is highly inefficient.
*   **The Action:** Utilise Z-Score modelling to identify exact statistical outliers (e.g., $Z < -1.0$). 
*   **The ROI:** Prevents "Resource Waste." Support capital and management time are deployed exclusively to the individuals flagged by the mathematical filter, ensuring maximum impact.
</details>

---

## 🛠️ The Technical Engine (ETL Pipeline Architecture)
I applied a systematic "Data-First" approach using **Pandas and NumPy** to ensure absolute data integrity before running any statistical models.

### 1. Exploratory Data Analysis (Schema Profiling)
Executed an initial EDA script to profile the dataset's structure and identify corruption.
![Data Audit](data_audit.png)
*   **Null Profiling:** Utilised Pandas (`df.info()` and `df.isnull().sum()`) to instantly verify data types and isolate missing (`NaN`) values before they could break the statistical model.

### 2. Data Cleaning & Feature Engineering
![Cleaning Logic](cleaning_logic.png)
*   **Missing Value Imputation:** Utilised `df.fillna()` with the column's mean to fill data gaps, ensuring the sample size remained statistically significant without artificially skewing the variance.
*   **Type Casting:** Standardised the dataset by converting floating-point numbers to integers using `astype(int)`.
*   **Composite KPIs:** Engineered a new `Average_Score` column by aggregating core metrics, providing stakeholders with a single, weighted KPI of overall performance.

### 3. Z-Score Outlier Analysis (NumPy)
To remove subjectivity, I transitioned the data into NumPy arrays to calculate the **Z-Score** for every record. In data analysis (and quantitative trading), Z-scores are the ultimate measure of volatility—they identify exactly how many standard deviations a result is from the mean.

![Z-Score Analysis](zscore_analysis.png)
*   **Statistical Logic:** Utilised `np.std(scores, ddof=1)` to correctly calculate the *Sample* Standard Deviation.
*   **The Filter:** Applied the formula `Z = (X - μ) / σ` to map Z-scores back into the Pandas DataFrame, instantly flagging both over-performers and at-risk individuals.

---

## 🏆 Core Competencies Demonstrated
*   **Data Pipeline Engineering (ETL):** Successfully translated a manual, error-prone auditing process into a highly scalable Python script.
*   **Data Integrity & Wrangling:** Expert-level handling of missing data (`NaN`), schema inconsistencies, and type conversions using Pandas.
*   **Statistical Profiling:** Proven ability to utilise Sample Standard Deviation (`ddof=1`) to find deep, actionable insights hidden within "Data Noise."
*   **Risk Architecture:** Applied quantitative outlier detection (Z-Scores) to corporate performance data to mitigate operational risk.

---

## ⚙️ Setup & Reproduction
*   **Technical Audit:** The full Python execution script, conditionals, and data-cleaning transformations are fully documented in the **[Automated_Performance_Intelligence_Technical_Report.pdf](Automated_Performance_Intelligence_Technical_Report.pdf)**.

---
*This project was completed as part of the Professional Certificate in Data Analytics & AI (Code Institute).*
