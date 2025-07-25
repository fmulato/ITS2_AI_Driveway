# 🛡️ AI-Driven Driveway Safety System

### *Preventing Child Accidents Using Computer Vision*

**MSE806: Intelligent Transportation Systems – Assessment 2**

---

## 🚗 Project Overview

This project presents a smart rear-view camera system that enhances vehicle safety in residential environments. It uses advanced **computer vision** and **AI-based object detection** to identify vulnerable individuals—especially **children**, **pets**, and **livestock**—within the vehicle’s reversing path. The system provides **real-time visual and audible alerts**, significantly reducing the risk of tragic backover accidents during low-speed manoeuvres.

> 📉 In New Zealand alone, around **five children are killed or injured annually** in driveway accidents (Otago Daily Times, 2025).

---

## 🎯 Objectives

* Detect small or partially hidden **children**, **pets**, and **adults** during reverse operations.
* Reduce **false positives** using context-aware thresholds and configurable confidence levels.
* Offer **visual (GUI pop-ups)** and **auditory alerts**; future integration with **automatic braking systems**.
* Ensure **GDPR-compliant** local video processing without cloud dependency.

---

## 🔍 Key Features

* ⚡ **Real-time detection** using YOLOv5n (fine-tuned with new "kids" class).
* 🧒 Reliable detection of babies, toddlers, adults, and various animals.
* 📺 Visual alerts via GUI (Tkinter).
* 🔊 Audio alerts via PyAudio with adjustable sensitivity.
* 🎯 Customisable **confidence threshold** and consecutive frame detection logic.
* 💻 Lightweight model, deployable on **embedded hardware** (Jetson Nano, Raspberry Pi).

---

## 🧠 Technologies Used

| Type             | Tools/Frameworks          |
| ---------------- | ------------------------- |
| Language         | Python 3.x                |
| Object Detection | Ultralytics YOLOv5        |
| Image Processing | OpenCV                    |
| GUI              | Tkinter                   |
| Audio Alerts     | PyAudio, wave             |
| Embedded Support | Raspberry Pi, Jetson Nano |

---

## 🛠️ System Architecture

The architecture follows a real-time edge-computing model:

1. **Rear-view camera feed** captured.
2. **YOLOv5n model** detects objects.
3. Results passed to GUI/audio handler.
4. Optional **braking system** can be triggered.

> All data remains local—no video leaves the device.

---

## 🧪 Model Training & Improvements

* ✅ Fine-tuned YOLOv5n using transfer learning.
* ➕ Added a new custom class: **kids**.
* 🗂️ Trained on a hybrid dataset (COCO + Roboflow).
* 🧮 Achieved strong **Precision (0.85)** and **mAP\@50 (0.86)**.
* 📊 Tested under various lighting and occlusion conditions.
* 📉 Identified challenges: small object visibility, poor lighting.

---

## ⚖️ Ethical & Security Considerations

* All processing is performed **on-device**.
* No cloud storage or third-party access.
* Model retrained to reduce **bias** and enhance detection of underrepresented groups.
* Faces blurred in training data to protect privacy.

---

## 📈 Future Enhancements

* 🌙 Integrate **thermal or night vision** cameras for low-light conditions.
* 🧠 Explore newer, lightweight AI models (e.g., YOLOv8, MobileNet variants).
* 🔧 Enhance robustness through **larger and more diverse datasets**.
* 🚦Add **haptic feedback** and more granular driver assistance features.

---

## 📦 Installation

### Prerequisites

* Python 3.x
* Hardware: Raspberry Pi 4 / NVIDIA Jetson Nano

### Dependencies

```bash
pip install ultralytics opencv-python pyaudio
```

> `wave` is included in Python's standard library.

---

## 🚀 Getting Started

```python
# Example Inference
from ultralytics import YOLO
model = YOLO("best.pt")
results = model("sample_image.jpg")
results.show()
```

---

## 📚 Citation & Credits

Developed by:

* **Alfredo Jr. Albis Torrena**
* **Eunseok Choi**
* **Fabricio Mello Mulato**
* **Yan Huang**

Supervisor: *Mukesh Mishra*
Yoobee College of Creative Innovation – MSE806 (ITS)

---

## 📄 License

This project is released under an **academic licence** for educational purposes only.

---

