# VisionVoice Companion  
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Open Source Love](https://badges.frapsoft.com/os/mit/mit.svg?v=102)](https://github.com/yourusername/VisionVoice/blob/main/LICENSE)

**AI-powered visual assistance for the visually impaired** - Real-time face recognition, text reading, and object detection using affordable hardware.

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

## 💻 Hardware Requirements  
- Standard USB webcam ($10-20)  
- Laptop/Raspberry Pi  
- Optional: 3D-printed glasses mount ([design files](/mount_designs))  

---

## ⚙️ Step-by-Step Installation  

### 1. Install System Dependencies
**Windows:**  
1. Install [Tesseract OCR](https://github.com/UB-Mannheim/tesseract/wiki)  
   - During installation:  
     ✅ Add Tesseract to your system PATH  
     ✅ Install additional language data (if needed)  
2. Install [Visual Studio Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/)  
   - Select "C++ build tools" during installation  

**Linux (Debian/Ubuntu):**  
```bash  
sudo apt update
sudo apt install tesseract-ocr libgl1-mesa-glx
