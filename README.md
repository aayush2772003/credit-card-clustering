# Credit Card Customer Segmentation

## Project Overview

This project focuses on understanding customer behavior through their credit card transactional data. The goal is to segment customers into distinct clusters based on their spending patterns. By identifying these patterns, financial institutions like banks can create personalized marketing strategies, enhance user engagement, and take proactive measures to prevent defaults.

## Objectives

- Segment customers into clusters based on credit card purchase details.
- Identify the spending patterns of customers and their correlation with balance, cash paid, installments taken, and other factors.
- Compare the performance of different clustering algorithms on the given dataset.

## Dataset

The dataset used for this project includes spending patterns of approximately 9000 credit card holders over a period of 6 months. It contains 18 behavioral variables such as:

- BALANCE
- PURCHASES
- ONEOFF PURCHASES
- INSTALLMENTS PURCHASES
- CASH ADVANCE
- PURCHASES FREQUENCY
- CASH ADVANCE FREQUENCY
- CREDIT LIMIT
- PAYMENTS
- MINIMUM PAYMENTS
- PRCFULLPAYMENT
- TENURE

## Algorithms Used

1. **K-Means Clustering**
   - Standard Euclidean Distance
   - Polynomial Kernel
   - Gaussian Kernel
   - Tanh Kernel

2. **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**

3. **Clustering Using Large Language Models**
   - Sentence transformer library for LLM embeddings

4. **Agglomerative Hierarchical Clustering**

## Methodology

1. **Data Preprocessing**
   - Removal of nominal data
   - Handling missing values using median filling
   - Outlier detection and removal using the IQR method
   - Standardization of continuous features

2. **Evaluation Metrics**
   - Silhouette Score
   - Within-Cluster Sum of Squares (WCSS)

3. **Experimental Setup**
   - Applied multiple clustering algorithms to the preprocessed dataset.
   - Compared the performance of different algorithms using various metrics.

## Results

### K-Means Clustering
- **Polynomial Kernel** performed the best with the highest Silhouette Score of 0.43 for 3 clusters.
- **Euclidean Distance** and **Gaussian Kernel** also formed meaningful clusters.
- **Tanh Kernel** did not perform well due to outliers.

### Hierarchical Clustering
- Identified 3 optimal clusters with a Silhouette Score of 0.37.
- The dendrogram helped visualize cluster composition and hierarchical relationships.

### LLM-Based Clustering
- **Paraphrase-MiniLM-L6-v2** model performed the best with a Silhouette Score of 0.375 for 4 clusters.
- Demonstrated the potential of LLM embeddings in capturing subtle data patterns.

### DBSCAN
- Performed the worst with a Silhouette Score of 0.15.
- Struggled with high-dimensional data and density variation.

## Conclusion

This research highlights the importance of selecting appropriate clustering techniques based on data characteristics and analysis objectives. The K-Means algorithm with Polynomial Kernel provided the best results for this dataset. However, there is significant potential for improvement in LLM-based clustering as advancements in language models continue. Future work can explore new prompting techniques and more sophisticated models for better performance.

## Keywords

- Clustering
- Customer Segmentation
- Large Language Models

## References

1. I. Karo, 'Segmentation of Credit Card Customers Based on Their Credit Card Usage Behavior using The K-Means Algorithm', Journal of Software Engineering, Information and Communication Technology (SEICT), vol. 2, pp. 55–64, 02 2022.
2. S. Tripathi, A. Bhardwaj, and P. Eswaran, 'Approaches to Clustering in Customer Segmentation', International Journal of Engineering & Technology, vol. 7, p. 802, 07 2018.
3. A. Petukhova, J. P. Matos-Carvalho, and N. Fachada, 'Text clustering with LLM embeddings', arXiv [cs.CL], 2024.
4. D. Deng, 'DBSCAN Clustering Algorithm Based on Density', in 2020 7th International Forum on Electrical Engineering and Automation (IFEEA), 2020, pp. 949–953.
5. I. Davidson and S. Ravi, 'Agglomerative Hierarchical Clustering with Constraints: Theoretical and Empirical Results', 11 2005, pp. 59–7.
