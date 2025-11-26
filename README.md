# 🛒 Customer Segmentation: A Strategic Recovery Plan
[![Kaggle](https://img.shields.io/badge/Kaggle-View_Notebook-blue?logo=kaggle&logoColor=white)](https://www.kaggle.com/code/alok158/alok158-customer-retention-analysis-using-rfm-k-me?scriptVersionId=281874381)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Strategy-Ready-green)

## 💡 The Problem
In e-commerce, **"one-size-fits-all" marketing is a waste of money.** Sending a generic discount to a loyal customer eats into margins, while sending a "Welcome Back" email to someone who just bought yesterday is annoying.

**The Goal:** Use data (not intuition) to group customers by behavior and assign a specific marketing strategy to each group.

## 🔍 The Solution: RFM & K-Means
I analyzed **390,000+ transactions** from a UK-based retailer. I engineered three key features for every single customer:
1.  **Recency:** How long has it been since they bought something?
2.  **Frequency:** How often do they buy?
3.  **Monetary:** How much do they spend?

Using **K-Means Clustering**, I let the data reveal the natural groupings of customers.

---

## 📊 The Results (Visualized)

### 1. The "Snake Plot" (Market DNA)
*This chart is the fingerprint of our customer base. It shows how each group differs from the average.*

![Snake Plot](https://github.com/user-attachments/assets/5605d658-63a2-44a1-8020-c3dfe44940e9)

* **The Orange Line (Champions):** Look how high it spikes on "Frequency" and "Monetary." These people are outliers in the best way.
* **The Blue Line (Lost):** It crashes at "Recency" (meaning the value is high, which in RFM is bad—lots of days since last purchase).

### 2. The Landscape (Recency vs. Monetary)
*Here we see exactly where our revenue comes from.*

![Scatter Plot](https://github.com/user-attachments/assets/8583fb6c-3bc4-417d-9665-de33bdf5507b)

* **Top Left (Orange):** The "Champions." They buy recently (Low Recency) and spend huge amounts.
* **Bottom Right (Red):** The "Lost." They haven't bought in ages, and when they did, they didn't spend much.

---

## 🎯 Strategic Action Plan
Based on the 4 clusters identified, here is the recommended strategy:

| Customer Segment | Who are they? | The Numbers | **My Recommendation** |
| :--- | :--- | :--- | :--- |
| **🏆 Champions** | The VIPs. They buy often and spend the most. | **868 Users**<br>Avg Spend: £7,042 | **Don't discount.** Give them early access to new products or a dedicated support line. Make them feel special. |
| **🌱 Potential Loyalists** | Recent buyers, but low spenders. | **1,657 Users**<br>Avg Spend: £612 | **Upsell.** Recommend higher-margin products. They trust us (high recency), now we need to increase their basket size. |
| **⚠️ At Risk** | Big spenders who haven't visited in 3+ months. | **436 Users**<br>Avg Spend: £1,518 | **Urgent Action.** Send personalized "We Miss You" coupons *immediately*. If we lose these 436 people, we lose significant revenue. |
| **💤 Lost / Low Value** | One-time shoppers from long ago. | **1,377 Users**<br>Avg Spend: £298 | **Ignore.** Do not waste marketing budget here. Focus resources on the "At Risk" group instead. |

## 🛠️ How I Built This
* **Data Cleaning:** Handled negative quantities (returns) and missing IDs.
* **Preprocessing:** Used **Log Transformation** to un-skew the data (Pareto Principle applies here: 80% of sales come from 20% of users).
* **Modeling:** Used the **Elbow Method** to determine that *k=4* was the mathematically optimal number of clusters.

## 🚀 Run it Yourself
1. Clone the repo.
2. Install requirements: `pip install -r requirements.txt`
3. Launch the Jupyter Notebook.

---
*Created by [Your Name]*
