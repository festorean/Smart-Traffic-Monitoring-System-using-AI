
# 🚦 Smart Traffic Monitoring System using AI

### 📌 Overview

The **Smart Traffic Monitoring System using AI** is an automated solution designed to detect vehicles, recognize license plates, and identify traffic violations such as **overspeeding** and **red-light jumping** using **CCTV footage**.
This project uses **Deep Learning (YOLOv8)** for vehicle detection and **OCR (PaddleOCR)** for license plate recognition. It aims to assist traffic authorities in maintaining road safety and enforcing traffic laws efficiently.

---

### 🧠 Project Objectives

* Detect vehicles from live CCTV/video feeds using AI.
* Recognize vehicle number plates using Optical Character Recognition (OCR).
* Estimate vehicle speed from video frames.
* Generate automatic alerts for overspeeding and red-light violations.
* Store results (timestamp, detected plate, confidence, speed) in CSV format.

---

### 🧩 Key Features

✅ Real-time vehicle and plate detection
✅ OCR-based license plate reading
✅ Speed estimation using frame distance
✅ Automatic alert and report generation
✅ Modular and easy-to-train pipeline
✅ Runs on Google Colab or local GPU systems

---

### 🛠️ Tools & Technologies

| Category                          | Tools / Libraries    |
| --------------------------------- | -------------------- |
| **Programming Language**          | Python               |
| **Deep Learning Framework**       | YOLOv8 (Ultralytics) |
| **OCR Engine**                    | PaddleOCR            |
| **Computer Vision**               | OpenCV               |
| **Data Handling**                 | NumPy, Pandas        |
| **Visualization & UI (optional)** | Gradio / Streamlit   |
| **Environment**                   | Google Colab         |
| **Version Control**               | Git & GitHub         |

---

### 🧱 Project Structure

```
Smart-Traffic-Monitoring-System-using-AI/
│
├── data/
│   ├── images/
│   ├── videos/
│   └── test_samples/
│
├── notebooks/
│   ├── 01_yolo_training.ipynb
│   ├── 02_paddleocr_integration.ipynb
│   ├── 03_speed_estimation.ipynb
│   └── 04_final_pipeline.ipynb
│
├── models/
│   ├── yolov8_license_plate.pt
│   └── paddleocr/
│
├── results/
│   ├── detections/
│   └── csv_reports/
│
├── app/
│   └── gradio_interface.py
│
├── requirements.txt
├── README.md
└── LICENSE
```

---

### ⚙️ Installation & Setup

Run this in **Google Colab** to set up your environment:

```bash
!git clone https://github.com/your-username/Smart-Traffic-Monitoring-System-using-AI.git
%cd Smart-Traffic-Monitoring-System-using-AI

!pip install ultralytics paddleocr opencv-python pandas gradio
```

Then open the notebook:

```python
from ultralytics import YOLO
from paddleocr import PaddleOCR
import cv2, pandas as pd
```

---

### 🎯 Usage Steps

1. Upload or connect CCTV/video footage.
2. Run YOLOv8 for **vehicle and plate detection**.
3. Crop detected plates and use **PaddleOCR** to read text.
4. Compute **speed estimation** using frame time differences.
5. Export all results to a CSV file.
6. (Optional) Run the **Gradio interface** for live demonstration.

---

### 📊 Expected Output

| Timestamp           | Plate Number | Confidence | Speed (km/h) | Violation    |
| ------------------- | ------------ | ---------- | ------------ | ------------ |
| 2025-10-10 10:45:32 | GJ03AB1234   | 0.94       | 78.3         | Overspeeding |
| 2025-10-10 10:46:01 | GJ03CD5678   | 0.90       | 45.6         | Normal       |

---

### 🧾 Future Enhancements

* Integrate cloud database for live data storage.
* Add sound alerts for detected violations.
* Deploy model on Raspberry Pi or Jetson Nano for edge use.
* Use Indian Vehicle Dataset for custom YOLO training.

---

### 👨‍💻 Author

**Adebayo Festus Bamidele**
B.Tech Computer Engineering, Marwadi University (2026)
📧 [festorean@gmail.com](mailto:festorean@gmail.com)
🔗 [GitHub: festorean](https://github.com/festorean)

---
