# Fine-Grained-Food-Classification-and-Image-Enhancement
Course: Visual Information Processing and Management - Università degli Studi di Milano Bicocca

## Introduction:
In this project, we tackled the fine-grained food classification problem using the FoodX-251 dataset. The dataset provided by the professor included:
- A training set with 20 images per class (5020 images total).
- An unlabeled training set with 113,455 images, allowing us to expand the training data.
- A degraded validation set (11,994 images), representing real-world conditions with suboptimal acquisition quality, serving as the true test set.
Our objective was to design, implement, and evaluate a classification system capable of handling high intra-class variability and challenging image conditions. We employed deep learning techniques, data augmentation, and image enhancement strategies to improve classification accuracy.

## Methods:
- Model Training:
Used DenseNet-201 with transfer learning.
Extracted features from the global average pooling layer.
Added custom fully connected layers with Batch Normalization and Dropout.
- Handling Low-Quality Images:
Anomaly Detection: Applied SIFT + K-Means clustering to detect and remove outliers.
Super-Resolution with ESRGAN: Enhanced image quality for better model performance.
Entropy-Based Filtering: Removed highly uncertain predictions.
Preprocessing Enhancements: Applied sharpening, contrast enhancement, and denoising.
Classification Approaches:
Trained the model on 20 images per class, then expanded the dataset using the unlabeled set.
Conducted classification on the validation set and degraded validation set.
Analyzed and compared different strategies for handling degraded images.

## Results & Conclusions:
DenseNet-201 performed well, benefiting from feature reuse and efficient parameter utilization.
Outlier detection and removal improved classification accuracy.
Image quality enhancement (ESRGAN, sharpening, contrast adjustment) led to better predictions on degraded images.
Entropy filtering helped refine predictions, reducing uncertainty in misclassified images.
Future improvements: Further fine-tuning of image enhancement techniques and exploration of alternative deep learning architectures.
This project demonstrates the effectiveness of feature extraction, image enhancement, and outlier detection in fine-grained food classification.
