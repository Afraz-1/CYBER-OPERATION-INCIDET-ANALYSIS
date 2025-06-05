# Cyber Operations Incidents Analysis

This project analyzes a dataset of global cyber operations and incidents. It performs data cleaning, exploratory data analysis (EDA), visualization, and classification modeling to understand patterns in attack sponsorship, victim profiles, response types, and more.

---

## Dataset

- **Filename**: `cyber-operations-incidents.csv`
- **Fields**: `Date`, `Sponsor`, `Victims`, `Category`, `Type`, `Response`, `Sources`, etc.
- **Focus**: Temporal trends, attack types, involved parties, and response behavior

---

## Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn, Plotly
- scikit-learn
- imbalanced-learn (SMOTE)
- (Optional) NetworkX

---

## Workflow

### 1. Data Cleaning
- Converted `Date` column to datetime format
- Extracted `Year` and `Month`
- Filled missing values with `'Unknown'`
- Dropped rows with both `Sponsor` and `Victims` missing
- Parsed `Response` into `Response_Type` and `Response_Ref`

### 2. Exploratory Data Analysis
- Attack trends by year and month
- Sponsor countries on a choropleth map
- Category-wise and type-wise distribution of attacks
- Affiliation analysis (stacked bars)
- Victim response breakdown

### 3. Preprocessing
- One-hot encoding for categorical features
- SMOTE for class imbalance
- Feature set: `Year`, `Month`, `Sponsor`, `Category`
- Target variable: `Type` (attack type)

### 4. Machine Learning
- Model: `RandomForestClassifier`
- Metrics: Accuracy, Precision, Recall, F1-score
- Visual comparison of class-wise model performance

---

## 📈 Key Visuals

- Yearly & monthly attack count line plots
- Global sponsor map
- Pie charts for attack categories
- Bar graphs of attack types and affiliations
- Response type charts per victim
- Class imbalance and model performance plots

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/cyber-ops-analysis.git
cd cyber-ops-analysis
