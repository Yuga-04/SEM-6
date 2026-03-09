## K-Means Clustering Algorithm with Example (15 Marks)

### 1. Introduction

K-Means clustering is an **unsupervised machine learning algorithm** used to group a dataset into **K clusters**. It divides the dataset into clusters such that data points in the same cluster are similar to each other and different from those in other clusters. The algorithm works iteratively by selecting centroids and assigning each data point to the nearest centroid based on distance. 

---

## 2. K-Means Clustering Algorithm

K-Means clustering is a **partition clustering algorithm** that divides the entire dataset into mutually exclusive clusters. The algorithm repeatedly adjusts the cluster centers until stable clusters are obtained. 

---

## 3. Steps of K-Means Algorithm

Given a dataset with **N entries** and **K clusters**, the algorithm works as follows:

1. Select **K random data points** from the dataset as the initial centroids.
2. Calculate the **distance between each data point and the centroids** using a distance metric such as Euclidean distance.
3. Assign each data point to the **cluster whose centroid is closest**.
4. Compute the **new centroid** by taking the mean of the data points in each cluster.
5. Repeat steps 2–4 until the centroids do not change and clusters become stable. 

---

# 4. Example of K-Means Clustering

Consider the following **6 data points**:

| Point | Coordinates |
| ----- | ----------- |
| A1    | (2,4)       |
| A2    | (3,5)       |
| A3    | (4,4)       |
| A4    | (8,7)       |
| A5    | (9,6)       |
| A6    | (10,8)      |

Let the number of clusters be **K = 2**.

---

## Step 1 – Select Initial Centroids

Choose two points as initial centroids:

Centroid 1 → **A1 (2,4)**
Centroid 2 → **A4 (8,7)**

---

## Step 2 – Assign Data Points to Nearest Centroid

Calculate distance between each point and centroid.

### Cluster 1

A1 (2,4)
A2 (3,5)
A3 (4,4)

### Cluster 2

A4 (8,7)
A5 (9,6)
A6 (10,8)

Points are assigned to the cluster with the **minimum distance from centroid**.

---

## Step 3 – Calculate New Centroids

### Cluster 1

Points: (2,4), (3,5), (4,4)

New centroid:

[
\left(\frac{2+3+4}{3}, \frac{4+5+4}{3}\right) = (3,4.33)
]

### Cluster 2

Points: (8,7), (9,6), (10,8)

New centroid:

[
\left(\frac{8+9+10}{3}, \frac{7+6+8}{3}\right) = (9,7)
]

---

## Step 4 – Check for Stability

Distances are calculated again using the new centroids. Since the points remain in the same clusters, the clusters are **stable**.

### Final Clusters

**Cluster 1:** A1, A2, A3

**Cluster 2:** A4, A5, A6

---

## 5. Applications of K-Means

K-Means clustering is used in many applications such as:

* Document classification
* Customer segmentation
* Image segmentation
* Fraud detection in banking and insurance 

---

## 6. Conclusion

K-Means clustering is a simple and efficient algorithm used to group similar data points into clusters. It repeatedly assigns data points to the nearest centroid and updates the centroid until the clusters stabilize. Because of its simplicity and scalability, it is widely used in data analysis and machine learning. 

