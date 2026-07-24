# 🌾 Rice Leaf Disease Detection using CNN and Transfer Learning

## Overview

This project presents a deep learning-based approach for automatically detecting rice leaf diseases from images. Three different deep learning models were implemented and compared to identify the most suitable architecture for accurate disease classification.

The final solution uses **Transfer Learning with MobileNetV2**, achieving high validation accuracy while remaining lightweight enough for future deployment on mobile or edge devices.

---

## Problem Statement

Rice is one of the world's most important food crops. Diseases affecting rice leaves can significantly reduce crop yield if not detected early.

Traditional disease identification relies on manual inspection, which is time-consuming and depends on expert knowledge. This project aims to automate disease detection using computer vision and deep learning techniques.

The model classifies rice leaves into the following categories:

- Bacterial Leaf Blight
- Brown Spot
- Leaf Smut

---

## Dataset

- Total Images: **119**
- Classes: **3**
- Image Format: JPG
- Image Size: **224 × 224**

| Disease | Images |
|----------|--------|
| Bacterial Leaf Blight | 40 |
| Brown Spot | 40 |
| Leaf Smut | 39 |

---

## Technologies Used

- Python
- TensorFlow
- Keras
- OpenCV
- NumPy
- Matplotlib
- Scikit-learn

---

## Project Workflow

1. Dataset Preparation
2. Image Preprocessing
3. Data Augmentation
4. CNN Model Development
5. Transfer Learning with VGG16
6. Transfer Learning with MobileNetV2
7. Fine-Tuning
8. Model Evaluation
9. Prediction on New Images
10. Model Comparison

---

## Data Preprocessing

The preprocessing pipeline includes:

- Image resizing (224×224)
- Pixel normalization
- Data augmentation
    - Rotation
    - Zoom
    - Horizontal Flip
    - Width & Height Shift
- Validation split
- Reproducibility using fixed random seeds

---

## Models Implemented

### 1. Custom CNN
A baseline convolutional neural network built from scratch.

### 2. VGG16
ImageNet pretrained VGG16 with transfer learning and fine-tuning.

### 3. MobileNetV2
ImageNet pretrained MobileNetV2 with transfer learning and fine-tuning.

---

## Model Performance

| Model | Validation Accuracy |
|--------|---------------------|
| CNN | 34.78% |
| VGG16 | ~90% |
| MobileNetV2 | **95.65%** |

MobileNetV2 achieved the highest validation accuracy and was selected as the final model.

---

## Results

The final model successfully identifies rice leaf diseases with high accuracy and demonstrates the effectiveness of transfer learning on small agricultural image datasets.

---

## Project Structure

```
Rice-Leaf-Disease-Detection/
│
├── Data/
├── notebooks/
├── saved_models/
├── images/
├── reports/
├── README.md
├── requirements.txt
└── app.py   (Future Deployment)
```
---

## 📁 Dataset

The dataset is **not included** in this repository due to GitHub storage limitations.

Download the rice leaf disease dataset and place it inside a folder named **`data`** (or update the notebook path accordingly) with the following structure:

```text
data/
│
├── Bacterial leaf blight/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
│
├── Brown spot/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
│
└── Leaf smut/
    ├── image1.jpg
    ├── image2.jpg
    └── ...
```

> **Important:** The notebook expects all three disease folders to be inside a single `data` directory. If your dataset is stored elsewhere, update the dataset path in the notebook before running the project.

---

## Future Improvements

- Grad-CAM visualization for model explainability
- Streamlit web application
- TensorFlow Lite conversion
- Mobile application deployment
- Larger dataset for improved generalization

---

## Author

**M. Chandra Sekhar**

Artificial Intelligence & Data Science Graduate

Interested in:
- Machine Learning
- Computer Vision
- Deep Learning
- Generative AI

LinkedIn: *https://linkedin.com/in/chandrasekharmangali*


---

## License

This project is intended for educational and research purposes.
