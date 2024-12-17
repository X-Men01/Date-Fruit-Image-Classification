# Date Fruit Image Classification

## Overview
This project classifies nine different types of date fruits using a **Custom Convolutional Neural Network (CNN)**. The custom CNN is lightweight and efficient compared to larger architectures like EfficientNet-B0.

---

## Dataset
The dataset consists of **9 classes** of date fruits:
- Ajwa
- Galaxy
- Mejdool
- Meneifi
- NabtatAli
- Rutab
- Shaishe
- Sokari
- Sugaey

**Training Images**: 1,156  
**Testing Images**: 502  

Images were preprocessed to size **224x224** with augmentation techniques such as:
- Random Horizontal Flip
- Random Rotation
- Normalization  

---

## Model Architecture
The **Custom CNN** includes:
1. **4 Convolutional Blocks**:
    - Convolutions → Batch Normalization → ReLU → Max Pooling
2. **Fully Connected Layer** with Dropout (0.5).  
![Date_Custom_CNN3](https://github.com/user-attachments/assets/4bcf0186-eb38-44ee-8973-b3e8faa69f0b)
Diagram generated using the [PlotNeuralNet](https://github.com/HarisIqbal88/PlotNeuralNet) library

**Model Summary**:  
- **Total Parameters**: 128,199  
- **Final Accuracy**: 97% on the test dataset.  

---
# Results

## Custom Model vs EfficientNet-B0

| Model            | Parameters | Size (MB) | Accuracy (%) |
|------------------|------------|-----------|-------------|
| Custom Model     | 128,199    | 30.22     | 97          |
| EfficientNet-B0  | 4,019,077  | 124.56    | 100         |

### **Model Comparison**  
- **Model Size**: EfficientNet-B0 is **4.12 times larger** than the Custom Model.
- **Parameter Count**: EfficientNet-B0 has **31.36 times more parameters**.
