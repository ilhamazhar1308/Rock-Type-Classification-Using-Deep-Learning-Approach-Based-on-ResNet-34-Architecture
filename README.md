# Rock Type Classification Using Deep Learning  ResNet-34 Architecture–Based Approach

This project presents an image-based rock type classification system using a deep learning approach built on the **ResNet-34 architecture**.  
The model is designed to automatically identify lithological classes from rock images to support geological and geophysical data analysis and interpretation.

---

⚠️ **Project Status:** Under active development  
Model behavior, class labels, and predictions may evolve as the dataset and training strategy are further refined.

---

## Project Overview

Rock identification traditionally relies on expert geological interpretation through field observation and laboratory analysis.  
This project explores the application of **computer vision and deep learning** to assist preliminary lithological classification using macroscopic rock images captured in the field or uploaded from files.

The system is intended as a **decision-support tool**, not a replacement for professional geological judgment.

The project consists of:

- A **PyTorch-based training pipeline**
- A **ResNet-34 inference model**
- A **Streamlit-based field identification application** with image upload and camera support

---

## Model Architecture

- **Backbone:** ResNet-34  
- **Framework:** PyTorch  
- **Pretrained weights:** ImageNet  
- **Training strategy:**
  - Transfer learning
  - Custom classification head
  - Partial fine-tuning (final residual block)
  - Checkpoint-based training and inference

The model is trained to classify **53 rock types**, covering igneous, sedimentary, and metamorphic lithologies.

---

## Rock Classes

The dataset includes 53 lithological classes such as:

Amphibolite, Andesite, Basalt, Granite, Gneiss, Limestone, Marble, Sandstone, Shale, Slate, Tuff, Travertine, Quartzite, Rhyolite, and others.

---

## Repository Structure
```
rock-type-identification/
├── train_resnet34_rocks.py # Model training script
├── streamlit_app.py # Streamlit application
├── model.py # Model definition & loader
├── requirements.txt # Python dependencies
├── README.md
├── dataset/ # Rock image dataset (not included)
└── checkpoints/ # Trained model checkpoints
```

---

## Dataset Format
```
dataset/
├── Andesite/
│ ├── img1.jpg
│ ├── img2.jpg
├── Basalt/
│ ├── img1.jpg
│ ├── img2.jpg
├── Granite/
│ └── ...
```

Each subdirectory represents one rock class.

---

## Project Files (Google Drive)

Due to large file sizes, trained checkpoints, datasets, and Streamlit files are hosted on Google Drive.

🔗 **Google Drive Link:**  
https://drive.google.com/drive/folders/1OYMSHvCee2RlpOfU93G6PDBw1d3mvSBZ?usp=sharing

Contents include:
- Streamlit application files (`app.py`, `model.py`)
- Trained model checkpoints (`checkpoint_*.pth`)
- Rock image dataset
- Supporting files

---

## Installation

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/rock-type-identification.git
cd rock-type-identification
```
2️⃣ Install Dependencies
```
pip install -r requirements.txt
```
# Training (PyTorch)
Run the training script:
```
python train_resnet34_rocks.py
```
Training features:

Data augmentation

Transfer learning

Periodic checkpoint saving

Resume training from checkpoint

# Field Identification App (Streamlit)
An interactive Streamlit web application is provided for rock classification in both laboratory and field environments.

Features:
Image upload or camera input

Top-K prediction display

Adjustable confidence threshold

Geological interpretation guidance

Lightweight, field-friendly interface

# Run Streamlit App
```
streamlit run streamlit_app.py
```
Then open your browser at:

```
http://localhost:8501
```
# Streamlit Interface Overview
User Options:
Camera input (field mode)

Image upload

Top-K prediction slider

Confidence threshold control

Prediction Output:
Predicted rock type(s)

Confidence percentage

Geological interpretation logic:

🟢 Defined — High confidence prediction

🟡 Possible — Ambiguous class

⚠️ Final validation should always be confirmed through field observation and petrographic/mineralogical analysis

# Checkpoint Usage
The Streamlit application automatically loads trained checkpoints from:

```
checkpoints/
└── checkpoint_*.pth
```
Each checkpoint contains:

Model weights

Training metadata

Class information

# Application Scope
Field geology assistance

Geophysical interpretation support

Academic research and education

Computer vision applications in Earth sciences

🚧 Current Development Status

✅ Training pipeline implemented

✅ ResNet-34 inference model

✅ Streamlit field application

🚧 Model validation and performance evaluation

🚧 Dataset expansion and refinement

⚠️ Disclaimer
This system is intended for research and educational purposes only.

It should not be used as the sole basis for geological or engineering decisions.

# Authors
Ilham Azhar

Laurens Roy

Muhammad Nabil

Putri Permata

Field: Geology & Geophysics
Focus: Deep Learning for Earth Science Applications

# LICENSE
MIT License

Copyright (c) 2025 Ilham Azhar

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
---
