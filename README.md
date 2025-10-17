<h1 align="center">🌱 Plant Disease Classification</h1>  
<p align="center"> 
 <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>  
 <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white"/>  
 <img src="https://img.shields.io/badge/Keras-D00000?style=flat-square&logo=keras&logoColor=white"/>  
 <img src="https://img.shields.io/badge/Numpy-013243?style=flat-square&logo=numpy&logoColor=white"/>  
 <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white"/>  
 <img src="https://img.shields.io/badge/Matplotlib-007ACC?style=flat-square&logo=plotly&logoColor=white"/>  
 <img src="https://img.shields.io/badge/Seaborn-4C8CBF?style=flat-square&logo=seaborn&logoColor=white"/>  
 <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white"/>  
</p>

---

## 📜 Project Overview
The **Plant Disease Classification** project aims to automatically detect and classify plant leaf diseases using the **PlantVillage dataset** consisting of **38 classes**. Implemented in a Colab Notebook, the workflow includes data preprocessing, augmentation, model building Custom CNN & MobileNetV2, training, and evaluation.

**Key highlight**: MobileNetV2 achieved **\~99% accuracy**, outperforming the baseline CNN (\~96% accuracy).

---

## 🚀 Features

### Data Preprocessing:

* Loaded dataset from Kaggle (PlantVillage Dataset).
* Resized images to **150×150 pixels**.
* Normalized pixel values (**Min-Max scaling → \[0,1]**).
* Used **ImageDataGenerator** for augmentation (rotation, shift, shear zoom, flip).

### Models Implemented:

* **Custom CNN**
* **MobileNetV2 (Transfer Learning)**

### Training:

* Loss: **Categorical Crossentropy**
* Optimizer: **Adam**
* Metrics: **Accuracy**
* Epochs: 10

---

## 📊 Dataset

* **Source**: [Kaggle – PlantVillage Dataset](https://www.kaggle.com/datasets/abdallahalidev/plantvillage-dataset)
* **Classes**: 38
* **Total Images**: \~54,000

**Split**:

* Training → 43,444 images
* Validation → 5,431 images
* Test → 5,430 images

---

## 📉 Results

### 🔹 MobileNetV2 (Transfer Learning)

* **Accuracy**: **0.99**
* **Macro Avg F1-score**: 0.98
* **Weighted Avg F1-score**: 0.99

✅ Strong generalization across all 38 classes.

---

### 🔹 Custom CNN

* **Accuracy**: **0.96**
* **Macro Avg F1-score**: 0.94
* **Weighted Avg F1-score**: 0.96

⚠️ Some classes show lower recall/precision compared to MobileNetV2.

---

## 📊 Visualizations

* Training vs Validation Accuracy and Loss curves
* Confusion Matrix
* Sample predictions on test data

---

## ⚠️ Other Models Tried

We also experimented with VGG16 and EfficientNet for transfer learning, but they didn’t give satisfactory results on this dataset compared to MobileNetV2. Hence, MobileNetV2 was chosen as the main model.
