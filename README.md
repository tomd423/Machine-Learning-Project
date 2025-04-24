# Surface Defect Detection Using CNNs

**Author:** Tom Deng  
**Course Project - [Course Name or Code, if applicable]**

## 📌 Project Description and Objective

This project focuses on the development of a Convolutional Neural Network (CNN) model for automated surface defect classification in industrial materials. Traditional visual inspection is prone to inconsistency and inefficiency. The objective of this work is to build a scalable deep learning model that can accurately classify six types of surface defects from grayscale images, contributing to more efficient quality control processes in manufacturing.

## 📂 Dataset Used

- **Source:** NEU Surface Defect Database (via Kaggle)  
- **Total Images:** 1,440 grayscale images  
- **Classes:** scratches, rolled-in scale, pitted surface, patches, inclusion, crazing  
- **Resolution:** Resized to 64x64 pixels  
- **Preprocessing:** Grayscale conversion, normalization (pixel values scaled between 0 and 1), label encoding

## 🧠 Model and Method Overview

- **Framework:** TensorFlow with Keras  
- **Architecture:**  
  - Two Conv2D layers (ReLU activation)  
  - MaxPooling layers after each convolution  
  - Flatten + Dense (64 units, ReLU)  
  - Output layer with Softmax (6 classes)  
- **Training:**  
  - Loss Function: Categorical Crossentropy  
  - Optimizer: Adam  
  - Epochs: 10  
  - Batch Size: 32  
  - Data split: 80% training, 20% testing  


## 📊 Summary of Results and Key Findings

- **Test Accuracy:** 78%  
- **Best Performing Class:** Patches (Precision = 0.96, Recall = 0.96)  
- **Most Confused Classes:** Crazing and pitted surface  
- **Key Insight:** Simple CNNs are effective for classifying surface defects with minimal preprocessing.  
- **Improvement Opportunities:** Apply data augmentation, increase image resolution, use pre-trained models like ResNet.

---


