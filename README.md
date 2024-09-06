# Powerlifting Barbell and Body Structure Tracking App

## Overview
This app processes training videos of powerlifters (MP4 format) and provides a visual analysis of the barbell's movement path and the athlete's body structure. Using OpenCV for video processing and pose estimation libraries, the app tracks both the barbell and key body joints during lifts (squat, bench press, deadlift).

## Features
- **Barbell Path Tracking**: Detects and visualizes the barbell’s movement throughout the lift.
- **Body Structure Analysis**: Detects key body joints (shoulders, elbows, knees, etc.) for biomechanical feedback.
- **Performance Metrics**: Calculates range of motion (ROM), barbell speed, joint angles, and more.
- **Easy-to-Use Interface**: Upload your MP4 video, and the app automatically processes and displays results.

## Installation

### Requirements
- Python 3.8+
- OpenCV
- Mediapipe or OpenPose
- Tkinter (for desktop UI) or Flask/Django (for web UI)

### Steps
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/powerlifting-app.git
    cd powerlifting-app
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the app (for desktop version):
    ```bash
    python app.py
    ```

   Or for web version (if using Flask):
   ```bash
   flask run
