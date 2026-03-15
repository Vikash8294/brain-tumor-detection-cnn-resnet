# Brain Tumor Detection using CNN and ResNet

## Project Overview
This project focuses on the detection of brain tumors using a convolutional neural network (CNN) architecture leveraging transfer learning with ResNet50. The aim is to provide a reliable and efficient method for brain tumor detection in medical images.

## Dataset Structure
The dataset used in this project is structured as follows:

```
Brain_Tumor_Dataset/
├── training/
│   ├── no_tumor/
│   └── with_tumor/
└── testing/
    ├── no_tumor/
    └── with_tumor/
```

Each folder contains images categorized based on the presence of tumors.

## Methodology
The methodology comprises several stages including data preprocessing, model building, training, and evaluation. Our approach is outlined as follows:
- Data Preprocessing: Resizing images, normalization, and data augmentation to enhance model robustness.
- Model Architecture: Utilizing ResNet50 as the backbone with custom layers implemented on top for optimal performance.
- Compilation: Configuring loss functions and optimizers suitable for binary classification.

## CNN Model Details
The CNN model consists of:
- **Base Model:** ResNet50
- **Additional Layers:** Fully connected layers followed by dropout and activation layers for classification.

## Transfer Learning with ResNet50
Transfer learning allows us to leverage the pre-trained ResNet50 model, which has been trained on thousands of images, enabling better feature extraction from the provided dataset. Fine-tuning of specific layers leads to improved performance on our task.

## Techniques Used
- Convolutional Neural Networks (CNN)
- Transfer Learning
- Data Augmentation
- Image Normalization

## Results
The model performance is evaluated based on accuracy, precision, recall, and F1-score. Initial tests demonstrate promising results with significant accuracy in brain tumor detection.

## Visualization
Visualizations include loss/accuracy curves and confusion matrices to interpret model performance clearly.

## Technologies
- Python
- TensorFlow/Keras
- OpenCV
- Matplotlib
- Scikit-learn

## Workflow
1. Data Collection
2. Data Preprocessing
3. Model Training
4. Model Evaluation
5. Visualization of Results

## Conclusion
The project provides a successful implementation of a CNN-based approach to brain tumor detection, showcasing the effectiveness of transfer learning with ResNet50.

## Future Improvements
- Exploring other architectures and methods for potentially better accuracy.
- Implementing an interactive web application for real-time tumor detection.
- Expanding the dataset with more diverse images for improved generalization.