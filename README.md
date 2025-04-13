# Project title:
  Number plates detection using YOLO11

## intro:
 This project focuses on detecting vehicle number plates using the powerful object detection model YOLOv11 (You Only Look Once, version 11). YOLOv11 is known for its real-time performance and high accuracy, making it an excellent choice for applications such as traffic surveillance, automated toll systems, parking management, and law enforcement.

By training YOLOv11 on a custom dataset of vehicles and number plates, the model can accurately identify and locate number plates in both images and videos. The training pipeline includes data preprocessing, augmentation, and fine-tuning to enhance detection performance.

Key Features:

🧠 Built with YOLOv11 for fast and accurate number plate detection

📦 Trained on a custom annotated dataset

📸 Supports both image and video input

⚡ Real-time inference with high precision and recall

🔧 Easily customizable for different regions or plate formats


## 📁 Dataset

The dataset contains images of vehicles with annotated bounding boxes around their number plates. You can use Roboflow to label and export your dataset in YOLO format.

## 🧠 Model

YOLOv11 is the latest version of the YOLO family, offering improved speed and accuracy. This model was fine-tuned using transfer learning on the custom dataset of number plates.

# 🛠️ Setup Instructions:
1. Clone the repository:
    git clone https://github.com/MrHasnain2522/number-plate-detection-yolov11.git

2. Install dependencies:
   pip install -r requirements.txt

3. Download or prepare your dataset:

Label your dataset using Roboflow or another tool
Export in YOLOv11 format
Place dataset inside datasets/ directory

4. Train the model:
   python train.py --img 640 --batch 16 --epochs 20 --data dataset.yaml --cfg yolov11.yaml --weights yolov11.pt

5. Run detection:
   python detect.py --weights runs/train/exp/weights/best.pt --img 640 --source path/to/your/image_or_video

## 📊 Training Results

Final mAP50: 85.7%

mAP50-95: 63.9%

Precision: 92.5%

Recall: 77.3%

# 📦 Output Samples

Detected number plates will be saved in the runs/detect/exp/ folder.

# 🤖 Tools Used

Python

PyTorch

YOLOv11

Roboflow (for annotation and preprocessing)

