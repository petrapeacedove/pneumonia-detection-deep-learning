# pneumonia-detection-deep-learning
Comparative deep learning study (CNN, VGG16, ResNet50) for pneumonia detection using chest x-ray datasets with experimental evaluation of data splits and model performance.

# Pneumonia Detection Using Deep Learning: A Comparative Experimental Study

## 1. Introduction

Pneumonia is a serious respiratory infection that can be detected using chest X-ray imaging. 
Automated detection using deep learning techniques can assist radiologists in early diagnosis 
and improve clinical decision-making.

This project presents a structured experimental comparison of three deep learning architectures 
for pneumonia classification using chest X-ray images:

- Custom Convolutional Neural Network (CNN)
- VGG16 (Transfer Learning)
- ResNet50 (Transfer Learning)

The study evaluates the impact of dataset size and train-test split strategies 
on model performance.

---

## 2. Objectives

The primary objectives of this project were:

1. To design and implement a baseline CNN architecture.
2. To apply transfer learning using VGG16 and ResNet50.
3. To compare model performance across different train-test splits (70:30 and 80:20).
4. To analyze performance differences between small and large datasets.
5. To determine the most effective configuration for pneumonia detection.

---

## 3. Experimental Design

The experiments were conducted in two structured phases.

### Phase 1: Small Dataset Experiments

Models trained:
- CNN
- VGG16
- ResNet50

Train-test splits:
- 70:30
- 80:20

Total experiments in this phase: 6

---

### Phase 2: Large Dataset Experiments

Models trained:
- CNN
- VGG16
- ResNet50

Train-test split:
- 80:20 (selected based on better generalization performance)

Total experiments in this phase: 3

---

### Total Experiments Conducted: 9

Each experiment required approximately 3 hours of GPU training time 
using Google Colab.

---

## 4. Dataset Description

The dataset consists of labeled chest X-ray images classified into:

- Pneumonia
- Normal

Images were preprocessed using:
- Resizing to uniform dimensions
- Normalization
- Data augmentation (if applied)
- Train-test splitting based on defined ratios

---

## 5. Methodology

### 5.1 Data Preprocessing
- Image resizing
- Normalization
- Dataset splitting
- Batch generation using data generators

### 5.2 Model Architectures

#### Custom CNN
- Multiple convolution layers
- ReLU activation
- MaxPooling layers
- Fully connected layers
- Softmax output layer

#### VGG16
- Pretrained on ImageNet
- Transfer learning approach
- Custom classification head added

#### ResNet50
- Residual network architecture
- Pretrained weights (ImageNet)
- Fine-tuned final layers

---

## 6. Evaluation Metrics

Models were evaluated using:

- Accuracy
- Training and validation loss curves
- Confusion matrix
- Validation performance comparison

---

## 7. Key Observations

- The 80:20 split consistently demonstrated better generalization.
- Transfer learning models (VGG16 and ResNet50) outperformed the baseline CNN.
- Larger dataset experiments showed improved validation stability.
- ResNet50 demonstrated strong generalization capability.

---

## 8. Repository Structure

```
notebooks/
    small_dataset/
        (6 experiments)
    large_dataset/
        (3 experiments)

results/
    (accuracy plots, confusion matrices)

docs/
    (project report)
```

All experiments are clearly separated by dataset size and split strategy.

---

## 9. Reproducibility

All notebooks can be executed independently in Google Colab.

Note:
Each training session required approximately 3 hours using GPU runtime.
Due to computational cost, notebooks retain final outputs to demonstrate results.

---

## 10. Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab (GPU)

---

## 11. Future Improvements

- K-fold cross-validation
- Hyperparameter tuning
- Grad-CAM visualization for model interpretability
- Testing EfficientNet and other architectures
- Deployment as a web-based diagnostic tool

---

## 12. Author

Petra Peace Dove  
MSc Bioinformatics  
Interested in Genomics, Artificial Intelligence in Medicine, and Computational Biology

If you use this work, please cite:

Petra Peace Dove (2026).
Pneumonia Detection using CNN and Transfer Learning.
GitHub Repository.
