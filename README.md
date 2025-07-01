

# Customer Segmentation Using K-Means Clustering & PCA

## Project Overview

This project performs customer segmentation on transactional and demographic data using unsupervised machine learning techniques. The goal is to group customers into meaningful clusters based on their purchasing behavior and other features, enabling targeted marketing and improved business strategies.

The main steps in this project include:

* Exploratory Data Analysis (EDA) to understand the dataset's characteristics
* Data preprocessing and encoding of categorical variables
* Feature selection based on variance
* Using K-Means clustering to identify customer segments
* Evaluating clustering performance using inertia and silhouette scores
* Visualizing cluster centers and customer segments using PCA

---

## Dataset

The dataset contains customer transactional and demographic data, including features such as:

* Customer Age Group
* Customer Gender
* Country
* Order Quantity
* Revenue, Profit, Unit Price, Cost, Unit Cost
* Date of transaction

*Note: Sensitive columns such as product details and location states were dropped for clustering.*

---
## 🔁 Workflow Summary  
1. Exploratory Data Analysis (EDA): We explored age group distribution (most customers were adults), gender distribution (slightly more males), order behavior (Canada and USA had highest average quantity ), and revenue trend by year (steady growth observed).  
2. Data Preprocessing: We converted date to datetime and extracted the year, dropped irrelevant fields (State, Product, Day, Month, etc.), label encoded gender (M=1, F=0), age group (Adults=0, Young Adults=1, Seniors=2, Youth=3), and country. Then we selected top 5 high-variance features for clustering: Revenue, Unit Price, Cost, Unit Cost, and Profit.  
3. Clustering Using KMeans: We applied KMeans clustering with different values of k from 2 to 12, and used inertia and silhouette score to evaluate them. The optimal number of clusters was found to be 3. We built the final model
4. PCA & Visualization: We applied PCA to reduce the 5 features to 2 principal components and visualized the clusters using a 2D scatter plot with Plotly, which confirmed clear separation among the segments.

   ## 💡 Business Value

This analysis enables businesses to:

* Tailor marketing campaigns to different customer types
* Predict customer behavior and preferences
* Identify underserved and high-potential segments
* Improve retention and reduce churn with targeted offers
* Optimize marketing spend and product development

## 🎯 Key Insights

Segment 0: Budget-conscious customers with low profit, cost, and revenue. Likely first-time or low-engagement buyers.  
Segment 1: Average spenders with balanced unit price, profit, and cost. Mid-tier customers who are responsive to standard marketing.  
Segment 2: High-value customers with very high profit, unit cost, and revenue. Ideal for loyalty programs and premium offers.

### 🔍 Cluster Interpretation and Recommendations

- **Cluster 0**: Shows minimal activity across all variables (Profit, Unit_Cost, Cost, Unit_Price, Revenue). This suggests a low-engagement or inactive customer segment, with values close to zero.  
- **Cluster 1**: Displays moderate activity. Profit and Unit_Price are around 1000–1500, Unit_Cost and Cost are slightly lower, and Revenue is around 2000. This cluster indicates balanced but moderate customer behavior with reasonable revenue generation.  
- **Cluster 2**: Exhibits the highest activity. Revenue peaks at approximately 6000, with Cost around 4000, Profit and Unit_Price around 2000, and Unit_Cost lower. This cluster represents the most profitable and active customer segment, driven by high revenue and manageable costs.

**✅ Recommendation:** Focus marketing and retention efforts on **Cluster 2** to maximize profitability, while exploring strategies to **activate or re-engage Cluster 0** customers. **Cluster 1** could benefit from targeted **upselling** to boost revenue further.

---
