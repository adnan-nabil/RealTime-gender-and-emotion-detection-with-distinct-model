# RealTime-gender-and-emotion-detection-with-distinct-model

This project implements a real-time detection system that captures frames from a webcam, detects faces, classifies gender, and predicts emotions using pre-trained deep learning models. The system leverages YOLOv8 for face detection and gender classification, and Facebook's DeiT Tiny model for emotion recognition.
Project Overview

    Face Detection & Gender Classification:
    A YOLOv8 small model detects faces in real-time video streams and classifies the gender of detected individuals.

    Emotion Detection:
    The cropped face images are passed to a fine-tuned Facebook DeiT Tiny model, which predicts the emotion (happy, sad, or neutral).

Key Features

    Real-Time Processing:
    Captures frames from the webcam and processes them instantly.

    Multi-Model Integration:
    Combines the power of YOLO for object detection and DeiT for emotion recognition.

    Efficient and Lightweight:
    Utilizes small, optimized models to ensure smooth performance on standard hardware.

Models Used

    YOLOv8 Small:
        Purpose: Face detection and gender classification.
        Trained on: Custom gender-labeled dataset.
    Facebook DeiT Tiny:
        Purpose: Emotion recognition.
        Trained on: Custom emotion dataset (happy, sad, neutral).

Installation
Requirements

    Clone this repository:

git clone https://github.com/yourusername/RealTime-gender-and-emotion-detection.git
cd RealTime-gender-and-emotion-detection

Install dependencies:

    conda create -n your_env_name python=3.8  # or any version you're using
    conda activate your_env_name
    pip install -r requirements.txt

Usage

    Activate the Conda environment:

conda activate your_env_name

Run the application:

    python main.py

Folder Structure

RealTime-gender-and-emotion-detection/
│
├── gender-yolo-v8-small-epoch80/    # YOLOv8 model files
│   ├── best.pt
│   └── results.csv
│
├── emotion-fb-deit-tiny-epoch50/    # DeiT model files
│   ├── model.safetensors
│   └── config.json
│
├── training-pipeline/
│   ├── gender-detection-yolos.ipynb
│   └── emotion-detection-fb-deit.ipynb
│
├── main.py                          # Main script to run the real-time system
├── requirements.txt
└── README.md

Future Improvements

    Add support for more emotions.
    Implement an optimized GUI using PyQt.
    Improve face detection accuracy with larger datasets.
