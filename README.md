# Depth-Estimation-in-Single-Image

Depth Estimation in a Single Image using Hugging Face & MiDaS

This project demonstrates how to estimate depth from a single 2D image using the MiDaS model from Intel-ISL
, integrated with Hugging Face and PyTorch. The application captures an image from a webcam, processes it through the MiDaS depth estimation model, and outputs a depth map as well as the estimated distance at any pixel coordinate selected by the user.

🚀 Features

Capture an image using your webcam inside Google Colab.

Apply MiDaS (small model) for depth prediction.

Generate and visualize a depth map.

Select any pixel coordinate and estimate the real-world distance (in units, meters, and centimeters).

Simple and interactive pipeline for beginners.

📂 Project Structure
Depth-Estimation/
│── Miniproject.ipynb   # Main notebook with code
│── README.md           # Documentation

⚙️ Installation

Run the following inside your Google Colab environment:

!pip install timm


Required libraries:

torch

opencv-python

matplotlib

timm

IPython

🖼️ How It Works

Capture an image

The code uses the browser’s webcam inside Google Colab.

Once you allow camera access, click Capture to take a photo.

Depth Estimation using MiDaS

Loads the MiDaS_small model from Intel-ISL via Torch Hub.

Preprocesses the image with MiDaS transforms.

Outputs a depth map using bicubic interpolation.

Pixel Distance Calculation

Enter pixel coordinates (x, y).

The model gives a relative depth value at that pixel.

Using a scaling factor (depth_scale), the relative depth is converted into:

Distance units

Meters

Centimeters

📊 Example Output

Input Image (captured via webcam)

Depth Map Visualization

Enter horizontal coordinate: 120
Enter vertical coordinate: 200

The distance at pixel (120, 200) is: 0.45 units
The distance at pixel (120, 200) is: 0.00012 meters
The distance at pixel (120, 200) is: 0.012 cm


(Values vary depending on calibration & input image)

📌 Notes

The MiDaS model predicts relative depth, not absolute metric distances.

To convert to real-world units, calibration with known objects or cameras is required.

depth_scale must be tuned depending on the use case.

🔮 Future Improvements

Support for larger MiDaS models (MiDaS_large) for higher accuracy.

Use Hugging Face Hub model versions for better portability.

Calibrate with real-world objects to achieve true metric depth estimation.

Extend for video streams instead of single images.

📚 References

Intel-ISL MiDaS Repository

PyTorch Torch Hub: MiDaS

Hugging Face Models
