# Lifestyle & Mental Health Recommender (Streamlit App)

### *MSc Big Data Analytics - Semester 3 Research Project*

* **Author:** Mauli Patel
* **Institution:** St. Xavier's College, Ahmedabad
* **Course:** MSc Big Data Analytics
* **Semester:** 3

---

## Project Overview

This repository contains the implementation of a **Lifestyle and Mental Health Recommender System** built with **Streamlit**.
The system performs **unsupervised clustering** on lifestyle, wellness, and stress survey data to identify behavioral patterns and potential wellbeing groups.

This work is part of my **Semester 3 MSc Big Data Analytics research project**, focused on **exploratory clustering for wellness prediction and personalized recommendations**.

---

## Core Objectives

* Automate preprocessing of lifestyle survey data (handling missing values, normalization, and encoding).
* Use **unsupervised learning (K-Means clustering)** to segment users by behavioral and wellness traits.
* Enable instant visual feedback through interactive charts and summary metrics.
* Optimize performance with **lazy imports** — clustering only runs when triggered by the user.
* Build a **deployable Streamlit web app** for real-time data exploration.

---

## Key Features

* **Upload CSV:** Accepts survey datasets with numeric and categorical attributes.
* **Automatic Column Detection:** Identifies numeric vs. categorical features heuristically.
* **Data Cleaning & Imputation:**

  * Median imputation for numeric features.
  * Most frequent imputation for categorical features.
* **Lazy Clustering Execution:** Heavy computation only runs on demand.
* **Interactive EDA Visuals:** Cluster distribution, age breakdowns, silhouette and Davies–Bouldin metrics.
* **Session Caching:** Retains clustering state across interactions.

---

## ⚙️ Tech Stack

| Component       | Technology Used     |
| --------------- | ------------------- |
| Frontend        | Streamlit           |
| Data Handling   | Pandas, NumPy       |
| Visualization   | Matplotlib, Seaborn |
| ML / Clustering | scikit-learn        |
| Imputation      | SimpleImputer       |
| Environment     | Python 3.10+        |

---

## Repository Structure

```
Lifestyle-MentalHealth-Recommender/
│
├── app.py                # Main Streamlit app
├── README.md             # Project documentation
├── requirements.txt      # Python dependencies
└── sample_data.csv       # Example survey dataset (optional)
```

---

## How to Run Locally

1. **Clone this repository**

   ```bash
   git clone https://github.com/yourusername/lifestyle-recommender.git
   cd lifestyle-recommender
   ```

2. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

   *(Or manually install:)*

   ```bash
   pip install streamlit pandas numpy seaborn matplotlib scikit-learn
   ```

3. **Run the app**

   ```bash
   streamlit run app.py
   ```

4. **Open the app**
   Visit → [http://localhost:8501](http://localhost:8501)

---

## Workflow Summary

### **1. Data Upload**

Upload your lifestyle or wellness survey dataset (CSV).
Example columns:

```
"How stressed do you feel due to work?"
"How many hours do you sleep on average?"
"How often do you take breaks from screen?"
```

### **2. Preprocessing**

* Detects and converts numeric columns.
* Imputes missing values using median/mode.
* Normalizes text categorical columns.

### **3. Clustering**

* Runs **K-Means** with configurable `k`.
* Computes clustering quality metrics:

  * Silhouette Score
  * Davies–Bouldin Index

### **4. Visualization**

* Displays:

  * Cluster distribution bar chart
  * Age distribution (if available)
  * Metric summaries

---

## Research Context

This tool is developed as part of academic research in **behavioral data analytics** — focusing on how lifestyle factors correlate with mental wellbeing.
It aims to serve as an **EDA + clustering prototype** for larger-scale mental health analytics projects.

---

## Possible Extensions

* Integration with wellness APIs or Fitbit data
* Deployment on Streamlit Cloud or Hugging Face Spaces
* Recommendation engine using cluster insights
* Dimensionality reduction (PCA, t-SNE) for visualization
* Saving model outputs and user insights

---

## Citation / Acknowledgement

If you use this project or its methodology for academic or research purposes, please cite:

> Mauli Patel (2025). *Lifestyle & Mental Health Recommender using Streamlit and K-Means Clustering.* MSc Big Data Analytics, Semester 3 Research Project.

---

## Author

* **Mauli Aptel**
* Data Science Student | MSc Big Data Analytics
* [LinkedIn](https://linkedin.com/in/your-profile) 

---

## Example `requirements.txt`

```txt
streamlit
pandas
numpy
matplotlib
seaborn
scikit-learn
```
