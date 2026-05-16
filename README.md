# Handwritten Digit Recognition

A machine learning project that recognizes handwritten digits (0-9) using the MNIST dataset and multiple classification algorithms. The project includes feature extraction, model training, and an interactive web interface built with Gradio.

## Overview

This project implements a complete handwritten digit recognition pipeline using:
- The MNIST dataset (70,000 grayscale images of 28x28 pixels)
- Advanced feature extraction techniques
- Multiple machine learning classifiers
- An interactive Gradio interface for real-time predictions

## Features

- **MNIST Dataset**: Automatically loads 60,000 training and 10,000 test images
- **Feature Extraction**: Implements HOG (Histogram of Oriented Gradients), histogram equalization, edge detection, mean, and variance features
- **Multiple Models**: Trains and compares KNN, Random Forest, SVM, Decision Tree, and Logistic Regression
- **Performance Metrics**: Evaluates models using accuracy, precision, and F1 score
- **Web Interface**: Interactive Gradio application for digit prediction
- **CSV Export**: Saves extracted features to CSV files for easy analysis

## Installation

Install the required dependencies:

```
pip install tensorflow scikit-image opencv-python scikit-learn pandas gradio numpy
```

## Usage

The project is organized into sections:

1. **Load MNIST Dataset**: Automatically downloads and loads the dataset
2. **Feature Extraction**: Extracts meaningful features from images using multiple techniques
3. **Model Training**: Trains five different machine learning models on extracted features
4. **Model Evaluation**: Compares model performance using various metrics
5. **Web Interface**: Launch an interactive Gradio application for predictions

### Running the Full Pipeline

Execute the Python script to:
- Load the MNIST dataset
- Extract features and save to CSV files
- Train all models
- Launch the Gradio web interface

```
python digit_recognition.py
```

### Using the Gradio Interface

1. Upload an image of a handwritten digit
2. Select a machine learning model from the dropdown
3. Click Submit to get the prediction
4. The interface will return the predicted digit (0-9)

## Feature Extraction Methods

The project uses four main feature extraction approaches:

- **HOG (Histogram of Oriented Gradients)**: Captures edge and texture information with 9 orientations, 8x8 pixel cells, and 2x2 blocks
- **Histogram Equalization**: Enhances image contrast and computes mean values
- **Canny Edge Detection**: Identifies edges in the image and sums their values
- **Statistical Features**: Computes mean and variance of pixel intensities

## Models Compared

| Model | Type | Best For |
|-------|------|----------|
| K-Nearest Neighbors (KNN) | Instance-based | Fast predictions, simple implementation |
| Random Forest | Ensemble | Handling multiple features, robustness |
| Support Vector Machine (SVM) | Kernel-based | High-dimensional data, complex boundaries |
| Decision Tree | Tree-based | Interpretability, feature importance |
| Logistic Regression | Linear | Fast training, baseline comparison |

## Project Structure

- **Data Loading**: MNIST dataset automatic download and split
- **Feature Extraction**: Processes images and creates feature vectors
- **CSV Generation**: Saves training and testing features with labels
- **Model Training**: Fits all classifiers on extracted features
- **Evaluation**: Generates accuracy, precision, and F1 scores
- **Prediction Interface**: Gradio web app for interactive predictions

## Dependencies

- **TensorFlow**: For MNIST dataset and deep learning utilities
- **scikit-image**: For HOG and histogram equalization
- **OpenCV**: For image processing and Canny edge detection
- **scikit-learn**: For machine learning models and metrics
- **Pandas**: For data handling and CSV operations
- **NumPy**: For numerical operations
- **Gradio**: For interactive web interface

## Output

The project generates:
- `mnist_train_features.csv`: Training features and labels
- `mnist_test_features.csv`: Testing features and labels
- Classification reports for each model
- Performance metrics comparison
- Interactive web interface for real-time predictions

## Error Handling

The project includes comprehensive error handling for:
- Missing CSV files
- Empty data files
- CSV parsing errors
- Prediction errors
- Invalid model selection

## Future Enhancements

- Implement deep learning models (CNN)
- Add data augmentation techniques
- Create an ensemble model combining multiple classifiers
- Deploy to cloud platforms
- Add model persistence and loading
- Implement batch prediction
- Add confidence scores to predictions
- Create visualization of extracted features

## Author

Created as a machine learning project for handwritten digit recognition.

## License

This project uses the MNIST dataset which is publicly available.
```

