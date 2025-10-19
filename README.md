# 🏍️ Bike Helmet Detection using YOLOv8

This project focuses on detecting whether bike riders and pillion passengers are wearing helmets or not, using a custom-trained **YOLOv8 model**. The system can accurately identify multiple scenarios such as both wearing helmets, only the driver wearing, or neither wearing.

---

## 📘 Project Overview

Road safety is a critical issue, especially for motorbike riders. This project leverages **computer vision and deep learning (YOLOv8)** to automatically detect:
- Riders without helmets
- Riders with helmets
- Passenger helmet compliance

This model can be integrated with **traffic monitoring systems, CCTV surveillance**, or **law enforcement automation** for helmet rule enforcement.

---

## 🎯 Objectives

- Detect motorbike riders in real-time.
- Identify whether the driver and passenger are wearing helmets.
- Support automatic video or image-based safety analysis.
- Provide accurate detections in various lighting and environmental conditions.

---

## 🧠 Classes Description

| Class Name | Description |
|-------------|-------------|
| **DHelmet** | Driver with Helmet |
| **DHelmetP1Helmet** | Driver and Passenger both wearing Helmets |
| **DHelmetP1NoHelmet** | Driver wearing Helmet, Passenger without Helmet |
| **DNoHelmet** | Driver without Helmet |
| **DNoHelmetP1Helmet** | Driver without Helmet, Passenger with Helmet |
| **DNoHelmetP1NoHelmet** | Driver and Passenger both without Helmets |

---

## 🧩 Model Details

- **Model Type:** YOLOv8 (You Only Look Once - Version 8)
- **Framework:** Ultralytics YOLOv8
- **Input Size:** 640×640
- **Dataset Format:** YOLO format
- **Training Epochs:** Customizable
- **Hardware:** GPU recommended (e.g., NVIDIA RTX)

