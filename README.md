# medical-imaging-machine-learning-pneumonia
Tests different machine learning models on actual patient x-ray data to detect penumonia


# Pneumonia Detection from Chest X-Ray Images using Machine Learning

## Overview
This project explores the application of machine learning techniques to classify chest X-ray images as either **normal** or **pneumonia-related lung opacity**. The work emphasizes not only predictive performance, but also **model behavior under class imbalance**, **evaluation trade-offs**, and **comparative analysis** between deep learning and traditional machine learning approaches.

The project was developed as part of a machine learning course and is presented as a complete, reproducible study including code, experiments, and a formal technical report.

## Problem Motivation
Pneumonia is a serious respiratory infection that can be life-threatening if not diagnosed early. Chest X-rays are a common diagnostic tool, but manual interpretation is time-consuming and subject to human error. Automated image classification using machine learning has the potential to assist clinicians by improving efficiency and diagnostic support.

## Dataset
- Adapted version of the *Chest X-Ray Images (Pneumonia)* dataset
- Two classes: **Normal** and **Pneumonia (Opacity)**
- Strong class imbalance reflecting real clinical conditions

> Raw image data is not included due to size constraints.  
> Dataset source: Kaggle (Paul Mooney)

## Models Implemented
Three supervised learning models of increasing complexity were evaluated:

### 1. Convolutional Neural Network (CNN)
- Learns spatial features directly from image data
- Achieved highest overall performance
- Required careful monitoring to mitigate overfitting

### 2. Logistic Regression with PCA
- Images flattened and reduced using PCA (95% variance retained)
- Served as a strong and interpretable baseline
- Demonstrated competitive ROC–AUC despite linear structure

### 3. Random Forest (PCA Features)
- Ensemble-based approach
- Captured non-linear relationships
- Exhibited high sensitivity but reduced specificity

## Evaluation Metrics
Given the imbalanced dataset, performance was evaluated using:
- Accuracy
- Precision
- Recall (Sensitivity)
- F1-score
- Confusion matrices
- ROC curves and AUC

## Key Findings
- All models favored **high sensitivity** for pneumonia detection, reflecting clinical priorities
- CNN achieved the strongest overall performance (AUC ≈ 0.92)
- Classical models remained competitive and interpretable
- Class imbalance strongly influenced specificity across all models

## Author
**Jatesh Joshi**
