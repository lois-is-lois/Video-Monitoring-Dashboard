# Video Monitoring Dashboard

**Version**: v1.0  
**Authors**: Xu Xuan, Wang Yi, Gong Yeting (Beijing Jiaotong University)  
**Date**: April 2025  

> This system is provided "as-is" without any warranty of applicability, accuracy, or stability. Use at your own risk.

---

## 📖 Citation

If you use this system in your research, report, or project, please cite it as:

> Xu Xuan. Video Monitoring Dashboard (v1.0) [Computer Software]. Beijing Jiaotong University, 2025.

---

## 📌 Overview

Video Monitoring Dashboard is an intelligent video monitoring system based on an enhanced YOLOv8 model with a **Triple Attention Mechanism** that significantly improves detection accuracy in complex scenarios.

### ✨ Key Features

- **Triple Attention YOLOv8**: Integrates H/W/C attention branches to capture cross-dimensional features.
- **Real-Time Detection**: 20+ FPS performance depending on hardware.
- **Multi-Class Recognition**: Detects pedestrians, vehicles, hazardous objects, etc.
- **Web-based Dashboard**: Built with Flask and Echarts, supporting interactive alarms and result filtering.
- **Custom for Railway Scenarios**: Optimized for low-light, occlusion, and railway-specific object detection.

---

## 🏗️ System Architecture

### Architecture Layers

1. **Input Layer**: Supports real-time streams or local file uploads.
2. **Core Processing**: Triple Attention YOLOv8 for detection and tracking + alarm rules engine.
3. **Application Layer**: Flask-based dashboard, real-time visualization, heatmaps.
4. **Output Layer**: Annotated video streams with alerts.

### Technology Stack

- **Detection Framework**: YOLOv8 + Triple Attention (PyTorch 2.0+)
- **Data Processing**: OpenCV 4.5+, LabelImg for annotation
- **Backend**: Flask 2.3+
- **Frontend**: Echarts, OpenCV.js
- **Deployment Environment**:
  - Python 3.8–3.10
  - CUDA 11.7+ (if using GPU)
  - Supported on Windows 10/11

---

## ⚙️ Installation Guide

### System Requirements

| Component | Minimum | Recommended | Production |
|----------|---------|-------------|------------|
| **CPU** | Intel i5 / AMD Ryzen 5 | Intel i7 / Ryzen 7 | Xeon / EPYC |
| **GPU** | GTX 1660 (6GB) | RTX 3060 (12GB) | RTX 4090 / A100 (24GB+) |

### Installation Steps

1. **Prepare Environment**:
   ```bash
   conda create -n video_monitoring python=3.9 -y
   conda activate video_monitoring
Create Conda environment:

2. **Install dependencies:**:
```bash
  conda create -n video_monitoring python=3.9 -y
  conda activate video_monitoring
Install dependencies:

3. **Start the server:**:
   ```bash
   python app.py
Access the dashboard:
Open your browser and visit: http://10.60.210.37:5000/

### 🧑‍💻 Usage Guide
Web Interface Features
Login Page: Use default admin credentials (admin / admin)

Monitoring Dashboard:

### 📺 Original Video: Displays the raw input stream

### 🧠 Processed Video: Displays detection results in real-time

### 📊 Detection Count: Shows statistics for each object class

### 🗺️ 3D Map: Visualizes camera deployment and alert status

### 🚨 Warning Light: Turns red if hazardous objects are detected

Upload and Download
Use the "Choose File" button to upload local videos

Results are stored in the /processed directory for download

📁 Project Structure
复制
VideoMonitoringDashboard/
├── app.py                    # Flask main application
├── best.pt                   # Trained YOLOv8 weights with Triple Attention
├── T-attention.py            # Training script for attention-enhanced YOLOv8
├── T-attention.yaml          # Model configuration file
├── static/                   # Static assets (JS, CSS)
├── templates/                # HTML templates
├── uploads/                  # Directory for uploaded files
├── processed/                # Output results (annotated videos)
├── ultralytics/              # YOLOv8 base code
├── new_env.yml               # Conda environment setup file
├── ...
📎 Notes
The Triple Attention mechanism is based on a split-attention strategy across spatial and channel dimensions

Detection classes are customizable in the YAML config file

For best performance, use GPU acceleration

📖 License
This project is for academic demonstration only. Commercial use is not permitted without written authorization.

🙋 Contact
If you have questions, please contact:

Xu Xuan – Beijing Jiaotong University
Email: xuxuan@bjtu.edu.cn (example placeholder)

📄 Appendix
Additional documentation (in Chinese) is available in the /docs folder, including:

Dataset labeling standards

Model structure explanation

Training/validation/testing configuration


