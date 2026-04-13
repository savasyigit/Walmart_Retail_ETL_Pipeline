# Walmart_Retail_ETL_Pipeline
Built a complete ETL pipeline to extract data from a PostgreSQL database, transform and clean it, and generate analytical insights using Python and Pandas
<p align="center">
  <img src="Images/walmartecomm.jpg" width="600"/>
</p>
# 🛒 Retail Data ETL Pipeline

## 📌 Project Overview

This project demonstrates an end-to-end **ETL (Extract, Transform, Load) pipeline** built using Python.

The pipeline extracts retail sales data from a PostgreSQL database and a Parquet file, processes and cleans the data, performs aggregation, and stores the results for further analysis.

It simulates a real-world **data engineering workflow**, including data validation and analytical insights.

---

## 🎯 Objectives

* Extract data from PostgreSQL
* Integrate multiple data sources (SQL + Parquet)
* Clean and transform raw data
* Perform aggregation for insights
* Store processed data
* Validate pipeline outputs

---

## 🏗️ Project Structure

```id="k3y8y2"
ETL_Pipeline_Retail/
 ├── data/
 │    └── extra_data (1).parquet
 │
 ├── Images/
 │    └── walmartecomm.jpg
 │
 ├── output/
 │    ├── clean_data.csv
 │    └── agg_data.csv
 │
 ├── Retail_ETL_Pipeline.ipynb
 ├── README.md
```

---

## ⚙️ Technologies Used

* Python 🐍
* Pandas
* NumPy
* PostgreSQL
* psycopg2

---

## 🔄 ETL Pipeline Steps

### 1. Extract

* Data is extracted from a PostgreSQL database
* Additional data is loaded from a Parquet file
* Datasets are merged into a single DataFrame

### 2. Transform

* Convert date column to datetime
* Handle missing values
* Filter invalid records
* Create new features (Month)
* Select relevant columns

### 3. Analysis

* Calculate average weekly sales per month
* Generate business insights

### 4. Load

* Save cleaned dataset (`clean_data.csv`)
* Save aggregated dataset (`agg_data.csv`)

### 5. Validation

* Verify that output files are successfully created

---

## ▶️ How to Run

1. Clone the repository:

```bash id="c1p7jv"
git clone https://github.com/your-username/ETL_Pipeline_Retail.git
cd ETL_Pipeline_Retail
```

2. Install dependencies:

```bash id="y2p8v1"
pip install pandas numpy psycopg2
```

3. Update database connection:

```python id="m7d4k9"
conn = psycopg2.connect(
    host="YOUR_HOST",
    database="YOUR_DATABASE",
    user="YOUR_USERNAME",
    password="YOUR_PASSWORD"
)
```

4. Run the notebook step by step.

---

## 📊 Output

The pipeline generates:

* `output/clean_data.csv` → cleaned dataset
* `output/agg_data.csv` → aggregated monthly insights

---

## ⚠️ Database Connection

Database credentials are not included for security reasons.
Please configure your own database connection before running the project.

---

## 💡 Key Features

* Multi-source data integration
* Data cleaning and transformation
* Aggregation and insight generation
* Output validation
* End-to-end ETL pipeline

---

## 🚀 Future Improvements

* Convert notebook into modular pipeline (`src + main.py`)
* Add logging
* Use environment variables (.env)
* Automate pipeline scheduling

---

## 👨‍💻 Author

Built as part of a data engineering learning journey.
