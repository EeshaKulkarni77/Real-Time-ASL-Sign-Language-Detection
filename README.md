# Real-Time ASL Sign Language Detection using Deep Learning

## Overview

This project implements a deep learning-based system for recognizing American Sign Language (ASL) hand gestures using a Convolutional Neural Network (CNN).

The system leverages:
- Image-based feature extraction using CNN  
- Data augmentation for improved generalization  
- Real-time webcam-based prediction  

The goal is to accurately classify ASL hand signs and demonstrate a practical real-time computer vision application.

---

## Problem Statement

Recognizing sign language from images is a challenging computer vision task due to:
- Variations in hand shapes and orientations  
- Differences in lighting and background conditions  
- High similarity between certain hand gestures  

This project addresses the problem by:
- Classifying ASL hand signs from image data  
- Learning spatial patterns using CNNs  
- Extending the model to real-time webcam-based prediction  

---

## Dataset

- Dataset: Sign Language MNIST  
- Classes: 25  
- Image Size: 28x28 grayscale  

The dataset includes:
- Static hand gesture images representing ASL alphabet letters  
- Pixel-level grayscale image data  

Note:
- Letters **J** and **Z** are excluded as they involve motion rather than static gestures  

---

## System Architecture

Input Images
- Data Preprocessing
- Data Augmentation
- CNN Model
- Feature Extraction
- Classification Layer
- ASL Letter Prediction
- Real-Time Webcam Inference
- 
---

## Approach

### Data Preprocessing
- Normalization of pixel values (0–255 → 0–1)  
- Reshaping images to CNN input format (28x28x1)  
- One-hot encoding of labels  
- Train-test split  

---

### Model Design

**CNN Layers**
- Multiple convolutional layers for spatial feature extraction  
- MaxPooling layers for dimensionality reduction  
- Dropout layers for regularization  

**Dense Layers**
- Fully connected layers for classification  
- Softmax output layer for multi-class prediction  

The model is trained using:
- Adam optimizer  
- Categorical cross-entropy loss  
- Early stopping to prevent overfitting  

---

### Data Augmentation
- Rotation  
- Zoom  
- Width and height shifts  
- Shear transformations  

Horizontal flipping is avoided to preserve the semantic meaning of ASL signs.

---

## Results

- Achieved **96.95% test accuracy** :contentReference[oaicite:0]{index=0}  
- Strong performance across most ASL classes  
- Consistent validation performance indicating good generalization  

### Key Insight
> Data augmentation and proper preprocessing significantly improve model robustness and accuracy.

---

## Real-Time Detection

- Implemented webcam-based prediction system  
- Captures live frames and processes them for inference  
- Converts frames into model-compatible format  
- Outputs predicted ASL letter in real time  

---

## Technologies Used

- Python  
- NumPy, Pandas  
- Matplotlib, Seaborn  
- TensorFlow / Keras  
- OpenCV  
- PIL  

---

## Project Structure

├── asl_sign_language_detection.ipynb

├── README.md


---

## How to Run

1. Clone the repository:

2. Open the notebook:
`RT_ASL_Detection.ipynb`

3. Run all cells  

4. For real-time detection:
- Allow webcam access  
- Run the final section of the notebook  

---

## Key Takeaways

- CNNs are effective for structured image classification tasks  
- Data augmentation improves generalization  
- Real-time inference adds practical usability to ML systems  
- Proper preprocessing is critical for performance  

---

## Future Improvements

- Improve robustness on real-world backgrounds  
- Convert notebook into a web or Streamlit application  
- Add confidence thresholding  
- Extend to dynamic gesture recognition (J, Z)  

---

## Disclaimer

This project is a prototype for ASL recognition and is intended for educational purposes, not for full sign language interpretation.
