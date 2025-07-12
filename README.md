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
