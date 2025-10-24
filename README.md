# 🎯 K-Means Clustering from Scratch using Python

🚀 **A simple and intuitive implementation of the K-Means Clustering algorithm built entirely from scratch using NumPy and Matplotlib.**  
This project demonstrates how K-Means works — from random centroid initialization to iterative assignment and update steps.

---

## 🧠 What is K-Means?

**K-Means** is an unsupervised machine learning algorithm used for clustering data into *k* distinct groups.  
It works by repeatedly assigning points to the nearest centroid and updating those centroids until convergence.  
💡 This project helps visualize how centroids move and clusters form over iterations.

---

## 🧩 Project Structure

├── kmeans_from_scratch.py # Main Python script
├── README.md # Documentation file

yaml
Copy code

---

## ⚙️ Libraries Used

- 🧮 **NumPy** — for numerical and vectorized operations  
- 📊 **Matplotlib** — for data visualization  
- 🤖 **Scikit-learn** — for generating synthetic datasets (make_blobs)

---

## 🏗️ Implementation Steps

### 1️⃣ Create Synthetic Dataset
Using `make_blobs()` to generate data points for clustering.

### 2️⃣ Initialize Random Centroids
Randomly place `k` centroids in the feature space.

### 3️⃣ Define Distance Function
Compute Euclidean distance between data points and centroids.

### 4️⃣ Assign and Update
Assign points to the nearest centroid and update each centroid to the mean of its assigned points.

### 5️⃣ Iterate Until Convergence
Repeat assignment and update steps multiple times to refine clusters.

### 6️⃣ Visualize the Results
Plot the dataset, initial random centroids, and final clusters 🎨

---

## 💻 Example Usage

```python
# Number of clusters
k = 3

# Run assignment and update steps
for _ in range(5):
    clusters = assign_clusters(X, clusters)
    clusters = update_clusters(X, clusters)

# Predict final clusters
pred = pred_cluster(X, clusters)

# Plot final clusters
plt.scatter(X[:, 0], X[:, 1], c=pred)
for i in clusters:
    center = clusters[i]['center']
    plt.scatter(center[0], center[1], marker='^', c='red', s=100)
plt.title("Final K-Means Clusters")
plt.show()
