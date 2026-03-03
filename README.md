# Flipkart Product Clustering & Outlier Detection 🛒🏷️

## Overview
This project focuses on market segmentation and anomaly detection using a Flipkart e-commerce dataset (80,000 products). By applying unsupervised learning, we identified distinct product categories based on pricing, discounts, and logistics.

## Key Methodology
* **Preprocessing**: Data cleaning, handling missing values (imputed `size` as "Unknown"), and feature scaling via `StandardScaler`.
* **Dimensionality Reduction**: Used **PCA** to explain 90% of variance and enable 3D cluster visualization.
* **Clustering Algorithms**: Implemented and compared **K-Means**, **DBSCAN**, **Gaussian Mixture Models (GMM)**, and **Hierarchical Clustering**.

## Market Segments (K-Means Profiles)
Based on our analysis ($k=4$), we identified the following segments:
* **Cluster 3 (Premium)**: High-end products with high prices and minimal discounts.
* **Cluster 1 (Promo)**: Products on deep sale with the highest discount percentages.
* **Cluster 2 (Standard - Heavy)**: Mid-range products with significantly higher shipping weights.
* **Cluster 0 (Standard - Light)**: Accessible, everyday products with low logistics impact.

## Model Comparison
| Algorithm | Silhouette Score | Insight |
| :--- | :--- | :--- |
| **GMM** | **0.2207** | **Best Performance**: Effectively handled overlapping data points. |
| **K-Means** | 0.0666 | Provided the most interpretable business segments. |
| **DBSCAN** | -0.1352 | Successfully isolated **1,699 outliers** (market anomalies). |

## Tech Stack
* **Analysis**: `Pandas`, `NumPy`, `Scikit-learn`
* **Visualization**: `Matplotlib`, `Seaborn`, `Plotly` (Interactive 3D plots)
* **Optimization**: `Kneed` (Automated Elbow Method detection)

## Conclusion
While K-Means provided a practical framework for business strategy, the **Gaussian Mixture Model (GMM)** proved to be the most mathematically accurate for this specific dataset. DBSCAN added critical value by identifying extreme outliers that do not follow standard market trends.

## Link to the dataset on Kaggle
[Flipkart Retail Product Dataset (Kaggle)](https://www.kaggle.com/datasets/rohiteng/flipkart-retail-product-dataset)
