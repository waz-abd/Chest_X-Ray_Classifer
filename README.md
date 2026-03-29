# 🫁 Chest X-Ray Pulmonary Disease Classifier
*A Deep Learning Multi-Class Chest X-Ray Classifier built with TensorFlow & Keras*

---

## 💡 About This Project

**Chest X-Ray Pulmonary Disease Classifier** is a deep learning project that classifies chest X-ray images into six distinct pulmonary disease categories using a Convolutional Neural Network (CNN) built from scratch with TensorFlow and Keras.

Built as the final project for **MBAI 5310G – AI Programming** at Ontario Tech University (Winter 2026).

> ⚠️ **Disclaimer:** This model is strictly for **educational and research purposes**.  
> It must **not** be used for any clinical, diagnostic, or treatment-related decisions.

---

## 🧩 Disease Classes

| Class | Description |
|---|---|
| **COVID-19** | Bilateral ground-glass opacities and peripheral lung involvement |
| **Emphysema** | Hyperinflation, flattened diaphragms, reduced vascular markings |
| **Normal** | Healthy chest X-rays with clear lung fields |
| **Pneumonia-Bacterial** | Localized lobar consolidations from bacterial infection |
| **Pneumonia-Viral** | Diffuse interstitial infiltrates from viral infection |
| **Tuberculosis** | Upper lobe fibrotic scarring or cavitations |

---

## 📁 Dataset

**ChestX6: Multi-Class X-ray Dataset** by Mohamed Asak (2024)  
📦 [Kaggle Dataset](https://www.kaggle.com/datasets/mohamedasak/chest-x-ray-6-classes-dataset)

| Split | Images |
|---|---|
| Training | 14,551 |
| Validation | 1,748 |
| Test | 1,737 |
| **Total** | **18,036** |

- Image format: JPG / PNG
- Image size: 224 × 224 pixels (pre-resized)
- Color space: Grayscale

---

## 🏗️ Model Architecture

A custom 4-block CNN built from scratch:

```
Input (224x224x3)
  → Conv2D(32) + BatchNorm + MaxPooling
  → Conv2D(64) + BatchNorm + MaxPooling
  → Conv2D(128) + BatchNorm + MaxPooling
  → Conv2D(256) + BatchNorm + MaxPooling
  → Flatten
  → Dense(256) + Dropout(0.5)
  → Dense(6, softmax)
```

**Total Parameters:** ~9.8 million

---

## 📊 Results

| Class | Precision | Recall | F1-Score |
|---|---|---|---|
| Covid-19 | 0.74 | 0.72 | 0.73 |
| Emphysema | 0.69 | 0.72 | 0.71 |
| Normal | 0.71 | 0.98 | 0.82 |
| Pneumonia-Bacterial | 0.70 | 0.50 | 0.58 |
| Pneumonia-Viral | 0.59 | 0.56 | 0.58 |
| Tuberculosis | 1.00 | 0.94 | 0.97 |

**Overall Test Accuracy: 74%** | **Macro F1-Score: 0.73**

---

## 🚀 How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/waz-abd/Chest_X-Ray_Classifer.git
```

### 2. Open in Google Colab
Upload `Chest_X_Ray_Classifer.ipynb` to [Google Colab](https://colab.research.google.com/) and enable **T4 GPU** (Runtime → Change runtime type → T4 GPU).

### 3. Upload the Dataset
- Download the dataset zip from [Kaggle](https://www.kaggle.com/datasets/mohamedasak/chest-x-ray-6-classes-dataset)
- Upload the zip file via the Colab file panel
- The notebook will unzip and load it automatically

### 4. Run All Cells
Run the notebook cells in order from top to bottom.

---

## 🛠️ Libraries Used

| Library | Purpose |
|---|---|
| TensorFlow / Keras | Model building and training |
| NumPy | Numerical operations |
| Matplotlib | Visualizations |
| scikit-learn | Evaluation metrics |

---

## 📂 Project Structure

```
Chest_X-Ray_Classifer/
│
├── Chest_X_Ray_Classifer.ipynb   # Main notebook
├── README.md                      # Project documentation
```

---

## 👤 Author

**Abdul Wasay**  
Master of Business Analytics and AI — Ontario Tech University  
MBAI 5310G – AI Programming | Winter 2026
