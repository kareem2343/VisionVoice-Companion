# VisionVoice Companion

[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/) [![MIT License](https://badges.frapsoft.com/os/mit/mit.svg?v=102)](https://github.com/yourusername/VisionVoice/blob/main/LICENSE)

**AI-powered visual assistance for the visually impaired**  
Real‑time face recognition, text reading, and object detection using affordable hardware.

---

## 📖 Table of Contents

1. [Features](#-features)  
2. [Hardware Requirements](#-hardware-requirements)  
3. [Installation](#-installation)  

---

## 🚀 Features

- **👨‍👩‍👧 Face Recognition**  
  Identifies saved contacts and announces their presence.  
- **📖 Text Reading**  
  Converts printed text to clear audio.  
- **🥤 Object Detection**  
  Recognizes everyday items.  
- **🎚️ Simple Controls**  
  Single‑key mode switching: `F` (Faces), `T` (Text), `O` (Objects).  

---

## 💻 Hardware Requirements

- Standard USB webcam ($10–20)  
- Laptop or Raspberry Pi  
- **Optional:** 3D‑printed glasses mount ([design files](/mount_designs))  

---

## ⚙️ Installation

### 1. System Dependencies

<details>
<summary><strong>Windows</strong></summary>

1. **Tesseract OCR**  
   - Download & install from [UB Mannheim](https://github.com/UB-Mannheim/tesseract/wiki).  
   - ✔️ Add to system PATH  
   - ✔️ Install extra language packs (if needed)  
2. **Visual Studio Build Tools**  
   - Install [C++ build tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/).  
</details>

<details>
<summary><strong>Linux (Debian/Ubuntu)</strong></summary>

```bash
sudo apt update
sudo apt install tesseract-ocr libgl1-mesa-glx
