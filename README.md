# Comparative Analysis of Deep Learning Architectures for Fruit Classification

This project presents a comparative study of multiple deep learning architectures for fruit image classification using Transfer Learning techniques.

A total of 10 fruit categories were used to evaluate the classification performance of five different pretrained CNN models:

- MobileNetV2
- VGG16
- InceptionV3
- ResNet50
- EfficientNetB0

The experiments focused on analyzing model accuracy, sensitivity, specificity, precision, F1-score, and AUC performance metrics.

---

# Project Objective

The primary objective of this study is to evaluate the effectiveness of pretrained deep learning architectures for fruit recognition tasks in computer vision applications.

The project investigates:

- Classification accuracy
- Model stability
- Transfer learning efficiency
- Computational performance
- Failure analysis of complex architectures

---

# Dataset Information

The dataset contains images from 10 different fruit classes:

- Apple
- Avocado
- Banana
- Cherry
- Kiwi
- Mango
- Orange
- Pineapple
- Strawberry
- Watermelon

### Training Parameters

- Input Size: `128x128`
- Optimizer: `Adam`
- Epochs: `10`
- Training Method: `Transfer Learning`

---

# Evaluation Metrics

The models were evaluated using the following performance metrics:

- Accuracy
- Sensitivity
- Specificity
- Precision
- F1-Score
- AUC (Area Under Curve)

---

# Model Performance Analysis

## MobileNetV2

MobileNetV2 achieved one of the best balances between speed and accuracy.

### Key Observations

- Accuracy reached approximately `88% - 90%`
- High sensitivity on:
  - Pineapple (`97%`)
  - Apple (`93%`)
- Efficient lightweight architecture with low computational cost

### Analysis

The use of Depthwise Separable Convolutions enabled the model to classify fruit shapes efficiently while maintaining high performance.

---

## VGG16

VGG16 demonstrated the most stable and reliable overall performance among all tested architectures.

### Key Observations

- Achieved `100% sensitivity` on the Strawberry class
- Produced AUC scores between `0.99 - 1.00`
- Strong feature extraction capability

### Analysis

Its deep convolutional structure successfully captured texture and color gradients in fruit images.

---

## InceptionV3

InceptionV3 showed stable learning behavior throughout training.

### Key Observations

- Pineapple classification accuracy reached `95%`
- AUC scores ranged between `0.94 - 0.99`

### Analysis

The architecture handled fruit size variations effectively and maintained strong classification consistency.

---

## ResNet50

ResNet50 produced significantly lower performance compared to other models.

### Key Observations

- Accuracy remained around `20%`
- The model frequently predicted the Mango class

### Failure Analysis

Possible reasons include:

- Hyperparameter incompatibility
- Overfitting / Underfitting issues
- Excessive model complexity for `128x128` input resolution

---

## EfficientNetB0

EfficientNetB0 failed to learn meaningful class distinctions during training.

### Key Observations

- The model predicted nearly all samples as Strawberry
- Strawberry sensitivity reached `100%`
- Other classes remained close to `0%`

### Failure Analysis

The model likely became trapped in a local minimum due to incompatible learning rate settings.

---

# Comparative Discussion

## Best Overall Architecture

VGG16 provided the most reliable and stable classification performance across all metrics.

Advantages:

- Strong texture extraction
- High feature representation capability
- Excellent AUC performance

---

## Most Efficient Architecture

MobileNetV2 achieved competitive accuracy with significantly fewer parameters.

Advantages:

- Faster inference
- Lower computational requirements
- Suitable for real-time systems

---

## Transfer Learning Impact

Transfer Learning significantly improved:

- Training efficiency
- Generalization performance
- Convergence speed

Pretrained ImageNet weights provided strong initialization for fruit classification tasks.

---

# Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab

---

# Project Structure

```bash
├── dataset/
├── models/
├── notebooks/
├── results/
├── confusion_matrices/
├── roc_curves/
├── train.py
├── evaluate.py
├── requirements.txt
└── README.md
```

---

# Future Improvements

Potential future improvements include:

- Hyperparameter optimization
- Dynamic learning rate scheduling
- Advanced data augmentation
- Larger fruit datasets
- Real-time deployment support
- Model ensemble techniques

---

# Conclusion

The experimental results demonstrate that pretrained CNN architectures can successfully classify fruit images with high accuracy using Transfer Learning techniques.

Among all tested models:

- VGG16 provided the highest overall reliability
- MobileNetV2 delivered the best efficiency-performance balance

The developed system shows strong potential for applications in:

- Agricultural technologies
- Smart retail systems
- Automated fruit recognition systems
- Computer vision-based quality control
