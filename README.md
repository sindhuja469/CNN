# Convolutional Neural Networks (CNN)

## Project Overview
This project focuses on building and evaluating **Convolutional Neural Networks (ConvNets)** to understand how training samples and model initialization (from scratch vs. pretrained) affect performance.  
The goal is to analyze the **generalization ability**, **accuracy**, and **overfitting** behavior across multiple CNN models trained on an image dataset.

---

## Dataset
##  Dataset Access
The dataset used for this project is available on Kaggle:  
👉 [Kaggle Dataset Link](https://www.kaggle.com/datasets/zeegelin/cats-and-dogs-small)

- **Total files:** 4,000 images  
- **Data split:** Training, Validation, and Test sets  
- **Augmentation techniques:** Rotation, Zoom, and Horizontal Flip to enhance generalization and reduce overfitting.

---

## Model Architectures

### Model 1 – Base CNN
- Trained from scratch using the entire dataset.
- Achieved high training accuracy but showed **overfitting** on validation and test sets.

### Model 2 – CNN with Data Augmentation & Dropout
- Introduced regularization and augmentation.
- Showed balanced training and validation performance.

### Model 3 – CNN with Reduced Training Samples
- Trained on a smaller dataset.
- Demonstrated **underfitting** and lower accuracy due to limited data.

### Model 4 – Pretrained Model (VGG16)
- Used transfer learning with VGG16 pretrained on ImageNet.
- Achieved the **best accuracy** and **strong generalization** across datasets.

---

## Hyperparameters
| Parameter | Value |
|------------|--------|
| Optimizer | Adam (learning rate = 0.0001) |
| Loss Function | Binary Cross-Entropy |
| Batch Size | 32 |
| Epochs | 30 |
| Dense Layer Neurons | 256 (Model 1 & 2), 512 (Model 3 & 4) |
| Activation | ReLU |
| Regularization | Dropout |

---

## Results Summary

| Model | Test Accuracy | Test Loss | Observation |
|-------|----------------|------------|--------------|
| **Model 1 (Base)** | 0.710 | 1.83 | Overfitting – high training accuracy but poor generalization |
| **Model 2 (Aug + Dropout)** | 0.774 | 0.464 | Improved generalization and balance |
| **Model 3 (Small Sample)** | 0.644 | 0.646 | Underfitting – insufficient feature learning |
| **Model 4 (VGG16 Pretrained)** | 0.899 | 0.375 | Excellent generalization and robustness |

---

##  How to Run the Project

1. **Clone this repository**
   ```bash
   git clone https://github.com/sindhuja469/CNN.git
   cd CNN
2. **install required dependencies**
    ```bash
   pip install tensorflow keras numpy matplotlib scikit-learn

3. **Open and run the Jupyter Notebook or Python script**
  ```bash
   jupyter notebook CNN.ipynb


