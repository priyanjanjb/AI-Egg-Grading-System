# 🥚 AI-Egg-Grading-System using YOLOv8

This project introduces an intelligent **AI-powered Egg Grading and Quality Detection System** built using **Ultralytics YOLOv8**, a state-of-the-art object detection framework.  
The system automates the traditional egg grading process by detecting and classifying eggs based on their surface quality (such as *Clean*, *Cracked*, or *Dirty*), ensuring **faster, consistent, and reliable** quality assessment for the poultry industry.

---

## 🎯 Project Objective

Manual egg grading is **time-consuming**, **inconsistent**, and **subjective**.  
This project aims to develop an **automated computer vision-based system** that:

- 🥚 Detects eggs in real-time from images or video streams  
- 🧩 Classifies eggs into quality-based categories (*Clean, Cracked, Dirty*)  
- 📈 Evaluates model performance using standard metrics (Precision, Recall, mAP)

---

## 🚀 Key Features

- ⚡ **YOLOv8-powered detection** for fast and accurate results  
- 🧠 Classifies eggs as *Clean*, *Cracked*, or *Dirty*  
- ☁️ Trained on **Google Colab** with Google Drive integration  
- 📊 Visualizes metrics such as **Precision**, **Recall**, **mAP**, and **Loss curves**  
- 🧩 Modular design for easy integration into industrial workflows  
- 💾 Trained model exported for deployment and inference  

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
| Hardware | GPU Runtime (Google Colab Pro) |

---

## ⚙️ Setup and Installation

### 1️⃣ Open in Google Colab
Run the notebook directly in **Google Colab** (recommended for quick setup and GPU support).

### 2️⃣ Install Dependencies
```bash
!pip install ultralytics tqdm
```

### 3️⃣ Verify Installation
```python
import ultralytics
ultralytics.checks()
```

### 4️⃣ Mount Google Drive
```python
from google.colab import drive
drive.mount('/content/drive')
```

---

## 🧠 Model Training

Train the YOLOv8 model with your dataset:
```bash
!yolo task=detect mode=train model=yolov8n.pt data=/content/drive/MyDrive/EggGradingFYP/data.yaml epochs=10 batch=32 project=/content/drive/MyDrive/EggGradingFYP/result name=egg
```

---

## 📈 Training Results

| Metric | Value |
|--------|-------|
| Precision | 0.919 |
| Recall | 0.913 |
| mAP@0.5 | 0.974 |
| mAP@0.5:0.95 | 0.973 |
| Epochs | 10 |

📁 Training results, metrics, and plots are saved in:
```
/content/drive/MyDrive/EggGradingFYP/result/egg
```

---

## 🔍 Model Inference (Prediction)

Run inference on test images:
```bash
!yolo task=detect mode=predict model=/content/drive/MyDrive/EggGradingFYP/result/egg/weights/best.pt source=/content/drive/MyDrive/EggGradingFYP/test/images
```

📂 Predictions will be saved in:
```
/runs/detect/predict/
```

---

## 📸 Sample Outputs

| Image | Classification |
|--------|----------------|
| 🥚 | Clean Egg |
| 🥚 | Cracked Egg |
| 🥚 | Dirty Egg |

*(You can add screenshots of your model’s predictions here.)*

---

## 📊 Performance Summary

The YOLOv8-based egg grading system achieved **high accuracy and robustness**, showing:

- ✅ Excellent detection precision and recall  
- 💡 Consistent performance under varied lighting conditions  
- 📉 Smooth training convergence with minimal overfitting  

This model provides a **reliable foundation** for real-world industrial egg grading and quality assurance systems.

---

## 🔮 Future Enhancements

- 🧠 Extend dataset with more egg varieties and lighting conditions  
- 📷 Develop a **real-time camera-based detection** system  
- 📱 Build a **mobile/web app interface** for live grading  
- ⚙️ Deploy on **edge devices** (Raspberry Pi, Jetson Nano)  

---

## 👩‍💻 Author

**Priyanjan Perera**  
🎓 Bachelor of Information and Communication Technology (Hons) – Software Technology  
🏛️ University of Sri Jayewardenepura, Sri Lanka  

---

## 🌐 Repository Name Suggestion
**`AI-Egg-Grading-System-YOLOv8`**

---

⭐ *If you find this project helpful, don’t forget to star the repository!*
