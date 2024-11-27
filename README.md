# K-Nearest Neighbors Variants: Performance Analysis and Misclassification Study

## Table of Contents
- [Introduction](#introduction)
- [Assumptions](#assumptions)
- [Network Model](#network-model)
- [Attributes and Parameters](#attributes-and-parameters)
- [Simulation Algorithm](#simulation-algorithm)
  - [Performance Analysis](#performance-analysis)
  - [Misclassification Analysis](#misclassification-analysis)
- [Simulation Analysis](#simulation-analysis)

## Introduction
This project explores two critical aspects of K-Nearest Neighbors (KNN) algorithms. The first part focuses on the performance analysis of different KNN variants, including Naive KNN, Locality-Sensitive Hashing (LSH), and KD-Tree. The aim is to analyze their performance in terms of training time, testing time, and memory usage across different dataset sizes and dimensions. The second part investigates misclassification in 2D data, highlighting how the assumptions made by these models can lead to incorrect predictions.

## Assumptions
- The dataset is randomly generated using a normal distribution.
- The number of neighbors \( K \) is fixed at 10 for all models during testing.
- The performance metrics are evaluated under identical conditions for fair comparison.

## Network Model
The project utilizes three different KNN models:
1. **Naive KNN**: A straightforward implementation that computes distances from the query point to all training points.
2. **Locality-Sensitive Hashing (LSH)**: A hashing-based approach that reduces the dimensionality of the data, allowing for faster nearest neighbor searches.
3. **KD-Tree**: A tree-based data structure that partitions the space into regions, optimizing search times for high-dimensional data.

## Attributes and Parameters
### Attributes:
- `data`: Input dataset for training or querying.
- `query`: The point for which nearest neighbors are to be found.
- `k`: Number of nearest neighbors to retrieve.

### Parameters:
- \( N \): Number of samples in the dataset.
- \( D \): Number of dimensions in the dataset.

## Simulation Algorithm
The simulation consists of two main parts:

### Performance Analysis:
1. Generate datasets with varying sizes \( N \) and dimensions \( D \).
2. Fit each KNN model to the training data.
3. Measure training time, testing time, and memory usage during predictions.
4. Visualize results through plots comparing performance metrics across models.

### Misclassification Analysis:
1. Create a 2D dataset to visualize the decision boundaries of each model.
2. Analyze how the assumptions of each model affect classification accuracy.
3. Identify scenarios where misclassification occurs due to model limitations.

## Simulation Analysis
The performance analysis reveals that:
- Naive KNN exhibits slower performance as dataset size increases due to its exhaustive search method.
- LSH offers speed advantages but may compromise accuracy in certain cases due to its hashing approach.
- KD-Tree performs well in lower dimensions but struggles with high-dimensional data.

In the misclassification analysis, it was observed that:
- Certain configurations in 2D space led to significant misclassifications, particularly when data points are closely clustered or when classes overlap.
- The assumptions inherent in each model can lead to different decision boundaries, affecting overall classification performance.
