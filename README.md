# Mall-Customers-Dataset

# Mall Customer Segmentation – AVM Müşteri Segmentasyonu

## 📌 Project Overview
This project applies clustering (KMeans) to segment mall customers based on **Annual Income (k$)** and **Spending Score (1–100)**.  
The goal is to help mall management design targeted marketing campaigns.

Bu proje, AVM müşterilerini **Yıllık Gelir (k$)** ve **Harcama Skoru (1–100)** üzerinden **KMeans kümeleme** ile segmente eder.  
Amaç, AVM yönetiminin pazarlama kampanyalarını daha verimli tasarlamasına yardımcı olmaktır.

---

## 🗂 Workflow Steps

### Step 0: Warnings Off
- Suppress warnings for clean notebook output.

### Step 1: Project Setup & Context
- Import libraries (pandas, numpy, seaborn, matplotlib, sklearn).
- Define project goal.

### Step 2: Load Data & Inspect
- Load `Mall_Customers.csv`.
- Inspect shape, info, missing values.

### Step 3: Exploratory Data Analysis (EDA)
- Distribution plots for Income & Spending Score.
- Scatter plot: Income vs Spending Score.

### Step 4: Preprocessing
- Select features: Annual Income, Spending Score.
- Scale features with `StandardScaler`.

### Step 5: Elbow Method
- Compute inertia for k=2..10.
- Plot inertia vs k to find elbow.

### Step 6: Silhouette Score
- Evaluate cluster separation quality.
- Select best k.

### Step 7: Final KMeans & Visualization
- Fit KMeans with best k.
- Visualize clusters in 2D scatter plot.

### Step 8: Segment Profiles & Business Actions
- Profile clusters by mean Income/Spending.
- Suggest marketing strategies:
  - High Income, Low Spending → loyalty perks
  - Mid Income, High Spending → seasonal promos
  - Low Income, Low Spending → discounts
  - High Income, High Spending → VIP campaigns

### Step 9: Save Outputs
- Export segmented dataset (`mall_customers_segmented.csv`).
- Export cluster summary (`cluster_summary.csv`).

---

## 📊 Results
- **Best k:** Determined via silhouette score (commonly 5).
- **Cluster Profiles:** Clear differentiation between income/spending groups.
- **Business Value:** Enables targeted campaigns, efficient budget allocation.

---

## ⚙️ Tech Stack
- Python 3.x
- pandas, numpy
- scikit-learn
- seaborn, matplotlib

---

## 🚀 How to Run
```bash
# Clone repository
git clone https://github.com/yourusername/mall-customer-segmentation.git
cd mall-customer-segmentation

# Install dependencies
pip install -r requirements.txt

# Run notebook
jupyter notebook Mall_Customer_Segmentation.ipynb
