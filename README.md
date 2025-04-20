<H1> K-Means Clustering Algorithm in Machine Learning </H1>

The <b>K-Means Clustering algorithm</b> is an unsupervised machine learning technique used for clustering data into groups based on their similarities. It is particularly useful when you want to identify patterns or groupings in a dataset without predefined labels. Below, I'll explain how K-Means works and how it can be applied to the <b>Iris flower dataset</b>.


<h2> How K-Means Works </h2>
1. <b> Initialization </b>:
   - Choose the number of clusters, $K$, you want to create.
   - Randomly initialize $K$ centroids (points that represent the center of each cluster).

2. <b> Assignment Step </b>:
   - Assign each data point to the nearest centroid based on the Euclidean distance.

3. <b> Update Step </b>:
   - Recalculate the centroids by taking the mean of all data points assigned to each cluster.

4. <b> Repeat </b>:
   - Repeat the assignment and update steps until the centroids no longer change significantly, or a maximum number of iterations is reached.

The algorithm minimizes the <b>intra-cluster variance</b>, which is the sum of squared distances between data points and their respective cluster centroids.


<h2> Iris Dataset Overview </h2>
The <b>Iris dataset</b> is a classic dataset in machine learning, containing 150 samples of iris flowers. Each sample has four features:
- Sepal length
- Sepal width
- Petal length
- Petal width

The dataset is divided into three species of iris flowers: Setosa, Versicolor, and Virginica. However, in clustering tasks like K-Means, the species labels are ignored because it is an <b>unsupervised learning algorithm</b>.

<b> Applying K-Means to the Iris Dataset </b>
1. <b> Preprocessing </b>:
   - Load the Iris dataset.
   - Normalize the features (optional but recommended) to ensure that all features contribute equally to the distance calculations.

2. <b> Choosing K </b>:
   - Use methods like the <b>Elbow Method</b> to determine the optimal number of clusters, $K$. For the Iris dataset, $K=3$ is often chosen because there are three species of flowers.

3. <b> Clustering </b>:
   - Apply the K-Means algorithm to group the data into three clusters.
   - Each cluster will ideally correspond to one species of iris flower.

4. <b> Evaluation </b>:
   - Compare the clustering results with the actual species labels, if available, to evaluate the performance. Metrics like <b> Adjusted Rand Index (ARI)</b> and <b>Silhouette Score</b> can be used.
  
<h2> Elbow Plot </h2>
When applying K-means clustering to the Iris dataset, the <b>inertial cluster (or elbow) plot</b> helps identify the natural grouping of the data. Since the Iris dataset has three species of flowers, the elbow plot often shows a noticeable elbow at "K=3," aligning with the dataset's inherent structure. This plot is a key step to ensure that the clustering algorithm is effectively capturing the underlying patterns in the data.  

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Elbow Method for Optimal K</title>
    <style>
        .scaled-image {
            transform: scale(0.7); /* Scale factor of 1.5 */
            /* Optional: Set the transform origin if needed */
            transform-origin: top left; 
        }
    </style>
</head>
<body>
    <h1>Elbow Method for Optimal K</h1>
    <a href='https://postimages.org/' target='_blank'><img src='https://i.postimg.cc/kggCNtzf/inertia-cluster-no.png' border='0' alt='inertia-cluster-no'/></a>
    <!--img src="./inertia_cluster_no.png" alt="Elbow Plot" class="scaled-image"-->
</body>


 <h2> K-means Clustering Iris Dataset K=3 </h2>
 When applying the K-means clustering algorithm with K=3, the algorithm effectively groups the data into distinct clusters that correspond to these species, demonstrating clear separations based on their morphological features.
 
<!--head>
    <!--meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>K=3 Results</title>
    <style>
        .scaled-image {
            transform: scale(0.7); /* Scale factor of 1.5 */
            /* Optional: Set the transform origin if needed */
            transform-origin: top left; 
        }
</style>
</head-->
<body>
    <h1>K=3 Results</h1>
    <a href='https://postimg.cc/DmzNG10G' target='_blank'><img src='https://i.postimg.cc/FFbX2ZQT/k-means-clustering-iris-dataset-k3-results.png' border='0' alt='k-means-clustering-iris-dataset-k3-results' style="width: 70%; height: auto;"></a>
    <!--img src="./k-means_clustering_iris_dataset_k3_results.png" alt="K=3 Results" class="scaled-image"-->
</body>
 
