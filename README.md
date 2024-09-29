# McDonald-s-Customer-Segmentation-Analysis
This repository contains a Python-based analysis for segmenting McDonald's customers using Principal Component Analysis (PCA) and K-Means clustering. The goal is to identify distinct customer segments based on various behavioral and demographic factors, enabling targeted marketing strategies and improved customer service.
# Introduction
Customer segmentation is a vital aspect of marketing strategy, allowing businesses to tailor their offerings to specific groups within their customer base. This analysis leverages machine learning techniques to segment McDonald's customers based on their responses to various survey questions and demographic information.
# Libraries and Tools
The analysis utilizes the following Python libraries:
Pandas: Data manipulation and analysis.
NumPy: Numerical operations.
Scikit-learn: Machine learning algorithms (PCA, K-Means, Label Encoding).
Matplotlib & Seaborn: Data visualization.
# Dataset
The dataset (mcdonalds.csv) contains survey responses and demographic information from McDonald's customers. The exact features include:
Binary Variables: First 11 columns with 'Yes'/'No' responses indicating various behaviors or preferences.
VisitFrequency: Categorical variable indicating how often a customer visits McDonald's.
Gender: Categorical variable indicating the customer's gender.
# Data Preprocessing
Encoding Categorical Variables
Machine learning algorithms require numerical input. Therefore, categorical variables are transformed into numerical formats:
Binary Encoding: The first 11 columns are mapped from 'Yes'/'No' to 1/0.
Label Encoding:
VisitFrequency is transformed using LabelEncoder, converting categorical labels to integers.
Gender is mapped directly from 'Female'/'Male' to 1/0.
# Feature Selection
The first 11 columns are selected as features (segmentation_vars) for segmentation analysis.
# Principal Component Analysis (PCA)
#Purpose
PCA is a dimensionality reduction technique that transforms high-dimensional data into a lower-dimensional space while preserving as much variance as possible. This simplifies the dataset, reduces computational complexity, and helps in visualizing the data.
#Implementation
Number of Components: Reduced to 2 principal components for easy visualization.
Explained Variance: Indicates how much information (variance) is captured by each principal component.
#Interpretation
Explained Variance Ratio: Shows the proportion of the dataset's variance captured by each principal component.
Cumulative Variance: Helps in understanding the total variance captured by the selected components.
# K-Means Clustering
#Purpose
K-Means is an unsupervised learning algorithm used to partition data into distinct clusters based on feature similarity. It minimizes the within-cluster sum of squares, ensuring that data points within the same cluster are as similar as possible.
#Implementation
Number of Clusters (k): Set to 4 based on prior knowledge or methods like the Elbow Method.
Random State: Ensures reproducibility of results.
#Interpretation
Each data point is assigned to one of the four clusters, representing a distinct customer segment. These segments can be analyzed to understand differing customer behaviors and preferences.
# Visualization
A scatter plot visualizes the customer segments in the reduced 2D PCA space, providing an intuitive understanding of the clustering.
#Interpretation
Axes: Represent the two principal components capturing the most variance in the data.
Clusters: Different colors indicate distinct customer segments.
Insights: Helps in identifying patterns or relationships between segments, such as preferences or behaviors common within a segment.
# Conclusion
This analysis demonstrates a systematic approach to customer segmentation using PCA for dimensionality reduction and K-Means for clustering. By identifying distinct customer segments, McDonald's can tailor marketing strategies, improve customer satisfaction, and optimize resource allocation.
