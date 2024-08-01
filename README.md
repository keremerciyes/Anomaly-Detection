# Anomaly Detection on Hyperthyroidism Dataset

## Overview

This project demonstrates anomaly detection on a hyperthyroidism dataset, which includes both categorical and continuous features. Three unsupervised algorithms—Nearest Neighbors, DBSCAN, and Isolation Forest—are applied to detect anomalies. The results of each algorithm are compared to determine the most effective method for this dataset.

**Authors:** Kerem Erciyes and Mustafa Soydan  
**Affiliation:** Physics Department, University of Milan Bicocca, Milan, ITALY

## Table of Contents

- [Introduction](#introduction)
- [Methodology](#methodology)
- [Data Preprocessing](#data-preprocessing)
- [Algorithms](#algorithms)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [References](#references)

## Introduction

Hyperthyroidism is an endocrine disorder characterized by excessive production of thyroid hormones. Early detection and diagnosis are crucial for effective treatment and management. This project aims to identify anomalies in a hyperthyroidism dataset using Nearest Neighbors, DBSCAN, and Isolation Forest algorithms.

## Methodology

### Data Preprocessing

The dataset comprises both continuous and categorical features. Preprocessing steps include:
- Scaling continuous features using `StandardScaler`.
- One-hot encoding categorical features for Isolation Forest.
- Computing Gower distance matrix for Nearest Neighbors and DBSCAN to handle mixed data types.

### Algorithms

1. **Nearest Neighbors:** Distance-based approach using Gower distance.
2. **DBSCAN:** Clustering approach with parameters `eps` and `min_samples` optimized using the KneeLocator algorithm.
3. **Isolation Forest:** Ensemble method for anomaly detection with hyperparameters tuned for the dataset.

## Results

- **Nearest Neighbors:** Detected 1609 anomalies.
- **DBSCAN:** Detected 1499 anomalies.
- **Isolation Forest:** Detected 360 anomalies.

The results indicate that Isolation Forest is the most effective method for this dataset, with anomalies detected by Isolation Forest largely overlapping with those found by the other methods.

## Installation

To run this project, you'll need Python and the following libraries:

- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- t-SNE

## Usage

1. **Clone the repository:**

git clone https://github.com/keremerciyes/Anomaly-Detection.git
cd anomaly-detection

2. **Run the Jupyter Notebook:**

jupyter notebook anomaly_detection.ipynb

3. **Dataset:**

The dataset (`hyperthyroid.csv`) is included in the repository. Ensure it is in the same directory as the notebook.

4. **Notebook:**

Open `anomaly_detection.ipynb` and run the cells to preprocess the data, apply the algorithms, and visualize the results.

## References

1. Lan, D. T., & Yoon, S. (2023). Trajectory Clustering-Based Anomaly Detection in Indoor Human Movement. Sensors, 23(6), 3318. https://doi.org/10.3390/s23063318
2. Nizan, O., & Tal, A. (2023). K-NNN: Nearest Neighbors of Neighbors for Anomaly Detection. arXiv.org. https://arxiv.org/abs/2305.17695
3. Xu, H., Pang, G., Wang, Y., & Wang, Y. (2022). Deep Isolation Forest for Anomaly Detection. arXiv (Cornell University). https://doi.org/10.48550/arxiv.2206.06602

## Contact

For any questions or inquiries, please contact:

- Kerem Erciyes: k.erciyes@campus.unimib.it
- Mustafa Soydan: m.soydan@campus.unimib.it