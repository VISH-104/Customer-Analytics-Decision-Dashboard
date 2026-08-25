# Customer Analytics & Decision Dashboard

> An end-to-end customer analytics and decision-support system that combines data engineering, business analytics, statistical analysis, machine learning, and interactive visualization to transform transactional data into actionable business decisions.

![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458.svg?logo=pandas)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-F7931E.svg?logo=scikit-learn)
![Streamlit](https://img.shields.io/badge/Streamlit-Dashboard-FF4B4B.svg?logo=streamlit)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C.svg)

---

## 1. Project Overview

**Customer Analytics & Decision Dashboard** demonstrates how raw transactional data can be transformed into customer intelligence, business insights, and actionable recommendations.

The project uses an e-commerce dataset structure as its business case, while the analytical framework is designed to be transferable across customer-driven industries such as retail, financial services, technology, marketplaces, and subscription businesses.

### End-to-End Workflow

```text
Raw Data → Validation → Feature Engineering → RFM Analysis → K-Means Segmentation → Decision Engine → Recommendations → Dashboard

## 2. Business Problem

Businesses generate large volumes of transactional data, but converting that data into actionable customer decisions remains challenging. This project addresses three core questions: **Who are the most valuable customers? Which customers are becoming inactive? What actions should be prioritized for each customer segment?**

The system combines customer analytics, segmentation, and rule-based recommendations into a single decision-support workflow.

---

## 3. Objectives

| Objective | Focus |
|---|---|
| **Customer Intelligence** | Identify customer value and behavioral segments using RFM analysis. |
| **Business Analytics** | Monitor revenue, orders, customers, trends, and key KPIs. |
| **Decision Support** | Translate analytical results into actionable recommendations. |
| **Product Delivery** | Deliver a reproducible pipeline and interactive Streamlit dashboard. |

---

## 4. Dataset & Data Strategy

The project follows the structure of the **Brazilian E-Commerce Public Dataset by Olist**, covering customers, orders, products, payments, sellers, reviews, and locations. For lightweight and reproducible execution, the current implementation generates a **5,000-order synthetic dataset** following the relevant schema. The synthetic data is used for development, testing, CI/CD, and offline demonstration and is **not presented as actual Olist observations**.

### Data Workflow

```text
Dataset Structure → Schema Definition → Synthetic/Public Data → Raw CSVs → Validation → Feature Engineering → Analytics Dataset

## 5. Analytical Methodology

### 5.1 Data Preparation

The pipeline handles **data ingestion, validation, cleaning, feature engineering, and analytical dataset generation**, including schema, missing-value, duplicate, date, and numerical checks.

### 5.2 RFM Analysis

Customer value is quantified using **Recency, Frequency, and Monetary Value (RFM)**. Log transformation is applied where required to reduce the effect of highly skewed monetary distributions.

| Metric | Measures |
|---|---|
| **Recency** | How recently a customer purchased |
| **Frequency** | How often a customer purchased |
| **Monetary** | How much a customer spent |

### 5.3 Customer Segmentation

Standardized RFM features are clustered using **K-Means** to identify customers with similar purchasing behavior.

```text
Transactions → RFM Features → Transformation → Standardization → K-Means → Customer Segments

## 6. Decision Intelligence & System Architecture

The decision layer converts customer analytics into **interpretable business actions** by combining customer behavior, segment/risk status, and business rules.

```text
Customer Data → Behavior → Segment/Risk → Business Rule → Recommended Action → KPI

The modular architecture connects data processing, analytics, decision logic, and presentation into a reproducible workflow.

Raw Transactions → Validation → Feature Engineering → Customer Analytics → Decision Engine → Dashboard

RFM and K-Means generate customer intelligence, the decision engine converts insights into recommendations, and Streamlit presents the results through an interactive dashboard.

Dashboard & Business Impact

The Streamlit dashboard provides three focused views: Executive metrics and trends, Customer Intelligence through RFM and segmentation, and Advanced Analytics for cluster and segment analysis.

Revenue Trend

Customer Segment Distribution

RFM Customer Segmentation

The platform supports high-value customer identification, early inactivity detection, targeted retention, customer prioritization, and reduced manual analysis.

## Tools & Technology 

| Category | Technologies |
|---|---|
| **Programming** | Python 3.10+ |
| **Data Analysis** | Pandas, NumPy |
| **Machine Learning** | Scikit-learn, K-Means |
| **Statistics** | SciPy |
| **Visualization & UI** | Matplotlib, Streamlit |
| **Development & Deployment** | Git, GitHub, Pytest, Docker |

Validation & Testing

The pipeline validates **data integrity, engineered features, segmentation consistency, model outputs, recommendation rules, and dashboard execution**.

Run the test suite with:

```bash
pytest
Roadmap
Analytics MVP → Predictive Analytics → Decision Intelligence → Experimentation → Productionization

| Phase | Development |
|---|---|
| **MVP** | Data pipeline, RFM, segmentation, dashboard |
| **Predictive Analytics** | Churn prediction, demand forecasting, CLV |
| **Decision Intelligence** | Automated recommendations and KPI monitoring |
| **Experimentation** | A/B testing and impact measurement |
| **Productionization** | APIs, monitoring, retraining, cloud and real-time deployment |

## Limitations

The project uses **synthetic data** unless the public Olist dataset is loaded, so results may not fully reflect real-world customer behavior. RFM and K-Means provide **descriptive, not causal, insights**, and recommendations require business validation.

Real-world ROI requires **deployment, controlled experimentation, and continuous monitoring**.

## Results

The project demonstrates an end-to-end **reproducible, interpretable, and business-oriented data product**, integrating analytics, machine learning, decision logic, and interactive visualization rather than functioning as an isolated ML model.

---

## References

1. **Olist — Brazilian E-Commerce Public Dataset**  
   https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

2. **MacQueen, J. (1967)** — *Some Methods of Classification and Analysis of Multivariate Observations.*

3. **Scikit-learn** — https://scikit-learn.org/

4. **Pandas** — https://pandas.pydata.org/

5. **Streamlit** — https://streamlit.io/
