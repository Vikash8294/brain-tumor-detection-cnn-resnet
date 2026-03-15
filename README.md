# Brain Tumor Classification using CNN and ResNet50

## Project Overview
This project focuses on detecting **brain tumors from MRI images using deep learning techniques**.  
The goal is to classify MRI scans into two categories:

- Tumor
- No Tumor

In this project, a **baseline CNN model** was first implemented, and then **Transfer Learning using ResNet50** was applied to improve the classification accuracy.

---

## Dataset

The dataset used is **Brain MRI Images for Brain Tumor Detection**.

### Dataset Structure

Total images: **~250 MRI scans**
<br>
brain_tumor_dataset/<br>
├── yes  → MRI images containing tumors<br>
└── no   → MRI images without tumors

---

## Data Preprocessing

The following preprocessing steps were applied:

- Image resizing
- Image preprocessing
- Label encoding
- Train–test split

Images were resized to:

224 × 224

which is required for **ResNet50 architecture**.

---

# Model 1: Convolutional Neural Network (CNN)

First, a **custom CNN model** was built as a baseline model.

### CNN Architecture

The CNN model contains:

- Convolution layers
- MaxPooling layers
- Flatten layer
- Dense layers
- Dropout layer (to reduce overfitting)

### Training Parameters

- Epochs: 15–20
- Batch Size: 32
- Optimizer: Adam
- Loss Function: Binary Crossentropy

### CNN Result

Accuracy achieved:

**76%**

This model provided a good baseline but had limited performance due to the **small dataset size**.

---

# Improving Accuracy using Transfer Learning

To improve the model performance, **Transfer Learning with ResNet50** was used.

ResNet50 is a deep convolutional neural network pretrained on the **ImageNet dataset**, which helps extract powerful image features.

---

# Model 2: ResNet50 (Transfer Learning)

Steps performed:

1. Loaded pretrained **ResNet50**
2. Removed the top classification layer (`include_top=False`)
3. Used **ImageNet pretrained weights**
4. Added custom classification layers

### Custom Layers Added

- GlobalAveragePooling
- Dense layer (ReLU)
- Dropout layer
- Final Sigmoid output layer

---

# Techniques Used to Improve Accuracy

Several improvements were made to increase model performance:

### 1. Transfer Learning
Used pretrained **ResNet50** to reuse learned image features.

### 2. ResNet Image Preprocessing
Used:


instead of simple normalization.

### 3. Larger Image Size

Images resized to:

224 × 224

to match ResNet architecture.

### 4. Freezing Base Layers
Most ResNet layers were frozen so pretrained features were preserved.

### 5. Custom Classification Head
New dense layers were added to adapt the model to the tumor detection task.

### 6. Smaller Learning Rate
A smaller learning rate was used to stabilize training.

---

# Results

| Model | Accuracy |
|------|---------|
| CNN (Baseline) | **76%** |
| ResNet50 | **92%** |

The **ResNet50 model significantly improved the performance** compared to the baseline CNN.

---

# Visualization

The project includes:

- Training vs Validation Accuracy Graph
- Loss Graph
- Random MRI Prediction Example

These visualizations help evaluate model performance.

---

# Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab

---

# Project Workflow

Dataset → Preprocessing → CNN Baseline Model → Evaluate Performance → Apply Transfer Learning (ResNet50) → Train Model → Evaluate Accuracy → Visualize Results

---

# Conclusion

This project demonstrates that **Transfer Learning significantly improves medical image classification performance**, especially when working with small datasets.

Using **ResNet50 improved the accuracy from 76% to 92%**, showing the effectiveness of pretrained deep learning models for healthcare applications.

---

# Future Improvements

Possible future improvements include:

- Data augmentation
- Fine-tuning deeper layers of ResNet
- Using advanced architectures like:
  - EfficientNet
  - MobileNet
  - DenseNet
- Increasing dataset size

---

Deep Learning Project – Brain Tumor MRI Classification
