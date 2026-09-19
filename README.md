# 🏍️ AI Motorcyclist Helmet Detection System (YOLOv8)

<div align="center">

[![YOLOv8](https://img.shields.io/badge/YOLOv8-Ultralytics-blue.svg?style=for-the-badge&logo=yolo)](https://github.com/ultralytics/ultralytics)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-EE4C2C.svg?style=for-the-badge&logo=pytorch&logoColor=white)](https://pytorch.org)
[![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-5C3EE8.svg?style=for-the-badge&logo=opencv&logoColor=white)](https://opencv.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

**Real-time computer vision system detecting helmet compliance for motorbike riders and pillion passengers from traffic surveillance video feeds.**

</div>

---

## 📌 Project Overview

Motorcycle road safety enforcement is a critical public safety challenge. This project implements a custom-trained **YOLOv8** deep learning model capable of accurately detecting:
- 🟢 Riders wearing helmets
- 🔴 Riders without helmets
- 👥 Multi-passenger (pillion) helmet compliance scenarios

Designed for direct integration with **traffic surveillance cameras, smart city CCTV systems, and law enforcement automated ticketing pipelines**.

---

## 🎯 Model Capabilities

| Class | Description | Compliance Action |
| :--- | :--- | :--- |
| **With Helmet** | Rider or passenger wearing an approved helmet | Verified ✅ |
| **Without Helmet** | Rider or passenger with head exposed | Violation Alert 🚨 |
| **Rider / Motorcycle** | Vehicle and occupant localization | Tracked 🏍️ |

---

## ⚡ Features

- **⚡ Real-Time High-FPS Processing**: Optimized inference for live RTSP traffic camera streams.
- **🎯 Multi-Class Localization**: Simultaneously detects riders, bikes, and headgear status in dense traffic.
- **🎥 Video Output Generation**: Automatically annotates violation bounding boxes and renders processed video.
- **📦 Pre-Trained Weights Included**: Ready-to-run custom weights saved in `model/best.pt`.

---

## 🛠️ Installation & Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/<your-username>/bike-helmet-detection.git
   cd bike-helmet-detection
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run Detection on Video**:
   ```bash
   python src/detect.py
   ```
   *Or specify custom input:*
   ```bash
   yolo task=detect mode=predict model=model/best.pt source=output_video.mp4 show=True
   ```

---

## 📂 Repository Structure

```text
bike-helmet-detection/
├── model/
│   └── best.pt               # Trained YOLOv8 model weights
├── results/                  # Validation metrics, confusion matrices, and charts
├── src/
│   └── detect.py             # Inference pipeline script
├── output_video.mp4          # Sample input/output demonstration video
├── requirements.txt          # Python dependencies
├── LICENSE                   # Apache 2.0 License
└── README.md
```

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for details.
