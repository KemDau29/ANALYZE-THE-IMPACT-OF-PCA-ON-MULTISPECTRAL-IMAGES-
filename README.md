# ANALYZE-THE-IMPACT-OF-PCA-ON-MULTISPECTRAL-IMAGES-

This project is a final-term assignment for the Mathematical for Artificial Intelligence course at the HCMC University of Technology and Education. The research investigates the impact of Principal Component Analysis (PCA) on the classification of multispectral satellite images using Support Vector Machine (SVM), based on the EuroSAT dataset.

## 1. Project Overview
Satellite image classification often faces challenges due to high dimensionality and large data volumes. This project aims to demonstrate how dimensionality reduction techniques, specifically PCA, can optimize computational resources (RAM and training time) while maintaining classification accuracy.

## 2. Key Features
Data Ingestion: Implemented a batch-based processing pipeline to handle large-scale .tif satellite images without exceeding memory limits.

Feature Engineering: Calculated the Normalized Difference Vegetation Index (NDVI) to enrich input features.

Dimensionality Reduction: Custom implementation of PCA to extract principal components, preserving 95% of cumulative variance.

Classification: Applied SVM with an RBF kernel, optimized via Grid Search and Random Search.

## 3. Project Structure
The project consists of three primary Jupyter Notebooks developed in the Kaggle environment:

ingestion-for-pca-svm.ipynb: Pipeline for data loading, preprocessing, and saving data in balanced batches.

eurosat-image-classifier-with-svm-raw.ipynb: Baseline training using SVM on raw, high-dimensional data.

eurosat-image-classifier-with-svm-after-pca.ipynb: Training SVM on PCA-transformed data to analyze performance improvements.

## 4. Key Findings
Resource Optimization: Achieved a ~75% reduction in RAM usage and a ~60% improvement in training speed compared to the raw dataset.

Performance: Maintained high classification accuracy (~83.56%) even after reducing the feature set, proving the efficiency of PCA in this context.

## 5. Implementation
The project is designed to run on the Kaggle platform.

The datasets are processed into .npy batches to manage memory efficiently.

The PCA engine performs eigen-decomposition on the covariance matrix.

SVM models are serialized using joblib for reusability.

For detailed methodologies and technical references, please refer to the project report.
