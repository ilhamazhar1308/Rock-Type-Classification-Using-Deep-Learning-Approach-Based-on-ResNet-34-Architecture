# Rock-Type-Classification-Using-Deep-Learning-Approach-Based-on-ResNet-34-Architecture
This study develops an image-based rock type classification method using a deep learning approach with the ResNet-34 architecture. The model is designed to automatically identify lithological classes to support geological and geophysical data analysis and interpretation.
Rock Type Identification Using ResNet-34

This repository contains a deep learning–based rock identification system using the ResNet-34 architecture. The project is developed to support geology and geophysics applications, including field-based rock identification through a Streamlit web application.

⚠️ Project Status: Under active development. Model behavior, labels, and predictions may change as the dataset and training strategy evolve.

# Project Overview

Rock identification traditionally depends on expert geological interpretation. This project explores the use of deep learning and computer vision to assist lithological classification using rock images captured in the field or uploaded from files.

The system consists of:
A PyTorch training pipeline
A ResNet-34 inference model
A Streamlit-based field application with camera support

# Model Architecture

Backbone: ResNet-34
Framework: PyTorch + Hugging Face Transformers
Pretrained weights: ImageNet
Strategy:
Transfer learning
Custom classification head
Checkpoint-based inference

## Repository Structure

```
rock-type-identification/
├── train_resnet34_rocks.py
├── streamlit_app.py
├── requirements.txt
├── README.md
├── dataset/        # Image dataset (not included)
└── checkpoints/    # Trained model checkpoints
```

## Dataset Format
```
dataset/
├── Andesite/
│   ├── img1.jpg
│   ├── img2.jpg
├── Basalt/
│   ├── img1.jpg
│   ├── img2.jpg
├── Granite/
│   └── ...
```

Each directory represents one rock class.

# Installation
1️⃣ Clone Repository
git clone https://github.com/username/rock-type-identification.git
cd rock-type-identification

2️⃣ Install Dependencies
pip install -r requirements.txt

# Training (PyTorch)

Run the training script:
python train_resnet34_rocks.py
Features:
Data augmentation
Transfer learning
Periodic checkpoint saving
Resume training support

# Field Identification App (Streamlit)
🔹 Features
Upload rock image or use device camera
Top-K prediction display
Confidence threshold control
Geological interpretation logic (defined / possible)
Field-friendly interface

# Run Streamlit App
streamlit run streamlit_app.py
Then open browser at:
http://localhost:8501

# Streamlit Interface Overview

User Options:
1. Camera input (field mode)
2. Image upload
3. Top-K prediction slider

# Confidence threshold control

Prediction Output:
Predicted rock type(s)
Confidence percentage
Geological decision logic:
🟢 Defined (high confidence)
🟡 Possible (ambiguous class)
⚠️ Final validation should always be confirmed through field observation and petrographic/mineralogical analysis.

# Checkpoint Usage

The Streamlit app loads trained checkpoints:
```
checkpoints/
└── checkpoint_20.pth
```
Checkpoint contains:
Model weights
Class names
Training metadata

# Application Scope

Field geology assistance
Geophysical interpretation support
Academic research
Computer vision for Earth sciences

# Current Development Status

✅ Training pipeline implemented
✅ ResNet-34 inference
✅ Streamlit field application
🚧 Model validation & evaluation
🚧 Dataset refinement

# Disclaimer

This system is intended as a decision-support tool only.
It does not replace expert geological judgment.

👤 Author

Ilham Azhar, Laurens roy, Muhammad Nabil, Putri permata
Field: Geology & Geophysics
Focus: Deep Learning for Earth Science Applications
