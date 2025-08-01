# Fruit-Color-Detection

 🍎 Fruit Color Detection and Report Generator

An AI-powered fruit detection web service using YOLOv8 and OpenCV. The system detects fruits (like apples, oranges, bananas, and limes), determines their dominant color (e.g., red, green, yellow), and generates a detailed PDF report.

Built with Flask + WebSocket for live image processing and reporting.

---

## 📸 Features

- 🧠 Detects fruits in images (apples, bananas, oranges, limes)
- 🎨 Detects and classifies color of fruits (Red, Green, Orange, Yellow, etc.)
- 📑 Generates downloadable PDF reports with detection data
- 📷 Supports real-time webcam-based fruit detection
- 🖼 Draws bounding boxes with fruit names and color
- 🔄 Supports multiple images upload

---

## 🛠 Tech Stack

- **Framework**: Python + Flask + Flask-SocketIO
- **Model**: YOLOv8 via Ultralytics
- **Image Processing**: OpenCV
- **PDF Generation**: ReportLab
- **WebSocket**: Flask-SocketIO

---

## 📦 Installation

### 1. Clone the repository
```
git clone https://github.com/yourusername/fruit-color-detector.git
cd fruit-color-detector
2. Install dependencies
pip install -r requirements.txt
3. Run the Flask app
python app.py

```

---
```
📂 Folder Structure
.
├── app.py               # Main backend file
├── uploads/             # Stores uploaded images temporarily
├── images/             # Images used for testing
├── results/             # Annotated output images
├── static/             # Main Frontend Files
├── reports/             # Generated PDF reports
├── requirements.txt     # Python dependencies
└── README.md
```
---

📑 PDF Report Includes
Date & time of detection

Total number of fruits

Detected fruit types

Detected fruit colors

---

📺 Real-time Camera Detection
Use the live webcam feed to scan fruits:

Runs detection on frames from your webcam

Uses WebSocket (/start_camera) to stream detections

Annotated bounding boxes with fruit type + color

---

🍌 Supported Fruit Classes
Apple

Banana

Orange

Lime

(Any other class supported by the YOLOv8 model will also be detected.)

---

📸 Demo Screenshots
(Add your screenshots here once the app is running)

📜 License
This project is under the GPL 3.0 License.

🙌 Acknowledgements
Ultralytics YOLOv8

OpenCV

ReportLab

Flask + SocketIO

✨ Author
Vishnu – AI Engineer, Builder of Sky-Hostings
