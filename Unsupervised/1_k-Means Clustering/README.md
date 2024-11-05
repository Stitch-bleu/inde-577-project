# K-Means Clustering

**K-Means Clustering** is an unsupervised machine learning algorithm used to partition a dataset into distinct groups, or "clusters," based on feature similarity. It aims to minimize the distance between data points within each cluster and maximize the distance between clusters, making it a popular choice for data segmentation tasks.

## Key Concepts in K-Means Clustering

1. **Centroids**:
   - Each cluster is represented by a **centroid**, which is the mean position of all points in the cluster.
   - The centroid serves as the "center" of a cluster, with all points assigned based on proximity to the nearest centroid.

2. **Distance Metrics**:
   - **Euclidean Distance**: Most commonly used distance metric in K-means, measuring straight-line distance between points
   - **Manhattan Distance**: An alternative metric, summing absolute differences between coordinates:

3. **Within-Cluster Sum of Squares (WCSS)**:
   - WCSS, also known as the **inertia**, is the sum of squared distances between each point and its assigned centroid.
   - Minimizing WCSS is the goal of the K-means algorithm, as it indicates that points are tightly grouped within clusters.

## K-Means Clustering Algorithm

The K-means algorithm follows an iterative process to refine clusters:

1. **Initialize**: Randomly select \( K \) initial centroids.
2. **Assign Clusters**: Assign each data point to the nearest centroid based on the chosen distance metric.
3. **Update Centroids**: Recalculate the centroid of each cluster as the mean of the points assigned to it.
4. **Repeat**: Repeat the assignment and update steps until centroids no longer change significantly or a maximum number of iterations is reached.

The goal is to find the optimal placement of centroids that minimizes the WCSS.

## Choosing the Optimal Number of Clusters

### Elbow Method
The **Elbow Method** helps to select the ideal number of clusters, \( K \), by plotting the WCSS for different values of \( K \). The optimal \( K \) is where the reduction in WCSS begins to level off, forming an "elbow" shape.

### Silhouette Score
The **Silhouette Score** measures how similar a data point is to its own cluster compared to other clusters. It ranges from -1 to 1:
- A score close to 1 indicates well-defined clusters.
- A score close to 0 suggests overlapping clusters.
- A negative score implies incorrect cluster assignment.

## Advantages and Limitations

### Advantages
- **Simplicity**: K-means is straightforward and easy to interpret.
- **Scalability**: Efficient for large datasets when \( K \) is relatively small.
- **Flexibility**: Works with various types of distance metrics beyond Euclidean.

### Limitations
- **Sensitivity to Initial Centroids**: Results can vary depending on initial centroid placement.
- **Assumes Spherical Clusters**: Performs best when clusters are circular and equally sized.
- **Fixed Number of Clusters**: Requires \( K \) to be defined beforehand, which may not be ideal in all scenarios.

## Common Use Cases

- **Customer Segmentation**: Grouping customers based on purchasing behavior, demographics, etc.
- **Image Compression**: Reducing the number of colors in an image by clustering similar pixel colors.
- **Anomaly Detection**: Identifying unusual patterns by assigning low-density clusters.

K-means clustering is a versatile tool for data exploration and segmentation, enabling insights into complex, unlabeled datasets.

