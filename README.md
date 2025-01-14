# Low Light Image Enhancement

## Project Overview
This project demonstrates the enhancement of low-light images using a **Convolutional Neural Network (CNN)**. The model improves the visibility, color fidelity, and noise reduction of images, making them suitable for critical applications like surveillance and professional photography. The project leverages the LOL dataset and real-world images captured at the UIC campus to validate its effectiveness.

---

## Problem Statement
Low-light conditions lead to images with poor visibility, high noise, and low clarity, limiting their usability in critical scenarios. Traditional enhancement methods, such as histogram equalization, often fail to handle complex lighting. This project utilizes CNNs to overcome these limitations and provide a robust solution for low-light image enhancement.

---

## Project Objectives
1. Develop a CNN-based model to enhance low-light images.
2. Improve visibility, color fidelity, and noise reduction without distorting natural imagery.
3. Evaluate performance using both standard datasets and real-world scenarios.

---

## Dataset
### **LOL Dataset**
- The LOL (Low-Light) dataset consists of 500 pairs of low-light and normal-light images. It was used to benchmark the model's performance.

### **Custom Dataset**
- For testing, our team curated a custom dataset by capturing images in low-light conditions across the UIC campus. These real-world images enriched our testing protocol, ensuring the model's effectiveness in practical scenarios.
- The dataset includes diverse lighting conditions and environments to test the model's robustness.
- **Access the Dataset:** A link to the dataset hosted on Google Drive is provided in the code file.

---

## Methodology
### **Data Preprocessing**
- Utilized the LOL dataset (500 pairs of low-light and normal-light images) and real-world images captured at the UIC campus.
- Applied **Histogram Equalization** to balance image contrast and enhance visibility.
- Normalized and converted images into suitable color spaces for further processing.

### **CNN Architecture**
- **Three Convolutional Layers:**
  - **Layer 1:** 64 filters, kernel size 5x5, padding 3.
  - **Layer 2:** 128 filters, kernel size 5x5, padding 2.
  - **Layer 3:** Transformed 128 input channels to 3 output channels (RGB) with a 3x3 kernel.
- **Activation Function:** ReLU after each layer for non-linearity.
- **Loss Function:** Mean Squared Error (MSE).
- **Optimizer:** Adam optimizer with a learning rate of 0.001.
- Trained in batches of 8 for 30 epochs using a CUDA-enabled GPU.

### **Evaluation Metrics**
- Tested on the LOL dataset and real-world UIC campus images.
- Key metrics included visibility, noise reduction, and color fidelity.

---

## Results
- **Dataset Images:** Significant improvement in contrast and visibility.
- **Real-World Images:** Effective enhancement of color fidelity and noise reduction.
- **Challenges Identified:** Extremely low-light conditions and natural color balance in some scenarios.

---

## Technologies Used
- **Frameworks/Libraries:** TensorFlow, Keras, NumPy, OpenCV
- **Dataset:** LOL Dataset and UIC campus images
- **Hardware:** CUDA-enabled GPU for training

