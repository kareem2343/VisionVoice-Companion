markdown
# VisionVoice Companion  
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Open Source Love](https://badges.frapsoft.com/os/mit/mit.svg?v=102)](https://opensource.org/licenses/MIT)

**AI-powered visual assistance for the visually impaired** - Real-time face recognition, text reading, and object detection using affordable hardware.

---

## 📋 Table of Contents
- [Features](#-features)
- [Requirements](#-requirements)
- [Installation](#%EF%B8%8F-installation)
- [Setup](#-setup)
- [Usage](#-usage)
- [Technical Details](#-technical-details)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🚀 Features  
- **👨‍👩‍👧 Face Recognition**  
  Identifies saved contacts and announces their presence  
- **📖 Text Reading**  
  Converts printed text to clear audio  
- **🥤 Object Detection**  
  Recognizes everyday items  
- **🎚️ Simple Controls**  
  Single-key mode switching: `F` (Faces), `T` (Text), `O` (Objects)  

---

## 📦 Requirements

### Hardware
- USB webcam (any standard model)
- Computer/Raspberry Pi
- (Optional) 3D-printed glasses mount

### Software
```text
# Python Dependencies (requirements.txt)
opencv-python==4.8.0
numpy==1.24.3
face-recognition==1.3.0
pyttsx3==2.90
pytesseract==0.3.10
Pillow==9.5.0
scipy==1.10.1
⚙️ Installation
1. System Setup
Windows:

Install Tesseract OCR (add to PATH)

Install Visual Studio Build Tools

Linux:

bash
sudo apt update && sudo apt install tesseract-ocr libgl1-mesa-glx
2. Project Setup
bash
# Clone repository
git clone https://github.com/yourusername/VisionVoice.git
cd VisionVoice

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate    # Windows

# Install dependencies
pip install -r requirements.txt

# Download AI models
curl -O https://raw.githubusercontent.com/pjreddie/darknet/master/data/coco.names
curl -O https://raw.githubusercontent.com/AlexeyAB/darknet/master/cfg/yolov4.cfg
curl -O https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights

# Create data folders
mkdir KNOWN_FACES KNOWN_OBJECTS
🛠️ Setup
Folder Structure
text
VisionVoice/
├── KNOWN_FACES/        # Store face images as name.jpg
├── KNOWN_OBJECTS/      # Auto-saved object images
├── visionvoice.py      # Main application
└── requirements.txt    # Dependencies
First Run
Add photos of known people to KNOWN_FACES (e.g., john.jpg)

For objects: Run app and press S in object mode to capture new items

🖥️ Usage
Running the App
bash
python visionvoice.py
Controls
Key	Action
F	Face Mode
T	Text Mode
O	Object Mode
S	Save Item (Object Mode)
Q	Quit
Example Workflow
Point camera at person → "Unknown face detected"

Enter name → "John saved"

Next time: "John is here"

🧩 Technical Details
Architecture
Diagram
Code






Raspberry Pi Setup
bash
# Create startup service
sudo bash -c 'cat > /etc/systemd/system/visionvoice.service <<EOF
[Unit]
Description=VisionVoice
After=network.target

[Service]
ExecStart=$(which python) $(pwd)/visionvoice.py
WorkingDirectory=$(pwd)
User=$USER
Restart=always

[Install]
WantedBy=multi-user.target
EOF'

# Enable service
sudo systemctl enable visionvoice.service
sudo systemctl start visionvoice
🚨 Troubleshooting
Common Issues
Camera Not Detected

python
# In visionvoice.py, change:
video_capture = cv2.VideoCapture(0) → Try 1, 2, etc.
Slow Performance

python
# Add to visionvoice.py:
video_capture.set(cv2.CAP_PROP_FRAME_WIDTH, 640)
video_capture.set(cv2.CAP_PROP_FRAME_HEIGHT, 480)
Tesseract Errors

python
# Set correct path:
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'  # Windows
# OR
pytesseract.pytesseract.tesseract_cmd = '/usr/bin/tesseract'  # Linux
🤝 Contributing
Fork the project

Create your feature branch (git checkout -b feature/amazing-feature)

Commit changes (git commit -m 'Add amazing feature')

Push to branch (git push origin feature/amazing-feature)

Open Pull Request

📜 License
Distributed under the MIT License. See LICENSE for more information.
