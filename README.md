# Ai-project-
There is most important project

# Multi-Object Tracking Pipeline

## Project Overview
This project detects and tracks multiple moving subjects in a public video using YOLO + tracking.

## Model / Tracker Choice
- Detector: YOLOv8
- Tracker: ByteTrack (or DeepSORT)
Reason:
- Fast detection
- Good ID consistency
- Handles occlusion reasonably well

## Dependencies
Install required packages:

pip install ultralytics opencv-python numpy

Dependencies:
- Python 3.x
- OpenCV
- Ultralytics YOLO
- NumPy

## Installation Steps
1. Clone repository

git clone <your-repo-url>

2. Move into project folder

cd project-folder

3. Install dependencies

pip install -r requirements.txt

## How to Run the Pipeline

Place input video in project folder.

Run:

python main.py

Or in Jupyter Notebook:

Run all notebook cells in sequence.

Pipeline flow:
Input Video
→ Frame Extraction
→ Object Detection
→ Multi-Object Tracking
→ Visualization
→ Output Video

## Assumptions Taken
- Subjects remain visible in most frames
- Camera motion is moderate
- Pretrained YOLO can detect relevant objects
- IDs remain stable except under heavy occlusion

## Limitations
- ID switches may happen
- Heavy crowd occlusion may reduce tracking quality
- Fast motion may cause missed detections
- Accuracy depends on pretrained model performance

## Output
- Annotated tracked video
- Bounding boxes with IDs
- Optional trajectory analysis
