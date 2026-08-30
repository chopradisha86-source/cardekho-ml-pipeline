# Car Dekho Data Analysis & Visualizations


[![Python](https://img.shields.io/badge/Python-3.12-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-150458.svg)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-3776AB.svg)](https://seaborn.pydata.org/)
[![VS Code](https://img.shields.io/badge/VS%20Code-IDE-007ACC.svg)](https://code.visualstudio.com/)

---

## 🛠️ Tech Stack & Dependencies
- **Programming Language:** Python 3.12
- **Data Manipulation & Processing:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Environment:** VS Code, Jupyter Notebooks
- **Version Control:** Git, GitHub

---

## 📁 Repository Structure
\```text
cardekho-ml-pipeline/
├── data/
│   └── car_data.csv          # Raw CarDekho dataset
├── notebooks/
│   └── eda_and_modeling.ipynb # Comprehensive EDA & Visualization Notebook
├── .gitignore                # Git exclusion rules
├── requirements.txt          # Python environment dependencies
└── README.md                 # Project documentation
\```

---

## 📊 Key Analytical Insights & Scope

The analysis answers 25 targeted questions structured into four main phases:

### 1. General Dataset Overview

* **Manufacturing Span:** Identifies the minimum and maximum manufacturing years present in the dataset.
* **Price Range:** Evaluates minimum and maximum resale prices (`Selling_Price`).
* **Data Health:** Scans total record counts and verifies missing values per attribute.
* **Categorical Breakdown:** Quantifies vehicle sales across `Fuel_Type` (Petrol, Diesel, CNG), `Seller_Type` (Dealer vs. Individual), `Transmission` (Manual vs. Automatic), and ownership history (`Owner`).

### 2. Cost Depreciation Drivers

* **Depreciation Feature:** Engineers `Vehicle_Age` (`Current_Year - Year`) and `Cost_Depreciation` (`Present_Price - Selling_Price`).
* **Brand Performance:** Isolates vehicle brands least and most affected by resale price drops.
* **Key Correlation:** Highlights the relationship between vehicle age, kilometers driven (`Kms_Driven`), and cumulative price depreciation.

### 3. Two-Wheeler (Bikes) Sub-Analysis

* Filters and isolates bike models (e.g., Royal Enfield, KTM, Bajaj, Hero, Honda Activa).
* Identifies the oldest, newest, and highest-volume bikes sold.
* Analyzes price outliers representing premium deals exceeding market expectations.

### 4. Four-Wheeler (Cars) Sub-Analysis

* Isolates car records to analyze price distributions across luxury vs. standard segments.
* Tracks depreciation curves across automatic vs. manual transmissions and individual vs. dealer sales.

---

## 📈 Visualizations Highlighted

* **Selling Price Distribution & Fuel Counts:** Combined histogram and Seaborn count plots evaluating market volume.
* **Correlation Matrix Heatmap:** Annotated heatmap illustrating relationships between `Vehicle_Age`, `Kms_Driven`, `Present_Price`, and `Cost_Depreciation`.
* **Outlier Boxplots:** Box plots isolating high-value vehicle deals that exceed average market valuations.
* **Scatter Plots:** Multi-variable scatter plots showing price decay over vehicle age categorized by transmission type.

---

## ⚙️ How to Run Locally

### 1. Clone the Repository

\```bash
git clone https://github.com/YOUR_USERNAME/cardekho-ml-pipeline.git
cd cardekho-ml-pipeline
\```

### 2. Set Up Virtual Environment

\```bash
# On Windows
python -m venv venv
.\venv\Scripts\activate

# On Mac/Linux
python3 -m venv venv
source venv/bin/activate
\```

### 3. Install Dependencies

\```bash
pip install -r requirements.txt
\```

### 4. Run the Notebook in VS Code

1. Open the folder in **VS Code**.
2. Open `notebooks/eda_and_modeling.ipynb`.
3. Select the `venv` kernel in the top-right corner and execute all cells.
