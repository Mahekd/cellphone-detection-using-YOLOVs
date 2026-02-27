# Cellphone Detection in Classroom using YOLOv5s

This project implements a deep learning–based object detection system to detect cellphone usage in classroom environments using YOLOv5s.

The model identifies mobile phones in classroom images and video frames and highlights them with bounding boxes.

## Project Overview

With increasing smartphone usage, maintaining student attention in classrooms has become challenging.  
This project aims to assist teachers by automatically detecting cellphones in classroom settings using computer vision.

The system was trained on a custom annotated dataset in YOLO format and supports both PyTorch and ONNX-based inference.

## Model Details

- **Architecture:** YOLOv5s  
- **Framework:** PyTorch  
- **Task:** Object Detection  
- **Class Detected:** Cellphone  
- **Export Format:** ONNX (for deployment)
  
## Dataset

The annotated dataset used for training is hosted on Hugging Face:

🔗 **Dataset Link:**  
https://huggingface.co/datasets/MahekDharod/cellphone-detection-dataset/tree/main

Dataset Information: 
The dataset contains classroom images with bounding box annotations for cellphones in YOLO format.

⚠️ Note: This is a limited dataset created for academic purposes.
If you would like to expand the dataset, you can create your own annotations using tools such as Label Studio:
🔗 https://labelstud.io
Label Studio allows you to:
Upload custom images
Draw bounding boxes
Export annotations in YOLO format
Prepare datasets for training object detection models
Retrain and improve the YOLOv5 model with additional data

### Dataset Structure:
images/
labels/
data.yaml

## Trained Model

The trained YOLOv5s model weights are hosted on Hugging Face:

🔗 **Model Repository:**  
https://huggingface.co/MahekDharod/cellphone-detection-yolov5s

### Available Files:

- `yolov5s.pt` → PyTorch training weights  
- `best.onnx` → Deployment-ready model (OpenCV-DNN compatible)

## ⚙ Installation

Clone this repository:

```bash
git clone https://github.com/YOUR_USERNAME/cellphone-detection-yolov5s.git
cd cellphone-detection-yolov5s
Install dependencies:
pip install -r requirements.txt
🚀 Running Inference
Option 1: Using PyTorch (.pt file)
import torch

model = torch.hub.load('ultralytics/yolov5', 'custom', path='yolov5s.pt')
results = model('test_image.jpg')
results.show()
Option 2: Using ONNX (OpenCV-DNN)
import cv2

net = cv2.dnn.readNetFromONNX("best.onnx")
📂 Project Structure
cellphone-detection-yolov5s/
│
├── cellphone_detection.ipynb   # Training & inference notebook
├── requirements.txt            # Required dependencies
├── README.md                   # Project documentation

🎯 Applications
Smart classroom monitoring systems
Student distraction detection
Real-time surveillance analysis
Academic computer vision projects

📊 Future Improvements
Real-time classroom video integration
Student identification (face recognition integration)
Alert system for teachers
Web-based live demo interface
