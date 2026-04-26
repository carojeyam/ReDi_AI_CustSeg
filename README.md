# ReDI-AI: Customer Segmentation E-Commerce Platform

Customer segmentation and personalization platform that uses **K-Means clustering** to classify customers into behavioral segments and deliver personalized shopping experiences.

---

## 🎯 Project Overview

This project demonstrates the integration of **Machine Learning + Web Development**:

- 🤖 **Machine Learning**: K-Means customer segmentation (3 behavioral clusters)
- 📊 **Data Analysis**: Customer behavior analysis using Python (pandas, scikit-learn, matplotlib)

----

## ✨ Key Features

- 👥 **Customer Segmentation** – Real-time classification based on purchase behavior
- 🎯 **Personalization** – Segment-specific recommendations and strategies
- 🛒

 ## 📊 Customer Segments

### 🟡 Cluster 0: Low Web Engagement (22.3%)
- **Profile**: Low wine preference, balanced product mix, minimal web activity  
- **Behavior**: Few web purchases, moderate spenders  
- **Strategy**: Improve UX, encourage first purchases, offer entry discounts  

---

### 🟣 Cluster 1: High-Value Web Enthusiast (28.7%)
- **Profile**: Premium wine lovers, frequent web users, highest spenders  
- **Behavior**: High engagement, strong spending intensity  
- **Strategy**: Upsell premium products, loyalty rewards, exclusive subscriptions  

---

### 🔵 Cluster 2: Deal-Seeker (49.0%)
- **Profile**: Price-sensitive, moderate spenders  
- **Behavior**: Balanced product mix, reacts to discounts  
- **Strategy**: Flash sales, coupons, bundle offers  

---

## 🧠 Machine Learning Pipeline

### Feature Engineering (9 Features)
- `spend_intensity = log(total_spend + 1)`
- Product category shares:
  - Wines, Fruits, Fish, Sweets
- Web behavior features:
  - Web purchases
  - Web visits per month
  - Web share
  - Deal purchases

---

### Scaling Method
**RobustScaler (median/IQR based)**


- Resistant to outliers
- Better for real-world noisy data

---

### Classification Logic

1. Compute feature vector from cart
2. Normalize using trained scaler
3. Compute Euclidean distance to cluster centroids
4. Assign nearest cluster

---

## 📈 Model Details

- **Algorithm**: K-Means Clustering
- **Clusters (k)**: 3
- **Dataset Size**: 2,240 customers
- **Features**: 9 engineered behavioral features
- **Silhouette Score**: 0.210 (moderate separation)

---

## 📓 Notebook Insights

The Jupyter notebook includes:

### 📂 Data Exploration
- Dataset overview (29 features)
- Missing value analysis
- Outlier detection

### 🧪 Feature Engineering
- RFM (Recency, Frequency, Monetary) analysis
- Product category segmentation
- Web behavior metrics

### 🤖 Clustering
- K selection (k=2 to k=10)
- PCA-based visualization
- Cluster profiling

### 📊 Model Evaluation
- K-Means vs Gaussian Mixture Model
- Adjusted Rand Index comparison
- Final model selection

### 📦 Export
- Cluster centroids
- Scaler parameters
- JavaScript-ready model export

---

## 🧪 Testing the Application

### 1. Browse Products
- Navigate categories: Fish, Fruits, Meat, Gold, Wine, Sweets
- View product listings

### 2. Add to Cart
- Click **"Add to Cart"**
- Cart updates in real time
- Data persists on refresh

### 3. View Cart
- Open cart page
- Modify quantities or remove items

### 4. Checkout & Segmentation
- Click **Checkout**
- View:
  - Order summary
  - Predicted customer segment
  - Personalized strategy

### 5. Order Confirmation
- Confirm order
- Cart resets
- Redirect to homepage

---

## 🧪 Sample Test Scenarios

### 🟡 Cluster 0 (Low Engagement)
- Low total spend ($20–$50)
- Mixed product categories
- Small cart size

### 🟣 Cluster 1 (High Value)
- High wine purchases ($150+)
- Wine-heavy cart (>75%)
- Premium items

### 🔵 Cluster 2 (Deal-Seeker)
- Moderate spend ($50–150)
- Balanced categories
- Discount-driven purchases

---

## 🔄 Project Improvements

### Code Quality Enhancements
- Separation of concerns
- Modular JavaScript architecture
- Reusable ML inference pipeline

---

## 👨‍💻 Team

**ReDI Team Project**  
GROUP PROJECT - ReDI AI learning program 🚀

---

## 📌 Summary

This project demonstrates how machine learning can be embedded directly into a web application to enable **real-time customer segmentation and personalization** without backend inference.

### Scaling Method
**RobustScaler (median/IQR based)**
