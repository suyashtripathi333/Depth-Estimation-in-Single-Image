# 🌌 Depth Estimation in a Single Image

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-Framework-red.svg)](https://pytorch.org/)
[![Hugging Face](https://img.shields.io/badge/Model-MiDaS-yellow.svg)](https://huggingface.co/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Estimate **depth from a single 2D image** using the **MiDaS model** from Intel-ISL, integrated with **Hugging Face** and **PyTorch**.  
This project captures an image from your webcam in **Google Colab**, processes it through MiDaS, and outputs:  
- A **depth map**  
- The **estimated distance** at any pixel coordinate  

---

## 🚀 Features
- 📸 Capture an image using your webcam inside Google Colab  
- 🔍 Apply MiDaS (small model) for depth prediction  
- 🖼️ Generate and visualize a depth map  
- 🎯 Select any pixel and estimate distance (units, meters, centimeters)  
- 🧑‍💻 Simple and interactive pipeline for beginners  

---

## 📂 Project Structure



---

## ⚙️ Installation

Run this inside **Google Colab**:

```bash
!pip install timm

Required libraries:

torch

opencv-python

matplotlib

timm

IPython


🖼️ How It Works
1. Capture an Image

Uses your browser’s webcam inside Colab.

Allow camera access → click Capture → take a photo.

2. Depth Estimation using MiDaS

Loads MiDaS_small from Intel-ISL (via Torch Hub).

Preprocesses image with MiDaS transforms.

Outputs a depth map (resized with bicubic interpolation).

3. Pixel Distance Calculation

Enter pixel coordinates (x, y).

Model returns relative depth at that pixel.

Converts to:

Distance units

Meters

Centimeters


Enter horizontal coordinate: 120
Enter vertical coordinate: 200

The distance at pixel (120, 200) is: 0.45 units
The distance at pixel (120, 200) is: 0.00012 meters
The distance at pixel (120, 200) is: 0.012 cm


📌 Notes

MiDaS predicts relative depth, not absolute distances.

Real-world metric conversion needs camera calibration.

depth_scale must be tuned per use case.


