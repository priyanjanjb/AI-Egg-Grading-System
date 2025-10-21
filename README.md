# 🥚 Egg Grading System using YOLOv8

This project presents an intelligent **egg grading and quality detection system** developed using **Ultralytics YOLOv8**, a cutting-edge object detection framework.  
The system automates the traditional egg grading process by detecting and classifying eggs based on their surface quality (such as *clean*, *cracked*, or *dirty*), enabling faster, more consistent, and reliable results in the poultry industry.

---

## 🎯 Project Objective

Manual egg grading is often time-consuming and inconsistent due to human subjectivity.  
The main goal of this research is to **develop an automated computer vision-based system** that:
- Detects eggs in real-time from images or videos  
- Classifies eggs into quality-based categories  
- Provides performance metrics to evaluate model efficiency  

---

## 🚀 Key Features

- 🧠 **YOLOv8-powered detection** for high-speed, real-time performance  
- 🥚 Classifies eggs as *Clean*, *Cracked*, or *Dirty*  
- ☁️ **Training on Google Colab** with Google Drive integration  
- 📊 Includes **precision, recall, mAP, and loss curves** visualizations  
- 🧩 Modular and scalable for integration into industrial grading systems  
- 💾 Trained model exported for easy deployment and inference  

---

## 🧩 Technologies Used

| Category | Tools / Libraries |
|-----------|------------------|
| Framework | [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics) |
| Language | Python |
| Environment | Google Colab |
| Deep Learning | PyTorch |
| Visualization | Matplotlib, Seaborn |
| Storage | Google Drive |
| Hardware | GPU runtime (Google Colab Pro) |

---

yaml
Copy code
---

## ⚙️ Setup and Installation

### 1. Open in Google Colab  
You can easily run this project in **Google Colab** without any local setup.

### 2. Install Dependencies
```bash
!pip install ultralytics tqdm
3. Verify Installation
python
Copy code
import ultralytics
ultralytics.checks()
4. Mount Google Drive
python
Copy code
from google.colab import drive
drive.mount('/content/drive')
🧠 Model Training
Train the YOLOv8 model with your dataset using:

bash
Copy code
!yolo task=detect mode=train model=yolov8n.pt data=/content/drive/MyDrive/EggGradingFYP/data.yaml epochs=10 batch=32 project=/content/drive/MyDrive/EggGradingFYP/result name=egg
📈 Training Results
Metric	Value
Precision	0.919
Recall	0.913
mAP@0.5	0.974
mAP@0.5:0.95	0.973
Epochs	10

Training results, metrics, and plots can be found in:

swift
Copy code
/content/drive/MyDrive/EggGradingFYP/result/egg
🔍 Model Inference (Prediction)
Use the trained model to make predictions:

bash
Copy code
!yolo task=detect mode=predict model=/content/drive/MyDrive/EggGradingFYP/result/egg/weights/best.pt source=/content/drive/MyDrive/EggGradingFYP/test/images
The predictions are saved in the /runs/detect/predict/ folder.

📸 Sample Outputs
Image	Classification
🥚	Clean Egg
🥚	Cracked Egg
🥚	Dirty Egg

(You can include screenshots of your model predictions here.)

📊 Performance Summary
The YOLOv8-based egg grading model demonstrated high accuracy and reliability, achieving:

Excellent detection precision and recall

Consistent classification across various lighting conditions

Smooth training convergence with minimal overfitting

This model can serve as a strong foundation for industrial egg sorting or quality assurance systems.

📦 Future Enhancements
🧠 Extend dataset with more egg varieties

📷 Real-time camera-based detection system

📱 Develop a mobile/web app interface for live grading

⚙️ Deploy model on edge devices such as Raspberry Pi or Jetson Nano

👩‍💻 Author
Priyanjan Perera
Bachelor of Information and Communication Technology (Hons) – Software Technology
University of Sri Jayewardenepura, Sri Lanka
