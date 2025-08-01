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

```bash
git clone https://github.com/yourusername/fruit-color-detector.git
cd fruit-color-detector
2. Install dependencies
bash
Copy
Edit
pip install -r requirements.txt
3. Run the Flask app
bash
Copy
Edit
python app.py
Visit: http://localhost:5000

📂 Folder Structure
bash
Copy
Edit
.
├── app.py               # Main backend file
├── uploads/             # Stores uploaded images temporarily
├── results/             # Annotated output images
├── reports/             # Generated PDF reports
├── requirements.txt     # Python dependencies
└── README.md
🎯 API Usage
POST /upload
Upload images using key: images[]

Returns detection summary and PDF report links

GET /results/<filename>
View/download the annotated output image

GET /reports/<filename>
Download the generated PDF report

📊 Sample Output
json
Copy
Edit
{
  "results": ["result_image.jpg"],
  "pdf_files": ["red_fruits_report_20250801_123456.pdf"],
  "total_red_fruits": 3,
  "detection_details": [
    {
      "fruit": "Apple",
      "total_count": 2,
      "red_count": 2,
      "color": "Red"
    },
    {
      "fruit": "Banana",
      "total_count": 1,
      "red_count": 0,
      "color": "Yellow"
    }
  ]
}
📑 PDF Report Includes
Date & time of detection

Total number of fruits

Detected fruit types

Detected fruit colors

📺 Real-time Camera Detection
Use the live webcam feed to scan fruits:

Runs detection on frames from your webcam

Uses WebSocket (/start_camera) to stream detections

Annotated bounding boxes with fruit type + color

🍌 Supported Fruit Classes
Apple

Banana

Orange

Lime

(Any other class supported by the YOLOv8 model will also be detected.)

📥 requirements.txt
txt
Copy
Edit
ultralytics
opencv-python
flask
flask-socketio
flask-cors
numpy
reportlab
Install all using:

bash
Copy
Edit
pip install -r requirements.txt
🔮 Future Improvements
Add more color detection granularity (e.g., Brown, Purple)

Train a custom YOLOv8 model with more fruit varieties

Add drag-and-drop UI

Save user session results to DB

Deploy to HuggingFace or Render

📸 Demo Screenshots
(Add your screenshots here once the app is running)

📜 License
This project is under the MIT License.

🙌 Acknowledgements
Ultralytics YOLOv8

OpenCV

ReportLab

Flask + SocketIO

✨ Author
Vishnu – AI Engineer, Builder of Sky-Hostings

GitHub
