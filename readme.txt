# AI-Powered Sales Analytics, Forecasting & Business Intelligence Dashboard

An end-to-end data analytics, machine learning, and business intelligence pipeline combining Python, SQLite, Machine Learning, Power BI, and LLM-driven executive insights.

---

## 🏗️ Architecture Workflow
Python (Cleaning & EDA) → SQLite (SQL Analysis) → Scikit-Learn (ML Forecasting) → Power BI (Dashboard) → Gemini API (AI Insights)

---

## 📊 Power BI Dashboard Screenshots

### Page 1: Executive Overview
![Executive Overview](assets/dashboard_overview.png)

### Page 2: Forecasting & Advanced Insights
![Forecasting Page](assets/dashboard_forecast.png)

---

## 🚀 Project Overview & Phases

1. **Data Cleaning & Preprocessing (`src/01_preprocess.py`):**
   - Handled missing numerical values using median imputation.
   - Removed duplicate records to ensure data integrity.
   - Parsed date fields and engineered revenue, month, quarter, and day-of-week features.

2. **SQL Analysis (`src/02_sql_analysis.py`):**
   - Loaded cleaned data into an in-memory SQLite database.
   - Executed multi-table queries to isolate category revenue, regional performance, and monthly trends.

3. **Machine Learning Forecasting (`src/03_ml_forecast.py`):**
   - Aggregated data monthly and engineered lag features (`lag_1`, `lag_2`).
   - Trained a **Random Forest Regressor** using a chronological train/test split.
   - Evaluated model performance using **MAE, RMSE, and R² scores**.

4. **Power BI Dashboard:**
   - Developed multi-page interactive reports with custom DAX measures (`Total Revenue`, `Total Units Sold`, `Average Order Value`).
   - Utilized native Power BI analytics features to project 6-month sales forecasts.

5. **LLM Integration (Gemini API):**
   - Built a direct Python script utilizing the `google-genai` SDK to ingest verified metrics and automatically generate strategic executive recommendations.

---

## 🛠️ Tech Stack
- **Language:** Python
- **Database:** SQLite & SQL
- **Machine Learning:** Scikit-Learn (Random Forest)
- **Data Visualization:** Matplotlib, Seaborn, Power BI
- **AI / LLM:** Google Gemini API (`gemini-2.5-flash`)