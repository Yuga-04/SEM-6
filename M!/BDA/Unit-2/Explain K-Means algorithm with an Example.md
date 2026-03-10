## K-Means Clustering Algorithm with Example (Reduced Iteration)

### 1. Introduction

K-Means clustering is an **unsupervised machine learning algorithm** used to divide a dataset into **K clusters** based on similarity between data points. The algorithm groups similar data points together so that objects in the same cluster are more similar to each other than to those in other clusters. 

The algorithm repeatedly assigns points to the nearest centroid and recalculates the centroid until the clusters become stable.

---

# 2. Steps of K-Means Algorithm

1. Select **K initial centroids** randomly from the dataset.
2. Calculate the **distance between each data point and the centroids**.
3. Assign each point to the **nearest centroid**.
4. Recalculate the **new centroid by taking the mean of all points in the cluster**.
5. Repeat the process until clusters become stable. 

---

# 3. Example of K-Means Clustering

Consider the following **8 data points**:

| Point | Coordinates |
| ----- | ----------- |
| A1    | (2,8)       |
| A2    | (3,7)       |
| A3    | (4,9)       |
| A4    | (7,5)       |
| A5    | (8,6)       |
| A6    | (9,5)       |
| A7    | (5,2)       |
| A8    | (6,3)       |

Let the number of clusters be **K = 2**.

---

# 4. Step 1 – Select Initial Centroids

Choose two random centroids:

Centroid 1 → **A1 (2,8)**
Centroid 2 → **A5 (8,6)**

---

# 5. Step 2 – Assign Points to Clusters

Compute the distance of each point from the two centroids and assign the point to the nearest centroid.

After calculating distances:

### Cluster 1

A1 (2,8)
A2 (3,7)
A3 (4,9)

### Cluster 2

A4 (7,5)
A5 (8,6)
A6 (9,5)
A7 (5,2)
A8 (6,3)

---

# 6. Step 3 – Calculate New Centroids

Compute the mean of each cluster.

### Cluster 1

Points:
(2,8), (3,7), (4,9)

New centroid:


<img width="350" height="113" alt="image" src="https://github.com/user-attachments/assets/b8c3cee3-410f-4311-82b6-d1e2bae17fe7" />



### Cluster 2

Points:
(7,5), (8,6), (9,5), (5,2), (6,3)

New centroid:



<img width="541" height="113" alt="image" src="https://github.com/user-attachments/assets/e155919f-f7ab-42fe-af10-2aa9798a570c" />



---

# 7. Final Clusters

After the next reassignment check, the clusters remain the same, so the algorithm **converges**.

### Final Cluster 1

A1, A2, A3

### Final Cluster 2

A4, A5, A6, A7, A8

---

# 8. Conclusion

K-Means clustering groups data points based on distance from centroids. The algorithm iteratively updates centroids until clusters stabilize. It is widely used for **data grouping, pattern recognition, and customer segmentation**. 

---

✅ If you want, I can also give you a **very clean exam-ready format (with diagram layout your professor expects)** so you can easily score full **15 marks**.
