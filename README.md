# Product Matching on a Marketplace

This project aims to solve the problem of matching products on a large marketplace by developing an efficient product matching algorithm. The primary objective is to find the most relevant products from a database for each item in a query, evaluated using the accuracy@5 metric.

## Tech Stack
- **Programming Languages**: Python
- **Data Analysis and Visualization**: Pandas, NumPy, Matplotlib, Sweetviz
- **Data Scaling**: Scikit-learn (StandardScaler, RobustScaler)
- **Clustering**: KMeans
- **Nearest Neighbors**: NearestNeighbors
- **Similarity Search**: FAISS

## Algorithm
1. **Clustering**: Performed clustering on the database.
2. **Cluster Membership**: Determined the cluster membership for each product.
3. **Similarity Search**: Searched for the most similar products within the corresponding cluster.

## Summary
- **Data Preprocessing**: No missing values or duplicates found.
- **Sampling**: Created samples from the training dataset and the database to reduce runtime.
- **Samples Implementation**: Used both sklearn and FAISS libraries. FAISS demonstrated faster performance.
- **Full Dataset Implementation**: Tested Cell probe method with different quantizers: Flat index, HNSW, PQ. Best: IndexIVFFlat with 250 clusters and 8 search queries (accuracy@5 = 63.889).

## Conclusion
The project successfully achieved its goal. The developed model can efficiently find similar items in a large database, accurately identifying 3 out of 5 items, demonstrating its feasibility for large-scale product matching in a marketplace environment.

