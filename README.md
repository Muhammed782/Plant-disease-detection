# 🌿 Plant Disease Detection using Deep Learning

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Streamlit](https://img.shields.io/badge/Streamlit-App-red)
![License](https://img.shields.io/badge/License-MIT-green)

> An AI-powered web application that detects plant diseases from leaf images using Transfer Learning (MobileNetV2). Built as a capstone project to help farmers identify crop diseases early and take timely action.

---

## 📌 Problem Statement

Crop diseases cause significant agricultural losses worldwide. Early detection is critical but requires expert knowledge that many smallholder farmers lack. This project builds an accessible AI tool that allows any farmer to photograph a plant leaf and instantly receive a disease diagnosis along with recommended treatment.

---

## 🎯 Key Features

- 📷 Upload a leaf image and get instant disease prediction
- 🧠 Powered by MobileNetV2 with Transfer Learning (38 disease classes)
- 📊 Displays prediction confidence score
- 💊 Provides treatment recommendations per detected disease
- 🌐 Simple, user-friendly Streamlit web interface

---

## 🗂️ Project Structure

```
plant-disease-detection/
│
├── data/
│   ├── raw/                  # Original PlantVillage dataset
│   └── processed/            # Preprocessed & augmented images
│
├── notebooks/
│   ├── 01_data_exploration.ipynb     # EDA and dataset analysis
│   ├── 02_preprocessing.ipynb        # Data cleaning & augmentation
│   └── 03_model_training.ipynb       # Model training & evaluation
│
├── src/
│   ├── preprocess.py         # Data loading and augmentation functions
│   ├── model.py              # MobileNetV2 model definition
│   ├── train.py              # Training script
│   └── evaluate.py           # Evaluation and metrics
│
├── app/
│   └── streamlit_app.py      # Streamlit web application
│
├── models/
│   └── plant_disease_model.h5  # Saved trained model
│
├── results/
│   ├── plots/                # Training curves, confusion matrix
│   └── metrics/              # Accuracy, precision, recall, F1 scores
│
├── docs/
│   └── final_report.pdf      # Final written report
│
├── requirements.txt          # Python dependencies
├── .gitignore
└── README.md
```

---

## 🧠 Model Architecture

- **Base Model:** MobileNetV2 (pretrained on ImageNet)
- **Technique:** Transfer Learning + Fine-tuning
- **Input:** 224 × 224 RGB leaf images
- **Output:** 38 disease/healthy classes
- **Framework:** TensorFlow / Keras

---

## 📦 Dataset

We use the **PlantVillage Dataset** available on Kaggle:
- 🔗 [https://www.kaggle.com/datasets/emmarex/plantdisease](https://www.kaggle.com/datasets/emmarex/plantdisease)
- 50,000+ labeled leaf images
- 14 crop types, 38 classes (diseases + healthy)

> **Note:** Download the dataset and place it in `data/raw/` before running the notebooks.

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/plant-disease-detection.git
cd plant-disease-detection
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Download Dataset
Download from Kaggle and place in `data/raw/`.

### 4. Run Notebooks (in order)
Open Google Colab or Jupyter and run:
- `notebooks/01_data_exploration.ipynb`
- `notebooks/02_preprocessing.ipynb`
- `notebooks/03_model_training.ipynb`

### 5. Launch the Web App
```bash
streamlit run app/streamlit_app.py
```

---

## 📊 Results

| Metric    | Score  |
|-----------|--------|
| Accuracy  | TBD    |
| Precision | TBD    |
| Recall    | TBD    |
| F1-Score  | TBD    |

> Results will be updated after model training is complete.

---

## 🛠️ Tech Stack

| Category        | Tools                            |
|----------------|----------------------------------|
| Language        | Python 3.9+                      |
| Deep Learning   | TensorFlow, Keras                |
| Data Handling   | NumPy, Pandas, OpenCV            |
| Visualization   | Matplotlib, Seaborn              |
| Web App         | Streamlit                        |
| Version Control | Git + GitHub                     |
| Training        | Google Colab (free GPU)          |

---

## 👥 Team

| Member     | Role                                      |
|------------|-------------------------------------------|
| Muhammed Sey   | Data preprocessing, Model training & evaluation |
| Ousainou Sanyang  | Streamlit app, Report writing & presentation |

---

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

## 🙏 Acknowledgements

- [PlantVillage Dataset](https://www.kaggle.com/datasets/emmarex/plantdisease) — Hughes & Salathé, 2015
- [MobileNetV2](https://arxiv.org/abs/1801.04381) — Google Research
- TensorFlow & Streamlit open-source communities
