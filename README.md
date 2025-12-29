# Rock Type Classification Using Deep Learning  ResNet-34 Architecture–Based Approach

This project presents an image-based rock type classification system using a deep learning approach built on the **ResNet-34 architecture**.  
The model is designed to automatically identify lithological classes from rock images to support geological and geophysical data analysis and interpretation.

---

⚠️ **Project Status:** Under active development  
Model behavior, class labels, and predictions may evolve as the dataset and training strategy are further refined.

---

## 📌 Project Overview

Rock identification traditionally relies on expert geological interpretation through field observation and laboratory analysis.  
This project explores the application of **computer vision and deep learning** to assist preliminary lithological classification using macroscopic rock images captured in the field or uploaded from files.

The system is intended as a **decision-support tool**, not a replacement for professional geological judgment.

The project consists of:

- A **PyTorch-based training pipeline**
- A **ResNet-34 inference model**
- A **Streamlit-based field identification application** with image upload and camera support

---

## 🧠 Model Architecture

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

## 🪨 Rock Classes

The dataset includes 53 lithological classes such as:

Amphibolite, Andesite, Basalt, Granite, Gneiss, Limestone, Marble, Sandstone, Shale, Slate, Tuff, Travertine, Quartzite, Rhyolite, and others.

---

## 📂 Repository Structure

rock-type-identification/
├── train_resnet34_rocks.py # Model training script
├── streamlit_app.py # Streamlit application
├── model.py # Model definition & loader
├── requirements.txt # Python dependencies
├── README.md
├── dataset/ # Rock image dataset (not included)
└── checkpoints/ # Trained model checkpoints

yaml
Copy code

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
yaml
Copy code

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
bash
Copy code
pip install -r requirements.txt
```
🏋️ Training (PyTorch)
Run the training script:

bash
Copy code
python train_resnet34_rocks.py
Training features:

Data augmentation

Transfer learning

Periodic checkpoint saving

Resume training from checkpoint

📸 Field Identification App (Streamlit)
An interactive Streamlit web application is provided for rock classification in both laboratory and field environments.

Features:
Image upload or camera input

Top-K prediction display

Adjustable confidence threshold

Geological interpretation guidance

Lightweight, field-friendly interface

▶️ Run Streamlit App
bash
Copy code
streamlit run streamlit_app.py
Then open your browser at:

arduino
Copy code
http://localhost:8501
🔍 Streamlit Interface Overview
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

📦 Checkpoint Usage
The Streamlit application automatically loads trained checkpoints from:

Copy code
checkpoints/
└── checkpoint_*.pth
Each checkpoint contains:

Model weights

Training metadata

Class information

🎯 Application Scope
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

👨‍💻 Authors
Ilham Azhar

Laurens Roy

Muhammad Nabil

Putri Permata

Field: Geology & Geophysics
Focus: Deep Learning for Earth Science Applications

markdown
Copy code

---

## ✅ HASIL AKHIR

✔ Sudah **satu README utuh**  
✔ Konsisten dengan **ResNet-34 + Streamlit**  
✔ Siap untuk **GitHub publik + dosen + reviewer**  
✔ Aman karena **dataset & model via Google Drive**

Jika mau, saya bisa:
- 🔹 Menyesuaikan ke **format paper/jurnal**
- 🔹 Menambahkan **citation / BibTeX**
- 🔹 Menyederhanakan untuk **Streamlit Cloud deployment**

Tinggal bilang 👍






You said:
BUAT JUGA STEP BY STEP MEMBUKA STREAMLIT NYA DARI DRIVE, DOWNLOAD LALU KE VSCODE


ChatGPT said:
Siap 👍
Berikut STEP-BY-STEP GUIDE (English) untuk membuka Streamlit app dari Google Drive → download → jalankan di VS Code, siap langsung kamu tambahkan ke README.md.

Kamu bisa tempel di bagian baru README, misalnya setelah bagian Google Drive Files.

▶️ Running the Streamlit App from Google Drive (Step-by-Step)
This section explains how to run the Streamlit application starting from files shared via Google Drive.

Step 1 — Download Project Files from Google Drive
Open the Google Drive link provided in this repository.

Download the project folder as a ZIP file.

Extract the ZIP file to a local directory, for example:

graphql
Copy code
D:\Rock-Type-Classification-Streamlit\
Step 2 — Open the Project in VS Code
Open Visual Studio Code.

Click File → Open Folder.

Select the extracted project directory.

Ensure the folder contains files such as:

app.py

`







You said:
BUAT DAN SATUKAN DI README.MD DENGAN TEKS SEBELUMNYA


ChatGPT said:
Baik 👍
Berikut README.md versi lengkap, rapi, dan sudah DISATUKAN, termasuk step-by-step menjalankan Streamlit dari Google Drive → download → VS Code.
Tinggal copy–paste langsung ke README.md di GitHub kamu.

Rock-Type-Classification-Using-Deep-Learning-Approach-Based-on-ResNet-34-Architecture
This study develops an image-based rock type classification method using a deep learning approach based on the ResNet-34 architecture. The system is designed to support geological and geophysical analysis by assisting lithological identification from rock images.

⚠️ Project Status: Under active development. Model behavior, labels, and predictions may change as the dataset and training strategy evolve.

Project Overview
Rock identification traditionally relies on expert geological interpretation in the field and laboratory. This project explores the application of deep learning and computer vision to assist lithological classification using rock images captured in the field or uploaded from files.

The system consists of:

A PyTorch-based training pipeline

A ResNet-34 inference model

A Streamlit-based field application with optional camera input

Model Architecture
Backbone: ResNet-34

Framework: PyTorch

Pretrained Weights: ImageNet

Training Strategy:

Transfer learning

Custom classification head

Checkpoint-based training and inference

Repository / Project Structure
graphql
Copy code
rock-type-classification/
├── app.py                     # Streamlit application
├── model.py                   # ResNet-34 model loader
├── requirements.txt           # Python dependencies
├── README.md
├── Rocks/                     # Image dataset (not included in repo)
│   ├── Andesite/
│   ├── Basalt/
│   ├── Granite/
│   └── ...
└── Checkpoints_Rocks_FINAL/   # Trained model checkpoints (.pth)
Dataset Format
Copy code
Rocks/
├── Andesite/
│   ├── img1.jpg
│   ├── img2.jpg
├── Basalt/
│   ├── img1.jpg
│   ├── img2.jpg
├── Granite/
│   └── ...
Each folder represents one rock class.

Installation (Local Environment)
1️⃣ Create and Activate Environment (Recommended)
Using Conda:

lua
Copy code
conda create -n rockai python=3.8
conda activate rockai
Or using virtualenv:

nginx
Copy code
python -m venv rockai
rockai\Scripts\activate
2️⃣ Install Dependencies
css
Copy code
pip install -r requirements.txt
Training (PyTorch)
Run the training script:

nginx
Copy code
python train_resnet34_rocks.py
Training features:

Data augmentation

Transfer learning

Periodic checkpoint saving

Resume training from checkpoint

Field Identification App (Streamlit)
Key Features
Upload rock image or use device camera

Top-K prediction results

Adjustable confidence threshold

Geological interpretation logic for field usage

Lightweight and field-friendly interface

▶️ Running Streamlit App from Google Drive (Step-by-Step)
This guide explains how to run the Streamlit application using files shared via Google Drive.

Step 1 — Download from Google Drive
Open the Google Drive link provided in this repository.

Download the project folder as a ZIP file.

Extract the ZIP file to a local directory, for example:

graphql
Copy code
D:\Rock-Type-Classification-Streamlit\
Step 2 — Open Project in VS Code
Open Visual Studio Code.

Click File → Open Folder.

Select the extracted project folder.

Make sure the folder contains:

app.py

model.py

requirements.txt

Checkpoints_Rocks_FINAL/

Rocks/

Step 3 — Install Dependencies
Open Terminal in VS Code:

nginx
Copy code
Ctrl + `
Then run:

css
Copy code
pip install -r requirements.txt
Step 4 — Run Streamlit Application
In the VS Code terminal:

arduino
Copy code
streamlit run app.py
Then open your browser at:

arduino
Copy code
http://localhost:8501
Streamlit Interface Overview
User Options
Upload image from file

Camera input (field mode ON/OFF)

Top-K prediction control

Confidence threshold adjustment

Prediction Output
Predicted rock type(s)

Confidence percentage

Geological interpretation logic:

🟢 Defined (high confidence)
🟡 Possible (ambiguous class)
⚠️ Final validation should always be confirmed through field observation and petrographic/mineralogical analysis

Checkpoint Usage
The Streamlit app automatically loads the latest checkpoint from:

Copy code
Checkpoints_Rocks_FINAL/
├── checkpoint_55.pth
├── checkpoint_125.pth
└── ...
Checkpoint contains:

Model weights

Training metadata

Application Scope
Field geology assistance

Geophysical interpretation support

Academic research

Computer vision for Earth science applications

Disclaimer
This system is intended as a decision-support tool only.
It does not replace expert geological judgment or laboratory analysis.

Authors
Ilham Azhar

Laurens Roy

Muhammad Nabil

Putri Permata

Field: Geology & Geophysics
Focus: Deep Learning for Earth Science Applications
