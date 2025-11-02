# 🧠 DefectVision — Industrial Surface Defect Detection System

> A computer vision project for automating industrial quality inspection using Convolutional Neural Networks (CNNs).  
> The goal: detect and classify surface defects in metallic sheets, reducing human error and improving manufacturing efficiency.

---

## 🎯 Objective

Automate surface defect identification by training a deep learning model that classifies defect types from metal surface images captured during production.  
This enables **real-time quality control** without manual visual inspection.

---

## 📊 Dataset — NEU Surface Defect Dataset

**Source:** [NEU Surface Defect Database](https://github.com/abin24/NEU-surface-defect-database)  
**Records:** 1,800 grayscale images (200×200 px)  
**Classes:** 6 defect types  
→ *Rolled-in scale, patches, crazing, pitted surface, inclusion, scratches*

| Attribute | Description |
|------------|-------------|
| Image | 200×200 px grayscale |
| Labels | 6 surface defect types |
| Split | 70% Train / 20% Validation / 10% Test |
| Format | `.jpg` files organized by defect folder |

---

## 🧠 Model Architecture — Custom CNN (No Transfer Learning)

Trained **from scratch** on the NEU dataset using a moderately deep CNN designed for small datasets with heavy augmentation.


**Optimizer:** Adam (lr = 1e-3)  
**Loss Function:** Categorical Crossentropy  
**Regularization:** Dropout + BatchNormalization  
**Epochs:** 40  
**Batch Size:** 32  

---

## ⚙️ Tech Stack

| Category | Tools |
|-----------|--------|
| 🧠 Deep Learning | TensorFlow, Keras |
| 🐍 Language | Python |
| 🎨 Visualization | Matplotlib, Seaborn |
| 🖼️ Image Processing | OpenCV |
| 📊 Evaluation | scikit-learn |

---

## 🧮 Training Setup

- **Augmentation:** Rotation, shift, zoom, brightness, flips  
- **Normalization:** Pixel values scaled to [0, 1]  
- **Regularization:** Dropout + BatchNorm  
- **Callbacks:** EarlyStopping, ModelCheckpoint  

---

## 📈 Results

| Metric | Value |
|:-------:|:------:|
| 🏋️ Training Accuracy | 96.8% |
| 🔍 Validation Accuracy | 95.4% |
| 🎯 Precision | 0.93 |
| 🔁 Recall | 0.92 |

---

---

## 💡 Key Insights

- Augmentation and normalization allowed strong generalization despite small dataset size.  
- Grad-CAM interpretability built trust in model predictions.  
- Model suitable for edge deployment on QA lines for automated defect detection.  
- Can be extended for segmentation-based defect localization.

---

## 🧰 Folder Structure
