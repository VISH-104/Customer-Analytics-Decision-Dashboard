# Customer Analytics & Decision Dashboard

> An end-to-end customer analytics and decision-support system that transforms transactional data into customer intelligence, actionable recommendations, and business insights.

##  Project Overview

This project demonstrates an end-to-end workflow for converting raw transactional data into **customer analytics, machine-learning-based segmentation, business recommendations, and an interactive dashboard**.

### End-to-End Workflow

```text
Raw Data → Validation → Feature Engineering → RFM Analysis → K-Means Segmentation → Decision Engine → Recommendations → Dashboard
```

The framework is designed to be applicable across customer-driven businesses such as **retail, e-commerce, finance, technology, marketplaces, and subscription services**.

---

##  Business Problem

Businesses generate large volumes of transactional data, but converting that data into actionable customer decisions remains challenging. This project addresses three core questions: **Who are the most valuable customers? Which customers are becoming inactive? What actions should be prioritized for each customer segment?**

The system combines customer analytics, segmentation, and rule-based recommendations into a single decision-support workflow.

---

##  Objectives

| Objective | Focus |
|---|---|
| **Customer Intelligence** | Identify customer value and behavioral segments using RFM analysis. |
| **Business Analytics** | Monitor revenue, orders, customers, trends, and key KPIs. |
| **Decision Support** | Translate analytical results into actionable recommendations. |
| **Product Delivery** | Deliver a reproducible pipeline and interactive Streamlit dashboard. |

---

##  Dataset & Data Strategy

The project follows the structure of the **Brazilian E-Commerce Public Dataset by Olist**, covering customers, orders, products, payments, sellers, reviews, and locations.

For lightweight and reproducible execution, the current implementation generates a **5,000-order synthetic dataset** following the relevant schema. The synthetic data is used for development, testing, CI/CD, and offline demonstration and is **not presented as actual Olist observations**.

##  Analytical Methodology

### Data Preparation

The pipeline handles **data ingestion, validation, cleaning, feature engineering, and analytical dataset generation**, including schema, missing-value, duplicate, date, and numerical checks.

###  RFM Analysis

Customer value is quantified using **Recency, Frequency, and Monetary Value (RFM)**. Log transformation is applied where required to reduce the effect of highly skewed monetary distributions.

| Metric | Measures |
|---|---|
| **Recency** | How recently a customer purchased |
| **Frequency** | How often a customer purchased |
| **Monetary** | How much a customer spent |

###  Customer Segmentation

Standardized RFM features are clustered using **K-Means** to identify customers with similar purchasing behavior.

```text
Transactions → RFM Features → Transformation → Standardization → K-Means → Customer Segments
```

Clusters are interpreted from their RFM characteristics to identify groups such as **high-value, regular, low-engagement, and at-risk customers**.

---

## Decision Intelligence & System Architecture

The decision layer converts customer analytics into **interpretable business actions** by combining customer behavior, segment/risk status, and business rules.

```text
Customer Data → Behavior → Segment/Risk → Business Rule → Recommended Action → KPI
```

The modular architecture connects data processing, analytics, decision logic, and presentation into a reproducible workflow.

```text
Raw Transactions → Validation → Feature Engineering → Customer Analytics → Decision Engine → Dashboard
```

**RFM and K-Means** generate customer intelligence, the **decision engine** converts insights into recommendations, and **Streamlit** presents the results through an interactive dashboard.

---

##  Dashboard & Business Impact

The Streamlit dashboard provides three focused views: **Executive** metrics and trends, **Customer Intelligence** through RFM and segmentation, and **Advanced Analytics** for cluster and segment analysis.

**Revenue Trend**
**Customer Segment Distribution**
**RFM Customer Segmentation**

The platform supports **high-value customer identification, early inactivity detection, targeted retention, customer prioritization, and reduced manual analysis**.

> **Note:** Since the project uses public/synthetic data, no real-world ROI is claimed. Impact estimates are scenario-based; actual business impact requires deployment and controlled experimentation such as A/B testing.

The pipeline validates **data integrity, engineered features, segmentation consistency, model outputs, recommendation rules, and dashboard execution**.

##  Roadmap

```text
Analytics MVP → Predictive Analytics → Decision Intelligence → Experimentation → Productionization
```

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

##  Results

The project demonstrates an end-to-end **reproducible, interpretable, and business-oriented data product**, integrating analytics, machine learning, decision logic, and interactive visualization rather than functioning as an isolated ML model.

```text
Business Problem → Data → Analytics → Machine Learning → Decision Intelligence → Dashboard → Business Action
```

---

## References

1. **Olist — Brazilian E-Commerce Public Dataset**  
   https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

2. **MacQueen, J. (1967)** — *Some Methods for Classification and Analysis of Multivariate Observations.*

3. **Scikit-learn**  
   https://scikit-learn.org/

4. **Pandas**  
   https://pandas.pydata.org/

5. **Streamlit**  
   https://streamlit.io/


##  Tools & Technology 

| Category | Technologies |
|---|---|
| **Programming** | Python 3.10+ |
| **Data Analysis** | Pandas, NumPy |
| **Machine Learning** | Scikit-learn, K-Means |
| **Statistics** | SciPy |
| **Visualization & UI** | Matplotlib, Streamlit |
| **Development & Deployment** | Git, GitHub, Pytest, Docker |
