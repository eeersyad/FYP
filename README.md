# Paddy Leaf Disease Detection Using Machine Learning 🌾

## Overview

This repository contains the complete source code, model training scripts, and Streamlit web application for an automated paddy leaf disease detection system. Developed as a Final Year Project for the Bachelor of Information Systems (Hons.) Intelligent System Engineering at Universiti Teknologi MARA (UiTM), this project leverages Deep Convolutional Neural Networks (DCNN) to assist farmers and agricultural specialists in diagnosing crop diseases quickly and accurately.

Manual detection of paddy diseases is time-consuming and prone to human error. This system provides a real-time, user-friendly diagnostic tool to improve crop yield and support agricultural food security.

## Features

* **High-Accuracy Classification:** Identifies 6 distinct classes of paddy leaf conditions (5 diseases + 1 healthy).


* **Web-Based Interface:** A lightweight, interactive prototype built with Streamlit for seamless image uploading and real-time inference.


* **Actionable Insights:** Displays the predicted disease alongside elementary recommendations for disease management.



## Dataset

The model was trained on a dataset of 2,628 augmented RGB images of paddy leaves, originally sourced from Kaggle (created by Dede Ikhsan Dwi Saputra). The dataset is categorized into the following six classes:

* Bacterial Leaf Blight


* Brown Spot


* Leaf Blast


* Leaf Scald


* Narrow Brown Spot


* Healthy



*(Note: The raw dataset is not included in this repository to conserve space. Please refer to the Kaggle link to download the original images.)*

## Model Performance & Methodology

Four transfer learning models were evaluated: MobileNet, VGG16, Xception, and ResNet50. Models were trained using TensorFlow/Keras on Google Colab with varied data split ratios and batch sizes.

**Xception** was selected as the final production model, achieving the highest performance metrics during the 8:1:1 data split and batch size 16 experimentations:

* **Accuracy:** 98.11%


* **Precision:** 0.98


* **Recall:** 0.97


* **F1-Score:** 0.97



## System Architecture

* **Frontend:** Streamlit (Python)


* **Backend Inference:** TensorFlow / Keras


* **Input:** 224x224 pixel image requirements handled automatically via backend preprocessing.



## Installation and Local Setup

1. **Clone the repository:**
```bash
git clone https://github.com/yourusername/paddy-disease-detection.git
cd paddy-disease-detection

```


2. **Install the required dependencies:**
```bash
pip install -r requirements.txt

```


3. **Download the model weights:**
Download the `xception_model.h5` file from [Link to Google Drive/External Host] and place it in the `models/` directory.
4. **Run the Streamlit prototype:**
```bash
streamlit run app.py

```



## Repository Structure

```text
├── app.py                 # Streamlit application script
├── notebooks/             # Google Colab Jupyter Notebooks for training
├── models/                # Directory for saved .h5 model weights
├── requirements.txt       # Python dependencies (TensorFlow, Streamlit, etc.)
└── README.md              # Project documentation

```

## Author

**Ahmad Irsyad Qayyum Bin Mohd Azam**


Universiti Teknologi MARA (UiTM) Shah Alam
Bachelor of Information Systems (Hons.) Intelligent System Engineering
