# Bangladesh Crime Clustering

An exploratory data analysis and unsupervised learning project that analyzes **crime, demographic, environmental, and infrastructure characteristics across regions in Bangladesh**.

The project applies data cleaning, exploratory analysis, K-Means clustering, model tuning, PCA visualization, and cluster profiling.

## Project Overview

Understanding regional characteristics can help reveal patterns in crime distribution and differences in population, infrastructure, and social conditions.

This project groups regions with similar characteristics using **K-Means clustering** and examines how crime types are distributed across the resulting clusters.

## Objectives

This project aims to:

* Perform exploratory data analysis on the crime dataset.
* Identify and handle data quality issues and anomalies.
* Prepare numerical and categorical variables for analysis.
* Determine an appropriate number of clusters.
* Apply K-Means clustering.
* Visualize clusters using PCA.
* Profile the characteristics of each cluster.
* Examine crime distributions across clusters.

## Data Cleaning

Several data quality issues were identified and addressed, including:

* Removal of unnecessary index columns.
* Standardization of categorical text.
* Treatment of extreme population-density values.
* Imputation of missing incident months.
* Correction of negative police station values.
* Imputation of missing literacy rates by division.
* Handling of missing categorical values.

The cleaned dataset was saved as:

```text
Cleaned_Bangladesh_Crime_Dataset.csv
```

## Clustering Method

The following variables were used for clustering:

* Precipitation
* Visibility
* Heat index
* Total population
* Gender ratio
* Average household size
* Population density
* Literacy rate
* Religious institutions
* Playgrounds
* Parks
* Police stations
* Schools
* Colleges

Before clustering, the numerical features were standardized using **StandardScaler**.

## Choosing the Number of Clusters

Two evaluation approaches were used:

### Elbow Method

The Elbow Method was used to examine the relationship between the number of clusters and within-cluster inertia.

### Silhouette Score

Silhouette Score was used to evaluate the separation and compactness of the clusters.

Based on the analysis, **K = 2** was selected for the final K-Means model.

## Cluster Visualization

Principal Component Analysis (PCA) was used to reduce the standardized feature space into two dimensions for visualization.

The resulting visualization provides a two-dimensional representation of the two clusters.

## Cluster Profile

### Cluster 0

Cluster 0 generally represents areas with:

* Relatively smaller populations.
* Low to moderate population density.
* Lower literacy rates.
* Smaller household sizes.
* Fewer public facilities such as schools, colleges, parks, and police stations.

Crime types such as **kidnap, bodyfound, and murder** were relatively prominent in this cluster.

### Cluster 1

Cluster 1 generally represents areas with:

* Higher population.
* Higher population density.
* Larger household sizes.
* Higher literacy rates.
* More developed public infrastructure.

Crime types such as **bodyfound and robbery** were relatively prominent in this cluster.

These profiles describe patterns observed in the analyzed dataset and should not be interpreted as causal explanations for crime.

## Key Insights

The analysis demonstrates that regional crime-related data can be grouped according to combinations of:

* Population characteristics
* Social conditions
* Environmental factors
* Public infrastructure

The clustering results provide a way to explore similarities between regions rather than evaluating regions individually.
