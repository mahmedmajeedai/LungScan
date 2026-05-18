<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a1a0a,40:1a3a1a,70:2d6a2d,100:0a1a0a&height=200&section=header&text=LungScan&fontSize=72&fontColor=ffffff&fontAlignY=38&fontStyle=bold&desc=COVID-19%20Detection%20from%20Chest%20X-Rays%20via%20Deep%20Learning&descSize=16&descAlignY=62&descColor=b7e4c7" width="100%"/>

<br/>

<p align="center">
  <img src="https://img.shields.io/badge/Keras%20%2F%20TensorFlow-CNN%20Training-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white"/>
  <img src="https://img.shields.io/badge/Transfer%20Learning-VGG%20%7C%20ResNet-2d6a2d?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Grid%20Search%20CV-Hyperparameter%20Tuning-green?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Input-Chest%20X--Ray%20Images-gray?style=for-the-badge"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Notebooks-3%20Approaches-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/Augmentation-ImageDataGenerator-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Domain-Medical%20Imaging%20AI-red?style=flat-square"/>
</p>

<br/>

> **LungScan** is a three-notebook deep learning study on COVID-19 detection from chest X-ray images — progressing from a custom CNN baseline, to pretrained model transfer learning, to full hyperparameter tuning with Grid Search Cross Validation.

</div>

---

## 📓 Three-Notebook Progression

This project is structured as a deliberate learning progression, each notebook building on the previous:

### Notebook 1 — Custom CNN (`Covid-19 Diagnose.ipynb`)

A Convolutional Neural Network built from scratch using Keras Sequential API.

```
Input X-Ray Image
       │
Conv2D (ReLU) → MaxPooling2D
Conv2D (ReLU) → MaxPooling2D
Flatten
Dense (ReLU) → Dense (Softmax)
       │
  COVID / Normal / Pneumonia
```

Training: Adam optimiser, categorical cross-entropy loss, 25 epochs with data augmentation.

### Notebook 2 — Pretrained Models (`Diagnose using Pre-trained Models.ipynb`)

Transfer learning using pretrained architectures (VGG16, ResNet) as frozen feature extractors. A new classification head is trained on top — significantly fewer epochs needed, higher accuracy from day one.

```
Pretrained CNN (frozen weights)
       │ Feature extraction
Custom Dense Head (trained)
       │
  COVID / Normal
```

### Notebook 3 — Grid Search CV (`Using Grid Search Cross Validation.ipynb`)

Systematic hyperparameter search across optimisers, learning rates, batch sizes, and dropout rates using `GridSearchCV` with Keras wrappers. Finds the optimal configuration for the best test accuracy.

---

## 🛠️ Tech Stack

| Library | Role |
|---|---|
| `tensorflow` / `keras` | Model building, training, and evaluation |
| `ImageDataGenerator` | Real-time data augmentation (flip, zoom, rotation) |
| `scikit-learn` | Grid Search CV, train-test split, metrics |
| `numpy` / `matplotlib` | Data manipulation and training visualisation |

---

## 📦 Dataset

Chest X-ray images organised into three classes:

```
Covid-19/
  ├── train/
  │   ├── COVID/
  │   ├── Normal/
  │   └── Pneumonia/
  └── test/
      ├── COVID/
      ├── Normal/
      └── Pneumonia/
```

---

## 🚀 Quickstart

```bash
git clone https://github.com/mahmedmajeedai/Covid-19-Diagnose-using-lungs-X-Rays-and-Pre-trained-Model.git
cd Covid-19-Diagnose-using-lungs-X-Rays-and-Pre-trained-Model
pip install tensorflow scikit-learn numpy matplotlib pillow
jupyter notebook
```

Run the notebooks in order: custom CNN → pretrained → Grid Search CV.

---

## 📊 What Each Notebook Teaches

| Notebook | Core Concept |
|---|---|
| Custom CNN | Building and training a CNN from scratch |
| Pretrained Models | Transfer learning and feature extraction |
| Grid Search CV | Systematic hyperparameter optimisation |

---

## ⚠️ Medical Disclaimer

LungScan is a research and educational deep learning project. It is not a clinical diagnostic tool and must not be used as a substitute for professional radiological evaluation or medical judgement.

---

<div align="center">

**Built by [Muhammad Ahmed Majeed](https://github.com/mahmedmajeedai)**

*COVID-19 chest X-ray classification via custom CNN, transfer learning, and hyperparameter tuning*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2d6a2d,50:1a3a1a,100:0a1a0a&height=80&section=footer" width="100%"/>

</div>
