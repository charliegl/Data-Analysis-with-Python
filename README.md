# 🚗 Exploratory Data Analysis — Automobile Dataset
 
A complete Exploratory Data Analysis (EDA) on an automobile dataset, exploring the relationships between vehicle features and price using statistical methods and visualizations.
 
---
 
## 📋 Overview
 
This project performs an end-to-end EDA to identify which vehicle attributes are most strongly correlated with price. It combines descriptive statistics, visual analysis, correlation coefficients, and statistical tests (ANOVA) to draw meaningful insights from the data.
 
---
 
## 📂 Dataset
 
- **Source:** IBM Developer Skills Network (via IBM Cloud Object Storage)
- **File:** `automobileEDA.csv`
- **Content:** Automobile specifications including engine size, horsepower, fuel efficiency, body style, drive wheels, and price.
---
 
## 🔍 Analysis Structure
 
### 1. Data Loading & Inspection
- Download dataset programmatically with a custom `download()` utility
- Load with `pandas` and inspect data types per column
### 2. Continuous Variables — Correlation Analysis
Regression plots and Pearson correlation coefficients between price and:
- Engine size
- Highway MPG
- Peak RPM
- Stroke
- Wheel base, horsepower, length, width, curb weight, bore, city-mpg
### 3. Categorical Variables — Distribution Analysis
Box plots to compare price distributions across:
- Body style
- Engine location
- Drive wheels
### 4. Descriptive Statistics
- `df.describe()` for numeric and object columns
- Value counts for `drive-wheels` and `engine-location`
### 5. Groupby & Pivot Tables
- Mean price grouped by drive wheels and body style
- Pivot table visualized as a heatmap (`pcolor` with `RdBu` colormap)
### 6. ANOVA
- One-way ANOVA comparing price across drive wheel types:
  - FWD vs RWD vs 4WD
  - FWD vs RWD
  - 4WD vs RWD
  - 4WD vs FWD
---
 
## 🛠️ Technologies Used
 
| Library | Purpose |
|---|---|
| `pandas` | Data manipulation |
| `numpy` | Numerical operations |
| `matplotlib` | Base plotting |
| `seaborn` | Statistical visualizations |
| `scipy.stats` | Pearson correlation & ANOVA |
| `urllib` | Dataset download |
 
---
 
## ▶️ How to Run
 
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```
 
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scipy
   ```
 
3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook exploratory-data-analysis-otro.ipynb
   ```
 
4. Run all cells — the dataset downloads automatically.
---
 
## 📊 Key Findings
 
- **Engine size** and **curb weight** show the strongest positive correlation with price.
- **Highway MPG** and **city MPG** are negatively correlated with price.
- **RWD vehicles** command significantly higher prices than FWD or 4WD (confirmed by ANOVA).
- **Engine location** (front vs rear) is a strong differentiator of price.
---
 
