# Rock-Type-Classification-Using-Deep-Learning-Approach-Based-on-ResNet-34-Architecture
This study develops an image-based rock type classification method using a deep learning approach with the ResNet-34 architecture. The model is designed to automatically identify lithological classes to support geological and geophysical data analysis and interpretation.

📌 Project Overview

Rock type identification traditionally relies on expert interpretation, which can be time-consuming when handling large image datasets. This project explores the use of Convolutional Neural Networks (CNN) with transfer learning to assist rock classification using image data.

The model is implemented in PyTorch and trained using image datasets organized by rock classes.

🧠 Model Architecture

Backbone: ResNet-34
Pretrained weights: ImageNet
Transfer learning with:
Frozen backbone layers
Fine-tuning on the final convolutional block (layer4)
Custom fully connected (FC) classifier head

📂 Dataset Structure

The dataset must be organized as follows:
Rocks/
├── Class_1/
│   ├── img1.jpg
│   ├── img2.jpg
├── Class_2/
│   ├── img1.jpg
│   ├── img2.jpg
├── Class_3/
│   └── ...


Each folder represents one rock type (class).

⚙️ Features

Data augmentation (rotation, flip, color jitter, perspective)
Train–test split (80% / 20%)
Checkpoint saving every 5 epochs
Resume training from latest checkpoint
Image prediction with confidence score
Top-k prediction output

🚀 How to Run (Google Colab)

Upload the notebook (.ipynb) to Google Colab
Mount Google Drive
Set dataset path:
data_dir = "/content/drive/MyDrive/Rocks"
Run all cells sequentially
Use the prediction function:
predict_image_with_photo("path_to_image.jpg")

🧪 Prediction Output

The prediction module:
Displays the input image
Shows predicted class and confidence
Outputs top-k class probabilities
Warns when confidence is low

📦 Dependencies

Python 3.x
PyTorch
Torchvision
NumPy
Matplotlib
PIL
tqdm
Install dependencies (if needed):
pip install torch torchvision matplotlib tqdm pillow

📌 Current Status

✅ Model training pipeline implemented
✅ Checkpointing system
✅ Image prediction module
🚧 Performance evaluation and optimization in progress
🚧 Dataset expansion planned

📖 License

This project is intended for academic and research purposes.
License can be added later (e.g., MIT License).

👤 Author

Developed by Ilham Azhar
Field: Geology & Geophysics
Focus: Deep Learning Applications in Earth Sciences
