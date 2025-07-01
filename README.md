# 🧠 Customer Segmentation Using K-Means & PCA

This project aims to group customers into meaningful segments based on their age, gender, location, and purchasing behavior using machine learning techniques. Customer segmentation helps businesses personalize marketing strategies, increase sales, and improve customer experience.

---

## 📁 Dataset Overview

The dataset contains transactional and demographic information of customers, including:

- **Customer Age**, **Age Group**
- **Gender**
- **Country**
- **Order Quantity**
- **Unit Price**, **Revenue**, **Cost**, **Profit**
- **Product Category and Sub-category**

The data was loaded from a local CSV file:  
`Customer_Segmentation_py.csv`

---

## 🔁 Workflow Summary

### 1. 🔍 Exploratory Data Analysis (EDA)
- **Age Distribution**: Most customers are young adults.
- **Gender Distribution**: Slightly higher number of female customers.
- **Country Analysis**: Certain countries like the United States and France generate more orders.
- **Revenue Insights**: Revenue patterns vary by gender and country.

### 2. 🧹 Data Preprocessing
- **Label Encoding** of categorical variables like Gender, Age Group, and Country.
- **Feature Scaling** using StandardScaler.
- **Dimensionality Reduction** using PCA to project the data into 2D for easier clustering and visualization.

### 3. 📊 Clustering Using KMeans
- Applied KMeans clustering with different `k` values.
- **Silhouette Score** was used to choose the optimal number of clusters.
- Cluster visualization was done after applying PCA.

### 4. 📌 Final Model
- Final model segmented the customer base into meaningful groups.
- Used visualizations (scatter plots, bar charts) to interpret each customer cluster.

---

## 🎯 Key Insights

- **Segment 1**: Young adults who order frequently but purchase low-cost items. Ideal for upselling and product bundle offers.
- **Segment 2**: Older customers with high average revenue per order. They respond well to loyalty programs.
- **Segment 3**: Customers from specific countries (e.g., US, UK) tend to have higher purchasing power. Consider localized promotions.
- **Segment 4**: Some clusters showed lower engagement — these users may need reactivation strategies like discounts or email campaigns.
- **Gender-based Patterns**: Revenue and product interests vary by gender, enabling more personalized product recommendations.

---

## 📌 Technologies Used

- **Python** (Jupyter Notebook)
- `pandas`, `numpy` – Data wrangling
- `matplotlib`, `seaborn`, `plotly` – Visualizations
- `scikit-learn` – Label encoding, scaling, PCA, KMeans, evaluation

---

## 💡 Business Value

This analysis enables businesses to:
- Tailor marketing campaigns to specific customer types
- Predict customer behavior more accurately
- Identify underserved segments
- Increase ROI through customer-targeted strategies

---

