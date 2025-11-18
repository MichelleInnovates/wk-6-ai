# wk-6-ai
# 🤖 Edge AI Recyclable Classifier

![TensorFlow Lite](https://img.shields.io/badge/Uses-TensorFlow%20Lite-orange)
![Python 3.9+](https://img.shields.io/badge/Python-3.9%2B-blue)
![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-brightgreen)

This project is a prototype for an **Edge AI** system. It uses a lightweight convolutional neural network (CNN) trained to classify images of trash into recyclable, organic, and general waste.

The model is converted to **TensorFlow Lite (`.tflite`)**, making it small, fast, and perfect for running directly on low-power devices like a Raspberry Pi or a smart trash bin, with no internet connection required.



## 📋 Table of Contents

* [Features](#-features)
* [Installation](#-installation)
* [Usage](#-usage)
* [Project Workflow](#-project-workflow)
* [Why Edge AI?](#-why-edge-ai)
* [License](#-license)

## ✨ Features

* **Image Classification:** Identifies items from images.
* **Lightweight Model:** Converted to `.tflite` for high performance and a small file size.
* **Offline Capable:** Runs 100% on-device, enhancing privacy and reducing latency.

## 🚀 Installation

To set up this project locally, clone the repository and install the required Python libraries.

1.  **Clone this repository:**
    ```bash
    git clone [https://github.com/your-username/edge-ai-classifier.git](https://github.com/your-username/edge-ai-classifier.git)
    cd edge-ai-classifier
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Install dependencies:**
    This project requires TensorFlow (for training) and Kaggle (for the dataset).
    ```bash
    pip install tensorflow numpy matplotlib kaggle
    ```

4.  **Download the dataset:**
    (Assumes you have your `kaggle.json` API key ready.)
    ```bash
    kaggle datasets download -d mostafaabla/garbage-classification
    unzip -q garbage-classification.zip
    ```

## 💻 Usage

There are two main parts to this project: training the model and converting it.

### 1. Train the Full Model

Run the `train.py` script to train the CNN on the downloaded dataset. This will save a standard Keras model (`full_model.h5`).

```bash
python train.py