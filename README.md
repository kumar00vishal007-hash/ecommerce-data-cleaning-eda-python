# ecommerce-data-cleaning-eda-python
End-to-end Python project performing data cleaning, outlier treatment, and exploratory analysis on messy e-commerce dataset.
# 🛒 End-to-End E-Commerce Data Cleaning & Exploratory Data Analysis (EDA)

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Cleaning-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green)
![License](https://img.shields.io/badge/Status-Completed-brightgreen)

## 📌 Project Overview
In real-world business scenarios, raw data is often messy, incomplete, and filled with anomalies. This project demonstrates a step-by-step data analytics pipeline in Python to clean, preprocess, and analyze a raw e-commerce sales dataset containing 1,000 transaction records.

The primary objective is to transform raw, unstructured data into analysis-ready clean data and extract key business metrics around sales trends, payment modes, and regional performance.

---

## 🛠️ Tech Stack & Tools Used
* **Programming Language:** Python
* **Environment:** Google Colab / Jupyter Notebook
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **File Formats:** Excel (.xlsx), CSV (.csv)

---

## 🧹 Raw Data Quality Issues & Solutions

| Feature / Column | Issue Identified | Cleaning Action Taken |
| :--- | :--- | :--- |
| **Transaction_ID** | 83 Duplicate rows | Applied `drop_duplicates(subset=['Transaction_ID'])` |
| **Customer_Name / City** | Extra whitespaces & irregular casing | Applied `.str.strip().str.title()` |
| **Category** | Mixed names (`'elec'`, `'ELECTRONICS'`) | Standardized values to `'Electronics'` |
| **Customer_Email** | Invalid string formats (`INVALID_EMAIL`) | Replaced with `NaN` using regex validation |
| **Age** | Outliers & impossible values (`-5`, `150`, `999`) | Filtered valid range between 18 and 80 years |
| **Price & Quantity** | Negative prices (`-200`) & extreme values (`99999`) | Kept values where $0 < \text{Price} < 50000$ and $\text{Quantity} > 0$ |
| **Order_Date** | Mixed date formats (`2025-01-15`, `15/02/2025`) | Converted to standard `datetime64` with `errors='coerce'` |

---

## 📊 Visual Insights & Dashboard

![Dashboard Charts](dashboard_charts.png)

### Key Business Takeaways:
1. **Payment Preferences:** UPI is the most preferred payment channel, capturing **52.9%** of total order transactions, followed by Cash on Delivery (**30.4%**).
2. **Geographic Distribution:** Bengaluru (27%) and Mumbai (25%) generate the highest share of sales volume.
3. **Monthly Trends:** Strong sales performance observed in early Q1 (Jan - Apr), followed by a seasonal dip requiring promotional campaigns.

---

## 🚀 How to Run This Project
1. Clone this repository:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/ecommerce-data-cleaning-eda-python.git](https://github.com/YOUR_USERNAME/ecommerce-data-cleaning-eda-python.git)

   <img width="1410" height="656" alt="Screenshot 2026-10-18 172418" src="https://github.com/user-attachments/assets/52ee5189-bbcd-43b5-a2fd-7580b49c4255" />
