# Neonatal Jaundice Prediction Using RGB-HSV Fusion and 1D CNN

## Overview

This project implements a non-invasive neonatal jaundice prediction system using skin images and deep learning. The goal is to estimate bilirubin levels from neonatal skin color information, reducing the need for invasive blood-based testing.

The model uses RGB and HSV color space features extracted from skin regions and processes them through a dual-stream 1D Convolutional Neural Network (1D CNN) for bilirubin level prediction.

## Features

* Skin region extraction from neonatal images
* RGB and HSV color space analysis
* Temporal sequence generation from pixel values
* Dual-stream 1D CNN architecture
* Bilirubin level regression
* Model evaluation using RMSE, MAE, and R² metrics

## Technologies Used

* Python
* TensorFlow / Keras
* OpenCV
* NumPy
* Pandas
* Scikit-learn
* Matplotlib

## Methodology

1. Load and preprocess neonatal skin images.
2. Extract skin regions of interest (ROI).
3. Convert images into RGB and HSV color spaces.
4. Generate pixel-based temporal sequences.
5. Feed RGB and HSV sequences into separate CNN branches.
6. Fuse extracted features and predict bilirubin levels.
7. Evaluate model performance using regression metrics.

## Model Architecture

RGB Features ──┐
├── 1D CNN ──┐
HSV Features ──┘            │
├── Feature Fusion
│
├── Dense Layers
│
└── Bilirubin Prediction

## Evaluation Metrics

* Root Mean Squared Error (RMSE)
* Mean Absolute Error (MAE)
* R² Score

## Results

The model was trained using a dual-stream RGB-HSV architecture with regularization techniques including Batch Normalization, Dropout, L2 Regularization, and Early Stopping to improve generalization performance.

## Disclaimer

This project was developed for academic and research purposes and is not intended for clinical diagnosis or medical decision-making.
