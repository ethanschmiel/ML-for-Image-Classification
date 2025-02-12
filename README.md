# Machine Learning for Image Classification: Fashion MNIST

## Project Overview

This project explores machine learning techniques to classify images from the Fashion MNIST dataset. The dataset consists of grayscale images (28x28 pixels) representing 10 different fashion categories. The study evaluates multiple models, including Principal Component Analysis (PCA), k-Nearest Neighbors (kNN), Support Vector Machines (SVM), Linear Discriminant Analysis (LDA), Quadratic Discriminant Analysis (QDA), and Convolutional Neural Networks (CNN). The goal is to compare the accuracy and computational efficiency of these approaches.

## Methodology

### 1. Data Preprocessing

- Images were flattened into 784-dimensional feature vectors and normalized.
- PCA was used to reduce dimensionality while retaining 90% of the variance.
- The optimal number of principal components was determined to be **137**.

### 2. Model Evaluations

#### a. k-Nearest Neighbors (kNN) Classification

- Implemented kNN on both the original 784-dimensional dataset and the PCA-reduced 137-dimensional dataset.
- Evaluated k-values ranging from **1 to 11**.
- PCA-reduced data improved computational speed significantly (~10-15 seconds vs. ~70 seconds per iteration) without a noticeable drop in accuracy.

#### b. Support Vector Machines (SVM), LDA, and QDA

- **Linear SVM** achieved ~85% accuracy but had long runtimes.
- **RBF SVM** provided the highest accuracy among traditional models but was computationally expensive.
- **LDA & QDA** were computationally efficient but had lower accuracy, with QDA performing the worst (~70%).
- **Conclusion**: RBF SVM was the best-performing traditional classifier, balancing accuracy and computational efficiency.

#### c. Convolutional Neural Networks (CNNs)

- Built a CNN model with convolutional and max-pooling layers.
- Trained for **30 epochs**, achieving the highest accuracy among all models.
- Experimented with a **reduced training set (1000 samples)** to analyze performance differences.
- Plotted training and validation loss/accuracy to evaluate model convergence.

## Key Findings

- **Dimensionality Reduction**: PCA significantly improved computational efficiency without reducing accuracy.
- **kNN Performance**: PCA helped optimize kNN’s runtime and accuracy.
- **Model Comparisons**: RBF SVM outperformed other traditional models.
- **Deep Learning with CNNs**: Achieved the best accuracy and efficiency, demonstrating the advantage of deep learning in image classification.

## Conclusion

This project highlights the benefits of dimensionality reduction and machine learning models for image classification. While traditional models like SVM provided strong results, **CNNs outperformed all methods**, emphasizing the power of deep learning for complex visual data analysis.
