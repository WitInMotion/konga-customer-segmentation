#  Customer Segmentation using K-Means Clustering

##  Overview
This project applies **unsupervised machine learning** to segment customers based on purchasing behavior using Konga e-commerce transaction data.

The goal is to uncover meaningful customer groups that can support targeted marketing, improve customer retention, and drive business growth.



##  Objectives
- Perform exploratory data analysis (EDA)
- Engineer meaningful customer-level features
- Apply clustering algorithms (K-Means & DBSCAN)
- Evaluate clustering performance using metrics
- Optimize clustering using PCA
- Generate actionable business insights



##  Tools & Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn



##  Dataset
The dataset contains transactional data including:
- Customer ID
- Order ID
- Product category
- Quantity purchased
- Unit price
- Total transaction value
- Order date
- City



##  Data Cleaning & EDA
- The dataset was checked for missing values — none were found.
- Orders were analyzed by city and category, revealing higher activity in major urban areas.
- A time-based analysis showed fluctuations in monthly orders, indicating possible seasonal trends.



##  Feature Engineering
Customer-level features were created to capture behavior:

- **Order Count** → number of purchases  
- **Total Quantity** → total items purchased  
- **Total Spent** → total revenue per customer  
- **Recency** → days since last purchase (time-based feature)  
- **Average Order Value** → average spend per order (ratio feature)  
- **Orders per Month** → purchase frequency  



##  Feature Scaling
StandardScaler was applied to normalize the dataset, ensuring all features contribute equally during clustering.



##  Model Selection

### Elbow Method
- Used to determine optimal number of clusters  
- Suggested **K = 3**

### Silhouette Score
- Evaluated cluster quality  
- Confirmed **K = 3** as optimal  



##  Models Used

### 1. K-Means Clustering
- Segmented customers into 3 groups  
- Initial silhouette score: **0.42**

### 2. DBSCAN
- Density-based clustering algorithm  
- Identified a large number of noise points  
- Produced weaker clustering performance  



##  PCA Optimization
- Reduced dimensionality to 2 components  
- Retained over 85% of variance  
- Improved silhouette score from **0.42 → 0.54**



##  Customer Segments

###  High-Value Customers
- High spending  
- Frequent purchases  
- Recently active  

###  Mid-Value Customers
- Moderate engagement  
- Growth potential  

###  Low-Value Customers
- Low spending  
- Infrequent purchases  
- Less recent activity  



##  Key Results

- Optimal clusters: **3**
- Initial silhouette score: **0.42**
- PCA improved score: **0.54**
- DBSCAN performance: Poor (high noise detected)



##  Business Insights
- High-value customers should be targeted with loyalty programs  
- Mid-value customers can be converted through upselling strategies  
- Low-value customers can be re-engaged with promotions and discounts  



##  Limitations
- Analysis is based only on transactional data  
- No demographic or behavioral data included  



##  Conclusion
K-Means clustering, enhanced with PCA, successfully identified meaningful customer segments. These insights can help businesses make data-driven decisions and improve customer targeting strategies.




